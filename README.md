# Masket Bakset Analysis
Market Basket Analysis using Association Rule Mining (Apriori Algorithm) to determine goods that are frequently bought together.

The data set used is publicly available on [Kaggle](https://www.kaggle.com/sivaram1987/association-rule-learningapriori/version/1).

## Association Rules
* If-then statements that helps us to show the probability of relationships between data items withn large data sets
* Eg
    * *Movie Recommendation*: If they watched this, then they also watched this.
    * *Market Basket Optimisation* : If they bought this, then they also bought this
* Has two parts:
    1. An antecedent (if) - An item found within the data
    1. A consequent (then) - An item found in combination with the data
* An association rule for items $M_1$ (antecedent) and $M_2$ (consequent) can then be expressed as:

$ M_1 \rightarrow M_2$  i.e. representation of having item $M_2$ on the itemset which has $M_1$ on it

*  **Note that implication here is co-occurrence and not causality**
* There are three metrics that help us understand the strength of the relationship (rule):
    1. **Support** -indicates how frequently the itemset occurs
         
       * Support($ M_1 \rightarrow M_2$  ) = $\frac{\text{# transaction containing $M_1$ and $M_2$}}{\text{# transaction}}$

    2. **Confidence** - the number of times the rule is found to be true (i.e. likelines of occurrence of consequent given the the antecedent has occurred)

     * Confidence($ M_1 \rightarrow M_2$  ) = $\frac{\text{# transaction containing $M_1$ and $M_2$}}{\text{# transaction containing $M_1$ }}$
 
    3. **Lift** - How many times the rule is expected to be found true
        * Ratio of confidence to the baseline probability of occurrence of the consequent
        * Think of it as the *lift* that $M_1$ provides to our confdence for having $M_2$ on the itemset
        *  IOW: lift is the rise in probability of having $M_2$ on the cart with the knowledge of $M_1$ being present over the probability of having $M_2$ on the cart without any knowledge about presence of $M_1$
     * Lift($ M_1 \rightarrow M_2$  ) =$\frac{\text{confidence}(M_1 \rightarrow M_2)}{\text{support}(M_2)}$ = $\frac{\frac{\text{# user transactions containing $M_1$ and $M_2$}}{\text{# user transactions containing $M_1$}}}{\text{# user transactions containing $M_2$}}$
     * In cases where $M_1$ actually leads to $M_2$, value of lift will be greater than 1
     * Generally:
         * A value of lift greater than 1 vouches for high association i.e. having $M_1$ on the itemset increases the chances of having $M_2$ on the itemset
         * If the value is positive, there is a positive correlation
         * If the value is negative, there is a negative correlation
         * If the value is 1, there is no correlation
 * The general worflow is:
     1. Generate an itemset from a list all items
     1. Generate a rule for each item set
         

## Reference         
 https://towardsdatascience.com/association-rules-2-aa9a77241654
 
 https://searchbusinessanalytics.techtarget.com/definition/association-rules-in-data-mining
 
 https://datascienceplus.com/visualize-market-basket-analysis-in-r/
 
 https://www.datacamp.com/community/tutorials/market-basket-analysis-r
