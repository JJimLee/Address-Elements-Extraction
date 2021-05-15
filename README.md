# Address-Elements-Extraction
Shopee Code League
## Background
At Shopee, we strive to ensure our customers' highest satisfaction for their shopping and delivery experience - fast and accurate delivery of goods. This can be better achieved if we have key address elements for each user address which allows us to accurately geocode it to obtain geographic coordinates to ship the parcel to our customers. These key address elements include Point of Interest (POI) Names and Street Names. However, most addresses that Shopee receives are unstructured and in free text format, not following a certain pattern. Thus it is important for us to develop a model to precisely extract the key address elements from it.

## Task
In this competition, you’ll work on addresses collected by us to build a model to correctly extract Point of Interest (POI) Names and Street Names from unformatted Indonesia addresses.

Participants are expected to build their own model for this competition, submissions by teams which directly call any third party APIs on the test set will not be taken into consideration.

## Submission Format
Extract the Point of Interest (POI) Names and Street Names, submission file format should be ‘csv’ file only.

For each ‘id’ in the test dataset, you need to provide two prediction results, one for POI and one for street. POI and street should be separated with a “/” character without any spaces in between. There are cases where POI/street elements in the raw_address are not complete, for this case, you also need to predict the complete subwords before returning the result.

### Examples - assume that:

The POI is “bengkel mandiri motor” and street name is “raya bosnik” the returned POI/street should be:
bengkel mandiri motor/raya bosnik
The POI is “primkob pabri” and no street name is found the returned POI/street should be:
primkob pabri/
No POI is found and the street name is “jalan mh thamrin” the returned POI/street should be:
/jalan mh thamrin
The word “pembangunan” in raw_address “smk karya pemban, pon” is not complete. The correct POI will be “smk karya pembangunan” and the returned result should be:
smk karya pembangunan/pon
If there is no result for a certain address element, please leave it as empty. The returned result should also be lowercase. The ‘csv’ file should contain a header and have the following format:

id	POI/street
0	/
1	pt tunas artha gardatama/lenteng agung barat
2	/lenteng agung barat
3	muh sigit wahyu p dr sp kj/jalan adi sucipto
4	senam melinda/

Your submission should have 50,000 rows, each with 2 columns.
