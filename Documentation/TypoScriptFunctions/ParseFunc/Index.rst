.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. _function-parsefunc:
.. _parsefunc:

parseFunc
^^^^^^^^^

This function parses the main part of the content, i.e., the content
which has been entered in the Rich Text Editor. The function is
responsible for the fact that the content is not rendered exactly as
it was entered in the RTE. Some default parsing rules are implemented
in "css\_styled\_content"; a part of them has already been explained in
the :ref:`encapsLines chapter <encapslines>`. If we liked to change how
TYPO3 wraps something, most of the time this can be done with a
parseFunc instruction. We could also use parseFunc to search and
replace a certain string.

In the following example, every occurrence of "COMP" is replaced by
"My company name". ::

   page.stdWrap.parseFunc.short {
    COMP = My company name
    }

The various possibilities of changing the default behavior can be found
by using the TypoScript object browser. All possibilities of how
parseFunc can alter the rendering can be found here: :ref:`parseFunc
<t3tsref:parsefunc>`.

