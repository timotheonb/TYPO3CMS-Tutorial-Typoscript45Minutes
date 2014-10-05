.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. _prerequisites:

Prerequisites
^^^^^^^^^^^^^

We assume that the reader has a :ref:`TYPO3 system up and running
<t3install:start>` and that the basic operations for installation are known. The
difference between pages and content elements will not be elaborated
on here. We also assume that you know that the content of a page is
put together by a combination of various content elements. Just to be clear, we point out the fact that these content elements are
stored in the table tt\_content. The database field "CType" defines
which typoe of content element we have. Depending on the CType, an appropriate
mask is loaded.

For a better understanding of TYPO3 and TypoScript, it is helpful to
study the database. The phpmyadmin extension enables easy access to the
database from the backend, where the relationships between the pages,
tt\_content and the backend can be studied. It should be understood
that PID (Page ID) stands for the ID of a page while UID (Unique ID)
stands for a unique record.

