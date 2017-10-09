# Wikidata - the Sherlock Holmes investigative AI## Given personal information about a person determine the probable cause of death.Personal information is provided in wikidata format, for example: [Abraham Lincoln](https://www.wikidata.org/wiki/Q91). Given all other information and entity links you need to build a classifier that would determine the most probable manner of death (you should not use manner of death or cause of death fields as your input data).There are many such manners defined in wikidata, but we are interested in the 4 most common ones:```natural causes 29764
suicide 6094
accident 5384
homicide 4523
```You can use the whole [wikidata dump](https://www.wikidata.org/wiki/Wikidata:Database_download), or SPARQL queries to gather the data to use. You need to devise training and evaluation procedure yourself. We are interested in a solution with good performance, that would be easy to improve and evaluate. It should also be built in a limited amount of time - a minimal working proof-of-concept will do.See also:[Most common high-level causes](https://query.wikidata.org/#SELECT%20%3FsomehowLabel%20%28count%28%3Fsomeone%29%20as%20%3Foccurences%29%20WHERE%20%7B%0A%20%20%3Fsomeone%20wdt%3AP1196%20%3Fsomehow.%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22en%22.%20%7D%0A%7D%0AGROUP%20B)

[Overall causes of death ranking](https://query.wikidata.org/#%23Overall%20causes%20of%20death%20ranking%0A%23added%20before%202016-10%0A%0A%23defaultView%3ABubbleChart%0A%23TEMPLATE%3D%7B%22template%22%3A%22Overall%20causes%20of%20death%20ranking%20of%20%3Fthing%20%22%2C%22variables%22%3A%7B%22%3Fthing%22%3A%20%7B%)