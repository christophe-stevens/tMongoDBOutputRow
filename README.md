# tMongoDBOutputRow


When using tMongoDBOutputRow with large shema (>1800 columns) I bumped into the 655535 method size limit. ( binary size of the method is too big). 

This is because the component adds all the columns one by one in the globalMap. 

This alternative version create a List<String> of columns and then loops through the List<String> to add them to the globalMap. 

It does exactly the same as the orginal method but the source code size should be reduced! 