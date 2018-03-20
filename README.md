# Data Wrangling with MongoDb

The data file is downloaded from mapzen, which is not offering its services any more. I have downloaded the data and performed the data munging on the raw data.

## Ideas to Improve the DataSet

I would like to summarise the problems encountered in auditing this part of the data and how I handled them :

1. The 'key' with 'mahesh' as value, it would be more approriate if it had been 'name', as that node represents the address of a person whose name is 'Mahesh Kumar'. I have changed this while importing the data into MonogoDb.
2. I have excluded the 'fixme' nodes, as they need further improvement and it is clearly mentioned that no copyrighted content should be used to improve those nodes in osm website.
3. A certain postcode which has 7 characters in it, I have striped off the space before converting it to int.
4. The street names where 'Telangana'( name of the state ) is included. I have stripped off the 'Telangana' and unwanted commas before importing data into MonogoDb

## Changes made in OpenStreetMap
I have also made following changes in the OpenStreetMap

I have edited the 'mahesh' tag and renamed it to 'name'. You find the same, in the following changeset of osm.
https://www.openstreetmap.org/changeset/47372134

I have also made following change to previuosly found street name issue, from 'Panjagutta Flyover' to 'Nagarjuna Circle Road'
https://www.openstreetmap.org/changeset/47372250

My username on osm is 'potter13'
