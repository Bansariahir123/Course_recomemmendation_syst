# Course_recomemmendation_system
Course Recommendation System Report
Introduction
The provided code implements a course recommendation system using a dataset ('coursea_data.csv') containing information about online courses. The system employs natural language processing and machine learning techniques to recommend courses based on user-specified keywords. Additionally, the system combines course ratings and enrollment information to enhance the relevance of recommendations.

Code Explanation
1. Data Loading and Preprocessing
The code begins by loading the dataset into a Pandas DataFrame and performs some preprocessing steps:

The 'course_students_enrolled' column is converted to numeric format, handling values with 'k' (thousands) and 'm' (millions).
2. Feature Extraction
A TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer is employed to convert textual information (course title, organization, and difficulty) into numerical features. This step is crucial for calculating the cosine similarity between courses.

3. Cosine Similarity Calculation
The cosine similarity matrix is computed using the TF-IDF matrix, representing the similarity between courses based on their textual features.

4. Combined Score Calculation
A new feature, 'combined_score,' is created by multiplying the course rating with the number of students enrolled. This combined score aims to emphasize popular and highly-rated courses.

5. Course Recommendation Function
The 'get_recommendations' function takes a keyword as input, searches for courses containing the keyword in their titles, and recommends the top three courses based on the combined score.

6. Visualizations
Two visualizations are provided:

Distribution of Course Ratings: A histogram depicting the distribution of course ratings.
Distribution of Enrolled Students: A histogram illustrating the distribution of the number of students enrolled in courses.
7. Mean Squared Error (MSE) Calculation
MSE is calculated for both course ratings and the number of enrolled students to evaluate the accuracy of the combined score in predicting these metrics.

8. Top Recommended Courses Visualization
A bar chart is generated to visually represent the top recommended courses related to a specified keyword.

9. Scatter Plot of Rating vs Enrolled Students
A scatter plot is created to explore the relationship between course ratings, the number of enrolled students, and course difficulty. The size of the points represents the combined score, offering insights into popular and well-rated courses.

Conclusion
The course recommendation system provides a versatile and informative tool for users seeking relevant courses based on specific keywords. The combination of TF-IDF vectorization, cosine similarity, and the introduction of a combined score enhances the accuracy and relevance of course recommendations. The visualizations aid in understanding the distribution of ratings, enrollment, and the top recommended courses. Additionally, MSE analysis provides insights into the predictive performance of the combined score.






