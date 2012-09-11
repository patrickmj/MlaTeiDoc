.. functions-loop:

################
Functions - loop
################


.. function:: loop($recordsVar, $records = null)

   Loop through records for display
   
   :since: 2.0
   :param string $recordsVar: The variable name for the loop. Typically corresponds to the record type, e.g., 'items', 'collections', etc.
   :param array $records: An array of records to loop through. If null, this is looked up by $recordsVar
   :returns: array of records to loop through
   
Usage Examples
--------------
.. code-block:: html+php

   <?php foreach(loop('items') as $item): ?>
      <h1><?php echo metadata('items', array('Dublin Core', 'Title')); ?></h1>
   <?php endforeach; ?>

See Also
--------

* :php:func:`metadata`