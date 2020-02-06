# Market-Basket-Model

* Download the dataset Online Retail and put it in the same directory as the iPython Notebooks.
* Market_Basket_Model notebook contains two phases : 
1- Explore the data 
2- Study customers purchases (Product association rules - Apriori Algorithm)

Here is a link that may help you understand how Apriori algorithm works 
EDA notebook which is an exploration of the data : https://intellipaat.com/blog/data-science-apriori-algorithm/

# Theory of Apriori Algorithm.
The Apriori algorithm was proposed by Agrawal and Srikant in 1994.
There are three major components of the Apriori algorithm:
1) Support
2) Confidence
3) Lift

We will explain this concept with the help of an example.
suppose we have a record of 1000 customers transactions and we want to find out support, confidence and lift for milk and diapers. out of 1000 transactions, 120 contains a milk and 150 contains a diaper. out of this 150 transaction where a diaper is purchased 30 contains transaction contains milk as well. we will use this data to calculate support, confidence and lift.

-Support

support refers to the popularity of item and can be calculated by finding the number of transactions containing a particular item divided by the total number of transactions.

Support(diaper) = (Transactions containing (diaper))/(Total Transactions)
Support(diaper) = 150 / 1000 = 15 %

-Confidence

Confidence refers to the likelihood that an item B is also bought if item A is bought. It can be calculated by finding the number of transactions where A and B are bought together, divided by the total number of transactions where A is bought. Mathematically, it can be represented as:

Confidence(A → B) = (Transactions containing both (A and B))/(Transactions containing A)
The confidence of likelihood of purchasing a diaper if a customer purchase milk.
Confidence(milk → diaper) = (Transactions containing both (milk and diaper))/(Transactions containing milk)
Confidence(milk → daiper) =30 / 120 = 25 %
Confidence is similar to Naive Based Algorithm.

-Lift

Lift refers to the increase in the ratio of the sale of B when A is sold.

Lift(A –> B) can be calculated by dividing Confidence(A -> B) divided by Support(B).

Mathematically it can be represented as:

Lift(A→B) = (Confidence (A→B))/(Support (B))

Lift(milk → diaper) = (Confidence (milk → diaper))/(Support (diaper))

Lift(milk → diaper) = 25 / 15 = 1.66

So by Lift theory, there is 1.66 times more chance of buying milk and diaper together then just buying diaper alone.

Association rule by Lift

lift = 1 → There is no association between A and B.

lift < 1→ A and B are unlikely to be bought together.

lift > 1 → greater the lift greater is the likelihood of buying both products together.
