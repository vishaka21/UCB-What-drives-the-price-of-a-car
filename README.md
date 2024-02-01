# What drives the price of a car?

#### Problem Statement

The correct pricing model for vehicles is absolutely essential for used auto dealers, both in terms of the inventory they want to sell, as well as the inventory they want to acquire from consumer trade-ins, as well as auction purchases. 

The margins in this industry are incredibly thin, so overpaying to bring in inventory can cripple these cash-starved business.

Likewise, correct pricing of vehicles for sale is essential, because underpricing will further cut into the already thin margins, and overpricing will lead to a loss of business, especially due to the growth digital vehicle marketplaces and the digital availabilty of dealerships that both allow consumers to find the cheapest vehicles available.

Our goal is to design a model that can reliably predict the price of a vehicle so that we can use it to make our own pricing decisions.

#### Approach

We applied an industry standard approach to this problem, called CRISP-DM. Without being too technical, the general steps are:
 - Understand the problem
 - Understand the data
 - Prepare the data
 - Model the data
 - Evaluate findings
 - Deploy (share findings with stakeholders)
 
The data we acquired needed significant preparation to be useful for our purposes.
We had many incomplete vehicle records (missing important values like odometer and title status), there were duplicates in the data, and some of the attributes contained junk values--odometers with 10 million miles, vehicle prices in the hundreds of thousands, etc.

Removing this "bad" data was straightforward, but unfortunately we needed to dispense with some attributes that might have some bearing on the price of the car, like model and manufacturer. Nonetheless, we feel that this is a generalizable model that can be used for a given dealership, regardless of region or brand. 

#### Results
We were able to produce a satisfactory model, with the one qualification that the model has a tendency to understate the true price for used cars over $25,000. For this reason, we recommend that this model be used with caution for higher priced vehicles, and instead more time should be allocated for follow-up.

We evaluated several models, selected the best one, and optimized it.

In terms of individual features, more expensive vehicles tend to have the following traits:
 - Larger
 - Utility nature such as pickup, truck, or offroad
 - Lower mileage (every mile reduces the price by ~ .05 dollars, on average)
 - Better condition
 - More powerful engine (although 8 cylinder engines have a higher price than 12 cylinder engines)
 - Manual transmission (although this could be due to the specialty nature of these vehicles, as automatic is now standard)
 - Title is secure
 
 From a relative perspective, rear-wheel drive and hybrid gas systems produce a higher price compared to their counterparts.

 #### Recommendation(s)

We advise dealers to follow current trends and acquire and sell larger vehicles with hauling or offroad capabilites. A medium large engine, good condition, and low mileage will also contribute to a higher price.

We also advise dealers to stay away from salvage and parts vehicles, and only stick to vehicles that have a title status of "lien".

#### Next steps
It would benefit branded dealers to know if these trends hold true by manufacturer. Perhaps more powerful engine has a greater impact for Fords than it does for Hondas. We can create custom models for dealers who exclusively sell certain brands to further tailor their pricing.

Additionally, there is scope to improve the predictive ability for this model for higher priced vehicles. This would take time and would require more model testing and evaluation, but would help for dealers who sell higher-end vehicles.