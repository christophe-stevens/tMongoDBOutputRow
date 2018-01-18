# tMongoDBOutputRow


When using tMongoDBOutputRow with large shema (>1800 columns) I bumped into the 655535 method limit. ( binary size of the method is too big). 

This is because teh component add all the column one by one in the globalMap. 

This alternative version create a List<String> of columns and then loops through the List<String> to add to the globalMap. 

It does exactly the same as the orginal method but the source code size should be reduced! 