.. functions-metadata:

####################
Functions - metadata
####################


.. function:: metadata($record, $field, $options = array())

   Get element set or property information from a record

   :since: 2.0
   :param string|record $record: If string, the record type to use. If record, an :php:class:`Omeka_RecordAbstract`
   :param string|array $field: If array, the element set and element name, like ``array('Dublin Core', 'Title')``. If string, the property to look up.
   :param string|array $options: 
     * 'all': If true, return an array containing all values for the field.
     *  'delimiter': Return the entire set of metadata as a string, where
          entries are separated by the given delimiter.
     * 'index': Return the metadata entry at the given zero-based index.
     * 'no_escape' => If true, do not escape the resulting values for HTML
          entities.
     * 'no_filter': If true, return the set of metadata without
          running any of the filters.
     * 'snippet': Trim the length of each piece of text to the given
          length in characters.
     * Passing simply the string 'all' is equivalent to array('all' => true)
     * Passing simply an integer is equivalent to array('index' => [the integer])
   :returns: string|array|null Null if field does not exist for record. Array if certain options are passed. String otherwise 
   
Usage Examples
--------------
.. code-block:: html+php

   <h1><?php echo metadata('item', array('Dublin Core', 'Title')); ?></h1>
   

See Also
--------


* :php:meth:`Omeka_RecordAbstract::save`
* :php:func:`loop` 

