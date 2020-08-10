# EDC Places Search

## Setup

You must have an active Google Places API Key and linked Billing Account. 

(Instructions here)

There are two different types of searches that you can do with different billing implications:

### Free 
  
You can get details for a single search result.
  
### Paid

You can search for a particular place near your current location. Useful for finding a dinner spot, for example. These requests cost about 1 cent each.
  
## Searching for a place:

send

`/places/get/place="Chipotle"`

will return

`/places/out/get/place/name="Chipotle Mexican Grill"`
`/places/out/get/place/address="736 Thompson Lane, Nashville TN 37204, United States"`
`/places/out/get/place/type="restaurant - food"`
