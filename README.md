# Team Food - MACS 30122

Team members: Emily Yeh, Hazel Chui, Yulun Han, Koichi Onogi

In-class presentation: https://docs.google.com/presentation/d/1mI6GgZG-vjXqf2UrMEpWxTTPQ_Nl1d8xGuuh-qNk-VM/edit?usp=sharing

Project video: https://drive.google.com/file/d/17mV_3KMsa7b-3M0NHZE-Ehe6no6BVamu/view?usp=sharing

## Python Libraries

* requests 2.27.1
* selenium 4.1.2
* statsmodels 0.12.2
* bokeh 2.4.2
* matplotlib 3.5.1
* seaborn 0.11.2

## Goal of the Project

Authenticity can be referred to a commonly agreed attribution to certain entities as to whether the entity is “genuine” or “real” (Trilling, 2009). Given the rising importance of authenticity in influencing consumers’ decisions and evaluation, we would like to study the relationship between authenticity and consumers’ rating from the restaurant domain. In Chicago, as a cultural fusion of different cultures, restaurants featuring cultural cuisines can be found in different neighborhoods. We would like to investigate how each restaurant's authenticity relates to consumers’ rating of the restaurant on restaurant review websites. Would more authentic restaurants tend to be highly rated? We plan to measure authenticity in two ways. First, we would adopt the authenticity scale developed by Kovacs, Carroll, and Lehman (2014). The scale contains a comprehensive list of keywords and corresponding scores. We would compute a final authenticity score for each restaurant by first summing the authenticity scores of all the words that appear in the reviews and the list and then dividing the sum by the total number of words. Second, we would also analyze socio- geographic locations and the surrounding culture of the restaurant. Creating two dummy variables, 1) whether the cuisine type matches the neighborhood’s culture and 2) whether the restaurant is located in a diversified neighborhood, we plan to study whether authentic restaurants (‘yes’ in both dummy variables) are more likely to have a higher rating. We would like to see whether the tendencies are recognized on different websites. Targeting restaurants in different neighborhoods of Chicago, we are selecting restaurants with more than 10 reviews in TripAdvisor and with more than 1 review in Zomato. 

## How to run the software
  First, use functions in TripAdvisor_Crawler.ipynb and Zomato_crawler_final.ipynb to crawl each restaurant and reviews from websites for targeted neighborhoods.
  
  Second, utilize check_scores & combine_dataset.ipynb and zomato cleaning.ipynb to combine each dataset for restaurants and reviews and calculate authenticity scores.
  
  Third, conduct several analyses in final_analysis.ipynb to examine relationships between each feature.
  
  Finally, visualize data features through Data_Visualization.ipynb.
## Contents
1. TripAdvisor_Crawler.ipynb (prepared by Emily)
  - Given URL for the resytaurant searching result of a specific neighborhood, crawl over each page and obtain the urls for restaurants more than 10 reviews.
  - For each restaurant url from the previous function, fetch restaurants information including price range, cuisine categories, ratings, etc.
  - For each restaurant url from the previous function, fetch all reviews of the resaurant, inculding title, contents, and ratings. 

2. Zomato_crawler_final.ipynb (prepared by Yulun and Hazel)
  - Same functions from TripAdvisor_Crawler.ipynb but customized for Zomato

3. check_scores & combine_dataset.ipynb (prepared by Koichi and Emily)
  - Calculate authenticity scores from reviews dateset, utilizing authenticity score table (table detail is in a reference paper "Authenticity and Consumer Value Ratings- Empirical Tests from the Restaurant Domain") and add new column at the restaurant dataset
  - Calculate cultural scores, which takes words from reviews and get ratio of words representing certain nationality (e.g., Chinese, Italian, etc) and add new column at the restaurant dataset
  - Combine all dataset for restaurants
  - Clean up the dataset such as deleting duplicates

4. zomato cleaning.ipynb (prepared by Hazel)
  - Use the same cleaning approach as check_scores & combine_dataset.ipynb to combine and clean up all datasets for restaurants scraped from Zomato

5. final_analysis.ipynb (prepared by Hazel)
  - Conduct linear regression analyses on data scraped from TripAdvisor and Zomato, respectively, and on combined data 
      - DV: Average rating
      - DV: Food rating
      - DV: Authenticity score
  - A textual interpretation of the results are included

6. Data_Visualization.ipynb (prepared by Yulun)
  - Visualize the linear regression analysis results of TripAdvisor and Zomato based on authenticity scores, cultural scores, and ratings of each restaurant

