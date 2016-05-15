# Opiniothon 2016

## Unified Customer Relationship Management Platform

Instead of spamming customers with promo emails, it makes better sense to present the promos to the customers who are actively searching for it. More so if the customer is in the vicinity of your particular stores. 

Our service will combine and present promotions to customers when they are actively looking for them, so the chance of conversion is significantly higher. So we collate all promotional activity of various businesses and present them to the customer in appropriate categories.

Reward customers with points for every purchase and score them regarding purchases from a brand. As the relationship grows, consumers will be eligible for more goodies.

With the power of GPS enabled smartphones, we can inform customers about offers which are specifically relevant to them and record the transaction if there is a successful conversion. 


### APIs
1. Businesses can submit promo details to our API
2. Client apps can get promo coupons based on proximity
3. Successful usage of coupon is recorded and sent back to server for serving analytics

### Assumptions
1. Locations of stores randomly placed in a square area within Bangalore.
2. Location of user is randomly moved around by use of a button
3. Coupon information for fictitious companies with random discount values.

### Database Tables
```
USER:
	id, username, email, birthdate

COUPONS:
	id, merchant, coupon_name, coupon_code, value, expiry

TX:
	id, user_id, coupon_id, store_id, timestamp,

"store":
	"id":12345, "merchant":"", "coupons":{1,2,5}, "lat":"", "long":"", "cluster":""

"coupons":
	"id":1, "merchant":"", "desc":"", "value":"", "expiry_date":""

"merchant":
	"stores":{12345,12346,12347}
```
