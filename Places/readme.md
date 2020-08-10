# EDC Places Search

## Setup

You must have an active Google Places API Key and linked Billing Account. 

(Instructions here)

There are two different types of searches that you can do with different billing implications:

### Free 
  
You can get details for a single search result, the closest result to your location.
  
### Paid

You can search for a particular place near your current location. Useful for finding a dinner spot, for example. These requests cost about 1 cent each.
  
## Searching for a place:

#### (Free Tier)

send

`/places/get/place="Chipotle"`

will return

`/places/out/get/place/name="Chipotle Mexican Grill"`

`/places/out/get/place/address="736 Thompson Lane, Nashville"`

`/places/out/get/place/type="restaurant - food"`


#### (Paid Tier)

send

`/places/search/place="Chipotle"`

will return

`/places/out/search/place/1/name="Chipotle Mexican Grill"`

`/places/out/search/place/1/address="736 Thompson Lane, Nashville"`

`/places/out/search/place/1/type="food"`

`/places/out/search/place/1/open="Open"` (or Closed)

`/places/out/search/place/1/pricelevel="$"` ($, $$, $$$ price levels)

`/places/out/search/place/1/rating=4.5`

Substitute the integer in  `/place/1/` on your magic sheet to display up to 5 search results. 


## Other Searches

You can search for just about anything.

`/places/search/place="Mexican"` - 5 closest Mexican Restaurants 

`/places/search/place="Grocery"` - 5 closest Grocery Stores
