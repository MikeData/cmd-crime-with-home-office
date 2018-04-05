# Crime

Done but various things to be aware of:

### Years Extracted

For now it's only '2017-18', that may change.

You can change `for sheetName in sheets[-1:]:` in the "Build Initial Files" code block to include additional years.


### Financial vs Calendar Years

This data uses financial years. There is a hacky switch for converting to rough calendar year equvilents but it's best
avoided.

I've put the Q in the financial quarters version regardless (i.e 1 = Q1) as that seems to be our convention.


### Hierarchy

The "Offences" dimension has a hierarchy. A file named Hierarchy_CSV_Offences.csv" will be generated when you run the notebook. This can be used to create a hiearchy.cypher file for cmd using:
https://github.com/ONSdigital/dp-hierarchy-builder/tree/feature/crimeMissingNodes/cmd/hierarchy-transformer

This shouldn't always be necessary but if additional codes are added to the data they will need hierarcical representation.


### Codelists

Generates some rough codelist CL_ files but if changed make sure to keep in sync with recipeAPI/hierarchy.cypher and loadfile.


### Inserting Parent Nodes

If needed/deemed wise, you can insert (sub)total observations into the V4 file for data points representing the empty parent codes in the heriarchy (groups and subGroups). You can use the v4 file (FINANCE_ ... etc) and the heriarchy CSV with the following to insert them.
https://github.com/ONS-OpenData/cmd-v4-hierarchy-parent-injector

