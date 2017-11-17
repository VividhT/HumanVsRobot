# HumanVsRobot

# Description:
In this Project, we are chasing down robots for an online auction site. Human bidders on the site are becoming increasingly frustrated with their inability to win auctions vs. their software-controlled counterparts. As a result, usage from the site's core customer base is plummeting. In order to rebuild customer happiness, the site owners need to eliminate computer generated bidding from their auctions. Their attempt at building a model to identify these bids using behavioral data, including bid frequency over short periods of time, has proven insufficient.

# Our Motive:
The goal of our Project is to identify online auction bids that are placed by "robots", helping the site owners easily flag these users for removal from their site to prevent unfair auction activity.

# About Data we have:
There are two data sets in this competition. One is a bidder data set that includes a list of bidder information, including their id, payment account, and address. The other is a bid data set that includes 7.6 million bids on different auctions. The bids in this data set are all made by mobile devices. The online auction platform has a fixed increment of dollar amount for each bid, so it doesn't include an amount for each bid.

# File descriptions:
	train.csv - the training set from the bidder dataset
	test.csv - the test set from the bidder dataset
	sampleSubmission.csv - a sample submission file in the correct format
	bids.csv - the bid dataset

# Data fields

# For the bidder dataset:
	bidder_id – Unique identifier of a bidder.
	payment_account – Payment account associated with a bidder. These are obfuscated to protect privacy. 
	address – Mailing address of a bidder. These are obfuscated to protect privacy. 
	outcome – Label of a bidder indicating whether or not it is a robot. Value 1.0 indicates a robot, where value 0.0 indicates human. 
	The outcome was half hand labeled, half stats-based. There are two types of "bots" with different levels of proof:

1. Bidders who are identified as bots/fraudulent with clear proof. Their accounts were banned by the auction site.
2. Bidder who may have just started their business/clicks or their stats exceed from system wide average. There are no clear proof that they are bots. 


# For the bid dataset:
	bid_id - unique id for this bid
	bidder_id – Unique identifier of a bidder (same as the bidder_id used in train.csv and test.csv)
	auction – Unique identifier of an auction
	merchandise –  The category of the auction site campaign, which means the bidder might come to this site by way of searching for  		"home goods" but ended up bidding for "sporting goods" - and that leads to this field being "home goods". This categorical field 			could be a search term, or online advertisement. 
	device – Phone model of a visitor
	time - Time that the bid is made (transformed to protect privacy).
	country - The country that the IP belongs to
	ip – IP address of a bidder (obfuscated to protect privacy).
	url - url where the bidder was referred from (obfuscated to protect privacy). 
