# Verve-Group-Case-Study


## Problem 1 : estimate the expected win rate for a bid repsonse at a given price

Assumptions :
1) Any external features which might impact the bidding price in real bidding process are out of scope
2) Entity 'Verve' can only choose the bidding price form given list of 'bid_price' provided in sample data

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
  
  Exception to above instances, Expected win rate increase with increase in bid_price
  

## Problem 2 : Maximize net revenue

Assumptions :
1) Maximizing & calculating the revenue considering total events as same of Historical data

- Our advertizer pays 0.50 per win. Hence, it becomes the threshold value for bid_price. Below are data points of our interest.

![image](https://user-images.githubusercontent.com/44555748/192392615-264d961d-7897-49f0-8dbb-6bc5750ff423.png)

- Revenue Generated for each bid_price = (Estimated win rate for each bid_price * total_events * 0.5) - (Estimated win rate for each bid_price * total_events * bid_price)

- Below line chart depicts the revenue generated for each selected bid_price

![image](https://user-images.githubusercontent.com/44555748/192393408-e7326b47-998c-4f8a-bfa5-890a25393664.png)

Hence, Maximum revenue generated with bid_rate = 0.1
