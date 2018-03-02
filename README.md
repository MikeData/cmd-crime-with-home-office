# Crime

Done but various things to be aware of:

### Years Extracted

I've only used '2015-16', '2016-17' and '2017-18'.
Anything before that and the inconsistencies in labels, codes and "outcomes" gets out of hand. Earlier might be possible but it'll be a pain.


### Financial vs Calendar Years
This data uses calendar years and numeric only quarters. So a time|type of 2017/2018|1 which may or may not equate to 2017 Q2, unsure so have included both versions.

I've put the Q in the financial quarters version regardless (i.e 1 = Q1) as that seems to be our convention.


### Sparsity

There will be some sparsity with more recent data. This is a consequence of it being quarterly updated data (i.e the update for Q1 2018 will add 2018 as a dimension combination before we have data for Q2, Q3, and Q4 of that year).

There are  likely to be other causes of sparsity in here as well.


### Hierarchy

The "Offences" dimension has a hierarchy. Can't see an obvious pattern in the codes but it's in separate columns. Have included a hierachy.cypher file in this repo that'll build it for cmd.


### Codelists

included some codelist CL_ files but if changed make sure to keep in sync with recipeAPI/hierarchy.cypher and loadfile.
