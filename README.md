# Churn or not - Churn Analytics
The [dataset](https://www.mavenanalytics.io/data-playground) of this project was analyzed exclusively with Microsoft Excel. However, the summary report was designed with Figma. 

___

# Table of Content

<!-- vscode-markdown-toc -->

* [Introduction](#Introduction)
* [The Problem](#TheProblem)
* [Methodology](#Methodology)
* [$3,000,000 is gone](#$3,000,000isgone)
* [They are searching for the best](#Theyaresearchingforthebest)
* [The more they subscribe monthly, the less they have to lose](#Themoretheysubscribemonthly,thelesstheyhavetolose)
* [Offer E is what we did to them](#OfferEiswhatwedidtothem)
* [Most of them are leaving before they pay more than $500](#Mostofthemareleavingbeforetheypaymorethan$500)
* [What should be done?](#Whatshouldbedone?)
* [Delay can make the company lose 547 more customers](#Delaycanmakethecompanylose547morecustomers)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->

##  <a name='Introduction'></a>Introduction

On July 9, exactly 8:29am, the Chief Marketing Officer (CMO) of a Telecoms Company and I had this conversation. 

CMO: Omo Nancy, I'm in trouble oh. 

Me: Why, what happened?

CMO: CEO says he's losing money and customers are cancelling their subscriptions. 

Me: Ah! Wahala oh. But why? You and your team are not doing your jobs well?

CMO: We are oh. We work our asses off. I seriously need your help. 

Me: Ok. What can I do?

CMO: I feel like my team and I relax when we acquire customers. We don't really know those that are likely to churn. I need you to help me figure out these people so we can pay more attention to them. 

Me: Oh. That's not a problem. Do you have the records of all these customers?

CMO: Yes, of course. I'll send it to your mail. Please help me. My job is at stake.

Me: Alright, I'll do what I can. 

CMO: Thank you. I owe you one. 

##  <a name='TheProblem'></a>The Problem

A Telecoms Company is experiencing high churn rate and wants to know what attributes that are highly associated with the customers that stop subscribing to their service. 

##  <a name='Methodology'></a>Methodology

The dataset contained 7043 rows and 38 columns. It was void of duplicate values. However, it contained null values. These null values were due to the non-association of the variables to the kind of service (Phone or Internet service) that the customers subscribed to.

For example, if the customer subscribed to Phone service only, the variable “Streaming TV” will have a null value for this customer. This is because it’s only those that have internet service that stream TV.

I needed to handle these null values so that they won’t affect my analysis. So for every null value like this, I inputted the word “None”. This helped me to easily distinguish them.

Visualizing the whole 38 columns to my audience would cause information overload so I needed to remove some columns but I didn't want to do this carelessly to avoid loss of important information. 

To filter the column variables that were relevant to determining the likelihood that a customer will churn, **Entropy and Information gain** were used. 

Entropy formula: 
![](Formulas/Entropy%20formula.png)

Information gain formula: 

![](Formulas/Information%20Gain%20formula.png)

The variables with information gains greater than zero were checked further to see if there were clear and significant distinctions between the two major classes: Stayed and Churned. 

Doing all these narrowed these variables down to five variables that were very important in determining the churn risks.

These variables include: Total revenue, refunds, Contract type, Offer type, and Tenure in Months. 

These variables will be explained in further headings.

##  <a name='Projectflowchart'></a>Project flowchart

The image below summarizes the main steps in this project: 

![](Charts/Churn%20or%20not%20Project%20flowchart.png)

To read a detailed description of the steps I took in my analysis, please click [HERE](https://amandinancy16.medium.com/churn-or-not-churn-analytics-my-thought-process-b0d25523f932). 

##  <a name='$3,000,000isgone'></a>#3,000,000 is gone

It's one thing to start a business and it's another thing to acquire upto 100 customers. The moment 100 customers are gotten, the next milestone to achieve is the retaining of these customers and the customers that will join later. 

The customer records of the Telecoms company from second quarter(Q2) of the year reveals that the company has crossed that milestone of getting 100 customers because currently they have 7043 customers. Or **had** rather. That number reduced to 5174 by the end of this second quarter. This equates to a 26.5% loss in customers. 

The consequence of this loss is great. The company had an approximate revenue of $21,000,000 but these churned customers left with $3,000,000 which is a huge proportion of 17.2% of the total revenue. That's a lot of money! 

![](Charts/Churn%20rate.png)

The question is, why are these people leaving? 

# Customers are trusting competitors better
A quick survey from these customers revealed that 841 of them (about 45% of the total churned customers) left because they found competitors that are offering better services. 

![](Charts/Churn%20Rate%20by%20Reason.png)

These customers are leaving for major reasons of better devices, better offers, higher download, and more data. This is a revelation that most of the customers are using more of the Internet service than the Phone service and the marketers should pay attention to this. 

But come to think of it. If most of these churned customers left because of competitors, it's most likely that these customers came into the Telecoms Company to test the waters but weren't convinced. 

This was confirmed due to the length of time period that they spent in the company. 

##  <a name='Theyaresearchingforthebest'></a>They are searching for the best

The minds of these customers are not yet stable to be transformed to loyal customers. 36% of them are spending 4months or less in the company.  

![](Charts/Churned%20Customer%20Count%20by%20Tenure(in%20Months).png)

They are searching for the best and to them, this Telecoms company is not the best. But why should we even bother? Is this affecting their spendings and behavior? The answer is Yes. 

##  <a name='Themoretheysubscribemonthly,thelesstheyhavetolose'></a>The more they subscribe monthly, the less they have to lose

Just as was said before, they are still on a search and because of this search, they try to put little at stake. What does this mean? 

It means that these customers are subscribing to the less costly month-to-month contract type because of lack of trust. 46% of the customers that subscribed to the month-to-month cobtract type are gone. 

![](Charts/Customer%20Percentage%20by%20Contract%20Type.png)

You might probably have two questions in your mind. First, maybe this 46% isn't large after all because 43% of these customers are still with the company. The difference isn't much so maybe you disagree. Or maybe something is making them to leave. 

We know it's the competitors. But what was done to them to make them find solace in our competitors

Second, how do we know that these customers are spending less? They might actually be subscribing for expensive monthly subscriptions. 

Now, let me answer your first question about what was done to them to make them leave. 

##  <a name='OfferEiswhatwedidtothem'></a>Offer E is what we did to them

53% of all customers that subscribed to offer E left. That's more than the stayed and new Offer E subscribers put together. 

![](Charts/Customer%20Percentage%20by%20Offer.png)

But what might be wrong with Offer E? Going back to the reasons these customers left. They left because of better devices, higher download bandwidth, more data, and better offer. 

Obvioulsy Offer E is not a better offer. It's possible that it lacks these features or even though these features are present in the offer, the value might be low. 

Onto the second question, how do we know they are spending less? 
 
##  <a name='Mostofthemareleavingbeforetheypaymorethan$500'></a>Most of them are leaving before they pay more than $500

A whooping 40% of these customers spent $500 or less before they left. This number is way more than the 13% proportion of those that paid the second least revenue of between $500 and $1000. 

![](Charts/Churned%20Customer%20Count%20by%20Revenue.png)

This number is too great to be looked away. This might be a confirmation that these customers want to pay less for more.

Here's a summary customer profile of customers that are most likely to leave the Telecoms Company. 

![](Summary%20Report/Summary%20Report.png)

Now that we know these customers that are likely to churn, what should be done?

##  <a name='Whatshouldbedone?'></a>What should be done?

We have already seen that most customers that left spent less than $500, stayed for only 4months or less, subscribed to the monthly contract, and/or Offer E. 

The major step to take is to increase the value of Offer E or upsell other offers. Whichever one that is chosen should contain important benefits like high download bandwidth, and more data. This is solely for the business team to decide. 

However, the marketers also have a role to play. The marketers should make these customers spend more time with the company. To achieve this, they can upsell the one-year and two-year contracts to both current and future customers. 

This will automatically make these customers spend both more time and more money. This puts them out of the profile of customers with high churn risks.

Lastly, the business team might not cooperate in increasing the value of Ofer E. The marketers can still play their part by evaluating the other Offers and upselling the offer that has more data and more bandwidth download. 

They could also choose to upsell Offer A since it has the less number of churned customers. 

It's one thing to know the actions that should be taken and it's another thing to know when to start. I would say, start now!

Why should the CMO and his team start now?

##  <a name='Delaycanmakethecompanylose547morecustomers'></a>Delay can make the company lose 547 more customers

If the Chief Marketing Officer and his team delay by one day, they are most likely to lose 1 in every 10 current customers. These current customers include both the retained and new customers that joined this second quarter. 

![](Charts/People%20Graph.png)

The more customers that leave, the more money the business loses. The marketers should pick the records of the customers that have at least one of these four churn risks and start work immediately with the recommended solutions unless they don't love their jobs. 

Click [HERE](https://amandinancy16.medium.com/churn-or-not-churn-analytics-my-thought-process-b0d25523f932) to see details of the steps I took in solving this problem. 




