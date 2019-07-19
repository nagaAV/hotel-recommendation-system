# hotel-recommendation-system
Problem statement:
             In the hotel industry, data analytics can be used in multiple ways in order to improve reputation, marketing strategies, tailor-made product/service offerings, efficiency of operations, occupancy rates and finally, profitability. Analytics can enable a good understanding of customers’ perception of product value and brand positioning of hotel and thus helps in accurately aligning product prices, placement and availability with each customer segment in an insightful way. Hotel management can predict which local tours to recommend that fit a guest’s preference based on his past behaviour as well.  The restaurant department to predict which menu items are likely to be ordered, based for example on the local weather and the reservation department to predict the optimal rate for a room. And also the sales and marketing team to create and send tailored messages across different networks.  Analytics can also help hoteliers cut down their energy costs without sacrificing guest comforts and be efficient in managing operations. Also through customer analytics, optimizing pricing can be achieved through prediction of demand based on a deep understanding of the individual customer’s willingness to pay,  seasonal trends of hotel occupancy, etc. Recently efforts are being made to link predictive analytics with geo-location data to deliver effective location specific recommendations on-property and in real time through mobile apps.
Dataset description:
                  The dataset consists of user hotel rating.csv file in them columns given are userid, hotelid and Overall rating.
Approach:
                The given dataset file contain hotels overall ratings which are given by userid. We need to develop a hotel recommendation to new userid in the given dataset. For this we used a Surprise library package api to build a recommender system for each user.

Firstly, we need to explore the data with EDA analysis. Then, load the dataset for Surprise library. With Surprise library, we will benchmark the following algorithms:
Basic Algorithms are as follows:

BaselineOnly():
BaselineOnly algorithm predicts the baseline estimate for given user and item.

K-NN Algorithms:
 
KNNBasic():
 KNNBasic is a basic collaborative filtering algorithm.
 
KNNBaseline():
 KNNBaseline is a basic collaborative filtering algorithm taking into account a baseline rating.
 
KNNWithMeans():
  KNNWithMeans is basic collaborative filtering algorithm, taking into account the mean ratings of each user.

We use best rmse from above models, KNNBaseline Algorithm gives best rmse and then we train and predict with KNNBaseline and use ALS(Alternating Least Square). We got rmse of 0.8361 and accuracy of 84%.
To inspect the predictions in details, we build a pandas data frame with all the predictions. We get a best predictions and worst predictions for each hotelid  ratings. Then, we define Recommender System based on predictions, so that each user gets a n number of unique recommended hotels.

From the above Recommendation we observed that for each userid gets n number of recommendation to choose from recommended hotelids. Thus, Surprise Library has done a good recommendation to this dataset to get Hotels Recommendations for each User.
