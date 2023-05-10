# Airbnb First Booking Prediction

## This project aims to predict which country a new user's first booking destination will be.

<img src="https://anitabemcriada.com/wp-content/uploads/2020/08/airbnbmgn4.jpg"/>

#### This project was made by Allan Casado

# 1. Business Problem

*Disclaimer: The dataset was collected from Kaggle's competition [Airbnb First Booking Prediction](https://www.kaggle.com/competitions/airbnb-recruiting-new-user-bookings/overview).*

### Goal

Airbnb is a community online service for people to advertise, discover and book passengers and accommodation. It's present all over the world, in almost all countries.

In this project, we are given a list of users along with their demographics, web session records, and some summary statistics. We have to predict which country a new user's first booking destination will be. It's important to note that all the users in this dataset are from USA. There are 12 possible outcomes of the destination country: 'US', 'FR', 'CA', 'GB', 'ES', 'IT', 'PT', 'NL','DE', 'AU', 'NDF' (no destination found), and 'other'. Note that 'NDF' is different from 'other' because 'other' means there was a booking, but is to a country not included in the list, while 'NDF' means there wasn't a booking.

### Why this is useful for the business?

Airbnb business model is a marketplace, where they connect people searching for accomodation with people offering this. In this business model we have:
* Offer
* Demand

And we have some metrics associated with these aspects.

* Offer:
	- Portfolio Size 
	- Portfolio Diversity and Density
	- Average Price
* Demand:
	- Number of users
	- LTV (Life Time Value)
	- CAC (Client Aquisition Cost)

Given that context, we can conclude some things:
1. If we have the capability of predicting the demand, we can also improve the offer. For example, if in our predictions we see that most of the users are prone to go to Italy and if we see that in Italy the offer isn't so good, we can promove campaings there to promote better offers for users.
2. Forecasting the demand, we can reduce the CAC because we don't spend so many money with useless marketing campaings, we can be more assertive in our recommendations. And it also prevents Airbnb from spending money with users that are only curious.


# 2.0 Business Assumptions
