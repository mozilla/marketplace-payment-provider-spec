Marketplace Payments Specification
==================================

This is a document outlining the payments specification for working with the
Marketplace Payments systems.

For a functional reference implementation of this specification, please check out zippy: http://zippypayments.readthedocs.org/en/latest/

These docs are also available as a PDF: https://media.readthedocs.org/pdf/marketplace-payments-specification/latest/marketplace-payments-specification.pdf

Overview
-----------

Sellers
~~~~~~~

In the Marketplace, **sellers** are the **developers** who are wanting to place something
for sale on the app market. They will need to create an account with the
payment provider:

* Setting up a developer account so that a developer can recieve payment.
* Registering one or more products with the payment provider.
* Any further configuration that the product needs.
* Confirming that data is all set up correctly.

See the :ref:`developer documentation <developer-label>`.

Payment
~~~~~~~

* The :ref:`transaction API <transactions>` to start the flow.
* Pages that should be shown and hosted by the payment provider.

See the :ref:`payment documentation <payment-label>`.

Reporting
~~~~~~~~~

* Reporting of transactions back to developers.

See the :ref:`reporting documentation <reporting-label>` documentation.

Miscellaneous
~~~~~~~~~~~~~

* Refunds and chargebacks, see :ref:`refunds <refunds-label>`
* Token checking and other security, see :ref:`security <security-label>`
* Status, see :ref:`status <status-label>`


Contents:

.. toctree::
   :maxdepth: 2

   developer.rst
   payments.rst
   reporting.rst
   refunds.rst
   security.rst
   miscellaneous.rst
   flow.rst
   faq.rst


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

