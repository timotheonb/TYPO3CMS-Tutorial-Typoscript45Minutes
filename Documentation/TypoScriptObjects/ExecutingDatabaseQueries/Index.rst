.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. _cobjects-database-queries:

Objects executing database queries
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- :ref:`CONTENT <t3tsref:cobj-content>` offers the functionality to
  access arbitrary tables of TYPO3 internals. This does not just
  include tt\_content, but also tables of extensions, and so on, can be
  referenced. The function "select" allows us to generate complex SQL
  queries.

- :ref:`RECORDS <t3tsref:cobj-records>` offers the functionality to
  reference specific data records. This is very helpful, if the same
  text has to be present on all pages. By using RECORDS, a single
  content element can be defined, which will be shown. Thus, an editor
  can edit the content without the need to copy the element numerous
  times. This object is also used, if the content element "insert
  record" is used.

  In the following example, the email address from an address record is
  rendered and linked as email at the same time. ::

     page.80 = RECORDS
     page.80 {
           source = 1
           tables = tt_address
           conf.tt_address = COA
           conf.tt_address {
                   20 = TEXT
                   20.stdWrap.field = email
                   20.stdWrap.typolink.parameter.field = email
           }
     }

- :ref:`HMENU <t3tsref:cobj-hmenu>` imports the page tree and offers
  comfortable ways to generate a menu of pages. Aside the menu which
  renders the page tree, there are some special menus, which allow
  various ways of usage. This object imports the internal structure for
  these menus. How a menu will be rendered depends on menu objects like
  TMENU (text menu) or GMENU (graphical menu). For every menu level,
  the object can be changed. Within a menu level, there are various
  menu items. For every item, we can define the differing states (NO =
  normal, ACT = active, etc.).

