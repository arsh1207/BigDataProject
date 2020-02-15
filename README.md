# BigDataProject
Towards the completion for the course Big Data

Big Data Analytics, the science of managing huge data repositories and extract useful knowledge from, has emerged as a young and interdisciplinary field in computer science. Storing huge amounts of data in data repositories amounts to nothing if we are not able to retrieve any useful information from them. In this project we have planned to create a recommender system for Amazon product recommendation system according to customers ratings. This project will emphasize the association rule for the products. After proper analysis and preprocessing of the dataset we will implement two algorithms of the recommender system that was discussed in the class. Later, we will analyse the difference between the two approaches and different results that are obtained.

# Introduction:
2.1 Problem Statement: 
Using amazon product dataset, we will create a recommender system based on two famous algorithms of content based and collaborative filtering recommendation systems. These algorithms we will create from scratch and will include other variations for the system. This will help us in a better analysis of the results. Also, we will analyse our model against pyspark als model for better analysis.
2.2  Motivation:
Recommendation systems help users find and select items (e.g., books, movies, restaurants) from the huge number available on the web or in other electronic information sources. Given a large set of items and a description of the user's needs, they present to the user a small set of the items that are well suited to the description. Recent work in recommendation systems includes intelligent aides for filtering and choosing web sites, news, stories, TV listings, and other information. The users of such systems often have diverse, conflicting needs. Differences in personal preferences, social and educational backgrounds, and private or professional interests are pervasive. As a result, we wanted to have personalized  intelligent systems that process, filter, and display available information in a manner that suits each individual using them. The need for personalization has led to the development of systems that adapt themselves by changing their behavior based on the inferred characteristics of the user interacting with them. Moreover, knowing the details of the different algorithms and how it works is another interesting goal that we want to master.


2.3  Objectives:
1. Applying machine learning using Collaborative Filtering and content based filtering
2.  Parsing data retrieved from a database and predicting user preference.
3. Evaluating different approaches of recommender systems.


# Materials and Methods 
3.1 Dataset description
For this project, we are using the Kaggle Dataset for Amazon products ratings [1] which is available for public use. The database contains 1048575 instances with 4 attributes. Using the aforementioned attributes and having no missing data, we will create a recommender system for different users.
Attribute Information:
UserID: Unique ID for each user
ProductID: Unique ID for each product
Rating: A value between 1 - 5
Timestamp: 1, 2, 3, more

3.2 Algorithms:
3.2.1 Content based Recommender System
The main idea revolves around recommending the user with similar products as was rated highly by him/her in the past. The word “content” here refers to the attributes of the product that a user has liked or disliked. So, basically it will be creating a user profile and a product profile. And based on the ratings provided by that user to that product it will recommend a similar product to the user.


WHY CONTENT-BASED FILTERING?
Collaborative filtering may be the state of the art when it comes to machine learning and recommender systems, but content-based filtering still has a number of advantages, especially in certain circumstances.
Results tend to be highly relevant. Because content-based recommendations rely on characteristics of objects themselves, they are likely to be highly relevant to a user’s interests. This makes them especially valuable for organizations with massive libraries of a single type of content.
Recommendations are transparent. Another advantage is that the process by which any recommendation is generated can be made transparent, which may increase users’ trust in their recommendations or allow them to tweak them. With collaborative-filtering, the process is more of a black box–the algorithm and users alike may not really understand why they’re seeing the recommendations they are.
Users can get started more quickly. Content-based filtering avoids the cold-start problem that often bedevils collaborative-filtering techniques. While the system still needs some initial inputs from users to start making recommendations, the quality of those early recommendations is likely to be much higher than with a system that only becomes robust after millions of data points have been added and correlated.
New items can be recommended immediately. Related to the cold-start problem, another issue with collaborative-filtering is that new objects added to the library will have few (if any) interactions, which means they won’t be recommended very often. Unlike collaborative-filtering systems, content-based recommenders don’t require other users to interact with an object before it starts recommending it.
It’s technically easier to implement. Compared to the sophisticated math involved in building a collaborative-filtering system, the data science behind a content-based system is relatively straightforward. The real work, as we’ve seen is in assigning the attributes in the first place.

3.2.2 Collaborative Filtering Recommender System
In this approach, the algorithm will try to recommend the product to the user by using the history of all the users who have a similar type of ratings for similar products. This method tends to take note of the hidden features of the product. So, here the similar users given ratings to the products will have higher recommendation than other products.

Why to use Collaborative Filtering:
Collaborative filtering works around the interactions that users have with items. These interactions can help find patterns that the data about the items or users itself can’t. Here are some points that can help you decide if collaborative filtering can be used:
·Collaborative filtering doesn’t require features about the items or users to be known. It is suited for a set of different types of items, for example, a supermarket’s inventory where items of various categories can be added. In a set of similar items such as that of a bookstore, though, known features like writers and genres can be useful and might benefit from content-based or hybrid approaches.
 
·Collaborative filtering can help recommenders to not overspecialize in a user’s profile and recommend items that are completely different from what they have seen before. If you want your recommender to not suggest a pair of sneakers to someone who just bought another similar pair of sneakers, then try to add collaborative filtering to your recommender spell.
