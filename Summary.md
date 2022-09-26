# Verve-Group-Case-Study

## Problem 1 : estimate the expected win rate for a bid repsonse at a given price

Assumptions :
1) Any external features which might impact the bidding price in real bidding process are out of scope
2) Entity 'Verve' can only choose the bidding price form given list of 'bid_price' provided in sample data

Key observations/Findings:
- Expected win rate for a bid response at a given price can be solved by Bayes theorem.
        
        P(Win|Price) = ( P(Price|Win) * P(Price) ) / P(Win)
        
        Where;
        
        P(Price|Win) = (# of winning Events for each bid_price / Total # of events for each bid_price) * Overall winning rate
        
        P(Price) = Probability of selecting a particular bid_price
        
        P(Win) = Overall winning probability
        
-  The target probability P(Win|Price) is incidated in the below picture as 'prob_win_price'

![image](https://user-images.githubusercontent.com/44555748/192387663-96f3dd09-c80b-4a33-80f4-9ee6da8478b0.png)

![image](https://user-images.githubusercontent.com/44555748/192389416-144fb045-745b-4530-ae3d-4acf23cddf3f.png)

- Expected win rate are same E.g. 0.124409 for bid_price in [0.10, 0.40, 0.75]

  Expected win rate are same E.g. 0.082939 for bid_price in [0.20, 0.50]
  

## Problem 2 : Maximize net revenue

- 
