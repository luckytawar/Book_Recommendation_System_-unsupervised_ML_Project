# Book_Recommendation_System_-unsupervised_ML_Project
Project Name

Book Recommendation System ML Unsupervised Learning

Programming language: Python

Libraries used: Numpy, Pandas, Matplotlib, Seaborn, sklearn.metrics.pairwise.cosine_similarity, scipy.stats.pearsonr, sklearn.neighbors.NearestNeighbors

NoteBook: Google Colab

Dataset Source: Almabetter

Project Summary-
During the last few decades, with the rise of Youtube, Amazon, Netflix, and many other such web services, recommender systems have taken more and more place in our lives. From e-commerce (suggest to buyers articles that could interest them) to online advertisement (suggest to users the right contents, matching their preferences), recommender systems are today unavoidable in our daily online journeys.

In a very general way, recommender systems are algorithms aimed at suggesting relevant items to users (items being movies to watch, text to read, products to buy, or anything else depending on industries). Recommender systems are really critical in some industries as they can generate a huge amount of income when they are efficient or also be a way to stand out significantly from competitors. The main objective of this project is to create a collaborative book recommendation system for users.

Problem Statement-
Developing an effective book recommendation system that provides popular books by ratings and personalized books recommendations to users based on similar users books ratings(collaborative filtering), this should increase book discovery and improve overall user satisfaction in the context of online book store platforms

Business Objective
To leverage the insights gained from both collaborative-based and popularity-based filtering approaches to develop a comprehensive book recommendation system. The primary goal is to enhance user satisfaction and increase book discovery by providing personalized recommendations based on users' preferences and popular trends. This approach aims to optimize user engagement and retention on the online book platform, thereby fostering a thriving community of readers and maximizing the platform's revenue potential through increased book sales and user interactions.

ISBN - International Book Standard Number
Book Title - Contains title of book
Book Author - Contains author of the book
Year of Publication - Contains year the book was published
Publisher - Name of Publisher released the book
Image URL S - small image URL
Image URL M - medium image URL
Image URL L - Large image URL
Users dataset-

User ID - Unique ID to each user logined to website
Location - Location of the user
Age - age of the user
Ratings dataset-

User ID - Unique ID to each user logined to website
ISBN - International Book Standard Number
Book Rating - Users rating for books
Handling missing values-

- books dataframe has 2 missing values in publishers and 1 missing value in author, remove those null values from books dataset

Data Visualization & storytelling
Chart - 1 Top 10 Author's written most number of books
Chart - 2 Top 10 publishers with most books published
Chart - 3 Top 20 Years with highest books published
Chart - 4 Top 10 books with highest count of ratings given by users
Chart - 5 Ratings value counts
Data Preprocessing for recommendation system
step - 1 filtering dataframe by removing books which doesn't have any ratings.

step - 2 based on user based similarities filtering dataframe by grouping users who have rated atleast 50 books for improving data richness and improved quality of recommendation.

step - 3 Dataframe from step 2 is further grouped by books and aggregated by sum of ratings and filtered books having atleast 15+ ratings named table as famous books.

step - 4 From famous books table pivot table has been created, by using pivot table book recommendation system has developed by using cosine similarity model and pearson correlation model.

step - 5 To overcome cold start of book recommendation system for new uers and less active users popularity based recommendation system has been developed.

Evaluation of models
SInce there is no evaluation metric to finalise the algorithm/model

we can conclude based on books recommended by Cosine similarity and Pearson correlation, the recommendations were very close with change in order of recomendations:

Case: 1 - Book name 'Message in a Bottle':

Case: 1 result - 4/5 books are similar recommended books, with change in order of books recommended

Case: 2 - Book name 'The Rescue':

Case: 2 result - 5/5 books are similar recommended books, with change in order of books recommended

Case: 3 - Book name 'Harry Potter and the Chamber of Secrets (Book 2)':

Case: 3 result - 5/5 books are similar recommended books including order of books recommended

Future scope in Book Recommendation System
Predictive Analytics for Book Releases: By leveraging the expanded dataset comprising book genre information, author ratings, and publisher details, the recommendation system can evolve into a predictive analytics tool. This tool could forecast the potential ratings a book might receive upon release. Utilizing machine learning algorithms trained on historical data, the system can predict the anticipated success of upcoming book releases(predicting book rating). This predictive capability empowers publishers and book retailers to make informed decisions regarding inventory stocking, marketing strategies, and sales projections.

Enhanced Personalization and Recommendation Accuracy: Incorporating author and publisher ratings data allows for a deeper understanding of user preferences and tendencies. By analyzing users past interactions with books authored by specific authors or published by certain publishing houses, the recommendation system can offer more personalized and relevant book suggestions. This heightened level of personalization enhances user satisfaction and engagement with the platform, leading to increased user retention and loyalty.

Dynamic Inventory Management: With predictive analytics capabilities, book retailers can optimize their inventory management processes. By anticipating the potential popularity and demand for upcoming book releases, retailers can strategically allocate resources and stock inventory accordingly. This proactive approach minimizes stockouts, reduces excess inventory holding costs, and maximizes sales opportunities. Additionally, retailers can identify niche or trending genres and authors to diversify their product offerings and cater to evolving consumer preferences.

Collaborative Partnerships and Marketing Opportunities: The predictive insights generated by the recommendation system can foster collaborative partnerships between publishers, authors, and retailers. Publishers and authors can leverage the predictive ratings forecasts to refine their marketing strategies, target specific reader demographics, and optimize promotional campaigns. Retailers can collaborate with authors and publishers to launch exclusive pre-order offers, host author events, and create curated book collections aligned with predicted consumer interests.

Conclusion
Collaborative-based filtering approach: recommendation system utilizing cosine similarity and Pearson correlation has been implemented effectively for book recommendation.

Initially, the dataset consists of book with no ratings fill as 0 instead null later dataset was refined by filtering out books with ratings only, ensuring data integrity. Then, by focusing on users who have rated at least 50 books, to enhance richness of the dataset, leading to improved recommendation quality.

Further refinement was achieved by selecting books with a minimum of 15 number of ratings given for each book, resulting in a subset termed "famous books". This step ensured that only books with a significant level of user engagement were considered for recommendation.

A pivot table was constructed from the famous books dataset, organizing ratings by users and books. Subsequently, cosine similarity and Pearson correlation models were generated from this pivot table to measure the similarity between books based on user ratings.

The evaluation of the recommendation system was conducted through three cases, where popular books like "Message in a Bottle", "The Rescue", and "Harry Potter and the Chamber of Secrets (Book 2)" were analyzed. In each case, the system demonstrated strong performance, recommending similar books with a high degree of overlap, albeit with variations in the recommended order.

Overall, the collaborative-based filtering approach, combined with cosine similarity and Pearson correlation, proves to be a reliable method for generating personalized book recommendations, contributing to an enriched user experience.

Popularity-based filtering approach: Therefore the top 50 books are selected based on specific criteria, they have received a substantial number of user ratings (greater than 200), and they are sorted based on their average ratings. This method has yielded a robust recommendation system. The selected books have mean of 283 count of ratings given by users(minimum of 204 count of ratings and a maximum of 707 count of ratings), Average book rating is 7.9 (minimum of 4.39 ratings and a maximum of 9.12 ratings), reflecting a diverse and high-quality collection.

