# Market Basket Analysis using R
Market Basket Analysis using Association Rule Mining (Apriori Algorithm) to determine goods that are frequently bought together.

The data set used is publicly available on [Kaggle](https://www.kaggle.com/sivaram1987/association-rule-learningapriori/version/1).

[(See the Report)](https://antonyrono.github.io/market_basket_analysis/Market-Basket-Optimisation.html)

## Association Rules
* If-then statements that helps us to show the probability of relationships between data items withn large data sets
* Eg
    * *Movie Recommendation*: If they watched this, then they also watched this.
    * *Market Basket Optimisation* : If they bought this, then they also bought this
* Has two parts:
    1. An antecedent (if) - An item found within the data
    1. A consequent (then) - An item found in combination with the data

*  **Note that implication here is co-occurrence and not causality**
* There are three metrics that help us understand the strength of the relationship (rule):
    1. **Support** -indicates how frequently the itemset occurs

    2. **Confidence** - the number of times the rule is found to be true (i.e. likelines of occurrence of consequent given the the antecedent has occurred)
 
    3. **Lift** - How many times the rule is expected to be found true
        * Ratio of confidence to the baseline probability of occurrence of the consequent
        * Generally:
          * A value of lift greater than 1 vouches for high association i.e. having $M_1$ on the itemset increases the chances of having $M_2$ on the itemset
          * If the value is positive, there is a positive correlation
          * If the value is negative, there is a negative correlation
          * If the value is 1, there is no correlation

## Reference         
 https://towardsdatascience.com/association-rules-2-aa9a77241654
 
 https://searchbusinessanalytics.techtarget.com/definition/association-rules-in-data-mining
 
 https://datascienceplus.com/visualize-market-basket-analysis-in-r/
 
 https://www.datacamp.com/community/tutorials/market-basket-analysis-r
