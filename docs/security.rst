.. _security-label:

Security
========


Token checking
--------------

If a the Marketplace server send you a notice, this API allows you to cryptographically
verify that the Marketplace really sent you that notice.

.. _notice-api:

.. http:post:: /notices

    **Request**

    :param qs:
        In some cases the Marketplace may redirect to a URL on your server.
        This parameter is the complete query string (after the '?') that the Marketplace sent to you.
        Example: ``result=success&transaction_id=123&sig=0:1bcde2f3fccdd...``

    **Response**

    If the signature of the notice is correct you can trust that all values in
    the query string were sent to you by the the Marketplace service.

    :param result:
        Result of the signature check. Possible values: ``OK``, ``FAIL``.

    :param reason:
        In the case of a failure, this is the reason why.

    A successful signature check results in this:

    .. code-block:: json

        {
          "result": "OK",
        }

    A failed signature check looks like this (this is a 200 response):

    .. code-block:: json

        {
          "result": "FAIL",
          "reason": "signature mismatch"
        }

    In case of an error:

    .. code-block:: json

        {
          "code": "InvalidArgument",
          "message": {
            "qs": "This field is required."
          }
        }

    :status 200: success.
    :status 409: conflict.
