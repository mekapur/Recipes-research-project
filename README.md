# Recipes-research-project
Project for DSC 80 at UCSD

Name: Mehak Kapur

Website Link: https://mekapur.github.io/Recipes-research-project/

## Introduction

A treasure trove of culinary inspiration and information, with over 234,000 recipes at your fingertips, this dataset offers a diverse array of dishes spanning cuisines, flavors, and cooking styles. In this project we are exploring the relationship between the number of calories and the average rating of a dish. 

This data set contains :

Number of rows: 234429 

No of columns: 18 

Columns relevant to question: 

Name - The name of the dish in the recipe 

Nutrition - The nutritional values like calories, total fat, sugar etc 

Ingredients - Ingredients used in making the dish 

Description - Use of words like chocolatey, delicious, sweet etc

## Data Cleaning and Exploratory Data Analysis

Description of data cleaning that took place: 

For the nutrition column I turned the strings into actual columns of the form in the form calories (#), total fat (PDV), sugar (PDV), sodium (PDV), protein (PDV), saturated fat (PDV), and carbohydrates (PDV). I also looked at how many missing values there are in each column and replaced them with NaN.

I also binned the 'average_rating' values into specified intervals defined by the bins list and assigns corresponding labels from the labels list to each interval. This way the average rating is not a categorical column which is consistent with the analysis being performed. 
The first 5 rows of the cleaned dataset:

| name                                 |     id |   minutes |   contributor_id | submitted   | tags                                                                                                                                                                                                                        |   n_steps | steps                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | description                                                                                                                                                                                                                                                                                                                                                                       | ingredients                                                                                                                                                                    |   n_ingredients |          user_id |   recipe_id | date       |   rating | review                                                                                                                                                                                                                                                                                                                                           |   average_rating |   calories |   total_fat |   sugar |   sodium |   protein |   saturated_fat |   carbohydrates |   average_rating_cat |
|:-------------------------------------|-------:|----------:|-----------------:|:------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------:|-----------------:|------------:|:-----------|---------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------:|-----------:|------------:|--------:|---------:|----------:|----------------:|----------------:|---------------------:|
| 1 brownies in the world    best ever | 333281 |        40 |           985201 | 2008-10-27  | ['60-minutes-or-less', 'time-to-make', 'course', 'main-ingredient', 'preparation', 'for-large-groups', 'desserts', 'lunch', 'snacks', 'cookies-and-brownies', 'chocolate', 'bar-cookies', 'brownies', 'number-of-servings'] |        10 | ['heat the oven to 350f and arrange the rack in the middle', 'line an 8-by-8-inch glass baking dish with aluminum foil', 'combine chocolate and butter in a medium saucepan and cook over medium-low heat , stirring frequently , until evenly melted', 'remove from heat and let cool to room temperature', 'combine eggs , sugar , cocoa powder , vanilla extract , espresso , and salt in a large bowl and briefly stir until just evenly incorporated', 'add cooled chocolate and mix until uniform in color', 'add flour and stir until just incorporated', 'transfer batter to the prepared baking dish', 'bake until a tester inserted in the center of the brownies comes out clean , about 25 to 30 minutes', 'remove from the oven and cool completely before cutting']                                                  | these are the most; chocolatey, moist, rich, dense, fudgy, delicious brownies that you'll ever make.....sereiously! there's no doubt that these will be your fav brownies ever for you can add things to them or make them plain.....either way they're pure heaven!                                                                                                              | ['bittersweet chocolate', 'unsalted butter', 'eggs', 'granulated sugar', 'unsweetened cocoa powder', 'vanilla extract', 'brewed espresso', 'kosher salt', 'all-purpose flour'] |               9 | 386585           |      333281 | 2008-11-19 |        4 | These were pretty good, but took forever to bake.  I would send it ended up being almost an hour!  Even then, the brownies stuck to the foil, and were on the overly moist side and not easy to cut.  They did taste quite rich, though!  Made for My 3 Chefs.                                                                                   |                4 |      138.4 |          10 |      50 |        3 |         3 |              19 |               6 |                    4 |
| 1 in canada chocolate chip cookies   | 453467 |        45 |          1848091 | 2011-04-11  | ['60-minutes-or-less', 'time-to-make', 'cuisine', 'preparation', 'north-american', 'for-large-groups', 'canadian', 'british-columbian', 'number-of-servings']                                                               |        12 | ['pre-heat oven the 350 degrees f', 'in a mixing bowl , sift together the flours and baking powder', 'set aside', 'in another mixing bowl , blend together the sugars , margarine , and salt until light and fluffy', 'add the eggs , water , and vanilla to the margarine / sugar mixture and mix together until well combined', 'add in the flour mixture to the wet ingredients and blend until combined', 'scrape down the sides of the bowl and add the chocolate chips', 'mix until combined', 'scrape down the sides to the bowl again', 'using an ice cream scoop , scoop evenly rounded balls of dough and place of cookie sheet about 1 - 2 inches apart to allow for spreading during baking', 'bake for 10 - 15 minutes or until golden brown on the outside and soft & chewy in the center', 'serve hot and enjoy !'] | this is the recipe that we use at my school cafeteria for chocolate chip cookies. they must be the best chocolate chip cookies i have ever had! if you don't have margarine or don't like it, then just use butter (softened) instead.                                                                                                                                            | ['white sugar', 'brown sugar', 'salt', 'margarine', 'eggs', 'vanilla', 'water', 'all-purpose flour', 'whole wheat flour', 'baking soda', 'chocolate chips']                    |              11 | 424680           |      453467 | 2012-01-26 |        5 | Originally I was gonna cut the recipe in half (just the 2 of us here), but then we had a park-wide yard sale, & I made the whole batch & used them as enticements for potential buyers ~ what the hey, a free cookie as delicious as these are, definitely works its magic! Will be making these again, for sure! Thanks for posting the recipe! |                5 |      595.1 |          46 |     211 |       22 |        13 |              51 |              26 |                    5 |
| 412 broccoli casserole               | 306168 |        40 |            50969 | 2008-05-30  | ['60-minutes-or-less', 'time-to-make', 'course', 'main-ingredient', 'preparation', 'side-dishes', 'vegetables', 'easy', 'beginner-cook', 'broccoli']                                                                        |         6 | ['preheat oven to 350 degrees', 'spray a 2 quart baking dish with cooking spray , set aside', 'in a large bowl mix together broccoli , soup , one cup of cheese , garlic powder , pepper , salt , milk , 1 cup of french onions , and soy sauce', 'pour into baking dish , sprinkle remaining cheese over top', 'bake for 25 minutes or until cheese is lightly browned', 'sprinkle with rest of french fried onions and bake until onions are browned and cheese is bubbly , about 10 more minutes']                                                                                                                                                                                                                                                                                                                              | since there are already 411 recipes for broccoli casserole posted to "zaar" ,i decided to call this one  #412 broccoli casserole.i don't think there are any like this one in the database. i based this one on the famous "green bean casserole" from campbell's soup. but i think mine is better since i don't like cream of mushroom soup.submitted to "zaar" on may 28th,2008 | ['frozen broccoli cuts', 'cream of chicken soup', 'sharp cheddar cheese', 'garlic powder', 'ground black pepper', 'salt', 'milk', 'soy sauce', 'french-fried onions']          |               9 |  29782           |      306168 | 2008-12-31 |        5 | This was one of the best broccoli casseroles that I have ever made.  I made my own chicken soup for this recipe. I was a bit worried about the tsp of soy sauce but it gave the casserole the best flavor. YUM!                                                                                                                                  |                5 |      194.8 |          20 |       6 |       32 |        22 |              36 |               3 |                    5 |
|                                      |        |           |                  |             |                                                                                                                                                                                                                             |           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                |                 |                  |             |            |          | The photos you took (shapeweaver) inspired me to make this recipe and it actually does look just like them when it comes out of the oven.                                                                                                                                                                                                        |                  |            |             |         |          |           |                 |                 |                      |
|                                      |        |           |                  |             |                                                                                                                                                                                                                             |           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                                |                 |                  |             |            |          | Thanks so much for sharing your recipe shapeweaver. It was wonderful!  Going into my family's favorite Zaar cookbook :)                                                                                                                                                                                                                          |                  |            |             |         |          |           |                 |                 |                      |
| 412 broccoli casserole               | 306168 |        40 |            50969 | 2008-05-30  | ['60-minutes-or-less', 'time-to-make', 'course', 'main-ingredient', 'preparation', 'side-dishes', 'vegetables', 'easy', 'beginner-cook', 'broccoli']                                                                        |         6 | ['preheat oven to 350 degrees', 'spray a 2 quart baking dish with cooking spray , set aside', 'in a large bowl mix together broccoli , soup , one cup of cheese , garlic powder , pepper , salt , milk , 1 cup of french onions , and soy sauce', 'pour into baking dish , sprinkle remaining cheese over top', 'bake for 25 minutes or until cheese is lightly browned', 'sprinkle with rest of french fried onions and bake until onions are browned and cheese is bubbly , about 10 more minutes']                                                                                                                                                                                                                                                                                                                              | since there are already 411 recipes for broccoli casserole posted to "zaar" ,i decided to call this one  #412 broccoli casserole.i don't think there are any like this one in the database. i based this one on the famous "green bean casserole" from campbell's soup. but i think mine is better since i don't like cream of mushroom soup.submitted to "zaar" on may 28th,2008 | ['frozen broccoli cuts', 'cream of chicken soup', 'sharp cheddar cheese', 'garlic powder', 'ground black pepper', 'salt', 'milk', 'soy sauce', 'french-fried onions']          |               9 |      1.19628e+06 |      306168 | 2009-04-13 |        5 | I made this for my son's first birthday party this weekend. Our guests INHALED it! Everyone kept saying how delicious it was. I was I could have gotten to try it.                                                                                                                                                                               |                5 |      194.8 |          20 |       6 |       32 |        22 |              36 |               3 |                    5 |
| 412 broccoli casserole               | 306168 |        40 |            50969 | 2008-05-30  | ['60-minutes-or-less', 'time-to-make', 'course', 'main-ingredient', 'preparation', 'side-dishes', 'vegetables', 'easy', 'beginner-cook', 'broccoli']                                                                        |         6 | ['preheat oven to 350 degrees', 'spray a 2 quart baking dish with cooking spray , set aside', 'in a large bowl mix together broccoli , soup , one cup of cheese , garlic powder , pepper , salt , milk , 1 cup of french onions , and soy sauce', 'pour into baking dish , sprinkle remaining cheese over top', 'bake for 25 minutes or until cheese is lightly browned', 'sprinkle with rest of french fried onions and bake until onions are browned and cheese is bubbly , about 10 more minutes']                                                                                                                                                                                                                                                                                                                              | since there are already 411 recipes for broccoli casserole posted to "zaar" ,i decided to call this one  #412 broccoli casserole.i don't think there are any like this one in the database. i based this one on the famous "green bean casserole" from campbell's soup. but i think mine is better since i don't like cream of mushroom soup.submitted to "zaar" on may 28th,2008 | ['frozen broccoli cuts', 'cream of chicken soup', 'sharp cheddar cheese', 'garlic powder', 'ground black pepper', 'salt', 'milk', 'soy sauce', 'french-fried onions']          |               9 | 768828           |      306168 | 2013-08-02 |        5 | Loved this.  Be sure to completely thaw the broccoli.  I didn&#039;t and it didn&#039;t get done in time specified.  Just cooked it a little longer though and it was perfect.  Thanks Chef.                                                                                                                                                     |                5 |      194.8 |          20 |       6 |       32 |        22 |              36 |               3 |                    5 |

Univariate Analysis

Distribution of Average Rating Categories

<iframe
  src="assets/plot1.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>

The plot shows that most recipes have an average rating of 5.

Bivariate Analysis

Relationship between calories and average_rating

<iframe
  src="assets/plot2.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>

This plot shows the distribution of calories across different categories of average ratings for recipes.

Interesting Aggregates 

| rating_range | Mean Calories | Median Calories | Max Calories | Min Calories | Calories Std Dev | Recipe Count |
|--------------|---------------|-----------------|--------------|--------------|------------------|--------------|
| 0-1          | 457.46        | 279.3           | 5475.2       | 0.0          | 645.63           | 697          |
| 1-2          | 464.26        | 319.4           | 13101.5      | 8.0          | 796.71           | 789          |
| 2-3          | 448.24        | 311.2           | 17551.6      | 0.0          | 701.32           | 3969         |
| 3-4          | 435.76        | 315.2           | 16894.9      | 0.0          | 591.72           | 23407        |
| 4-5          | 415.40        | 299.0           | 45609.0      | 0.0          | 575.14           | 202790       |


This pivot table summarizes statistics related to calories for recipes categorized into different average rating ranges.
It includes columns such as mean, median, maximum, minimum, standard deviation, and count of calories for each rating range.
For example, for recipes with an average rating between 0 and 1, there are 697 recipes. The mean calorie value for these recipes is approximately 457.46, with a median of 279.3. The maximum calorie count is 5475.2, and the minimum is 0.

## Assessment of Missingness

There are only 4 missing columns - name, description, average_rating, rating

As such, I believe none of the columns are NMAR. I think this is true because there are only 2 columns that aren't MD - name, description.
In these two columns, the missing values cannot be NMAR - there is no reason for someone not to provide the name of their meal, or the description. Therefore, we believe NONE of the columns are NMAR.

<iframe
  src="assets/plot3.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>
Permutation Test for calories vs. Missingness in Average Rating

P-value for calories: 0.0

We conducted a permutation test to examine whether there's a significant difference in the mean calories between recipes with missing and non-missing 'average_rating' values. The observed mean difference in calories was found to be 0.0, and the permutation test yielded a p-value of 0.0. This indicates that the observed difference is statistically significant, suggesting a potential association between the missingness in 'average_rating' and the calories of recipes.

<iframe
  src="assets/plot4.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>
Permutation Test for Minutes vs. Missingness in Average Rating

P-value for dependency of 'average_rating' on 'minutes': 0.542

We also conducted a permutation test to investigate the dependency of 'average_rating' on the 'minutes' column. The observed p-value for this test was 0.542, indicating that we fail to reject the null hypothesis. This suggests that there's no significant relationship between the average rating of recipes and the duration of time required to prepare them.

## Hypothesis Testing

Null Hypothesis:
There is no relationship between the number of calories in a recipe and its average rating.

Alternative Hypothesis:
Greater the number of calories, greater the average rating of the recipe.

Test Statistic:
Total Variation Distance (TVD) was chosen as the test statistic. TVD measures the difference between two probability distributions. In this context, it quantifies the discrepancy between the distribution of average ratings for recipes with low, moderate, and high calorie counts. TVD is suitable for comparing distributions and quantifying the difference between them. It allows us to assess the divergence between the distribution of average ratings for recipes with different calorie levels, providing insights into the relationship between these variables.

Significance Level:
We chose a significance level of α = 0.05, which is a common threshold for hypothesis testing.

Resulting p-value:
After conducting the permutation test with TVD as the test statistic, we obtained a p-value of 0.0.

Conclusion:
With a p-value of 0.0, which is less than the chosen significance level of 0.05, we reject the null hypothesis. This indicates strong evidence against the hypothesis that there is no relationship between calories and average rating. Therefore, we conclude that there is a statistically significant relationship between the number of calories in a recipe and its average rating. Specifically, recipes with higher calorie counts tend to have higher average ratings, supporting our alternative hypothesis.

## Framing a Prediction Problem

Prediction Problem and Type:
The prediction problem in this scenario is to predict the average rating category of recipes based on various features. This is a classification problem as we are categorizing recipes into different rating categories. This would qualify as a multiclass classification beacuse we would be predicting ratings as 'low', 'medium' or 'high'

Response Variable:
The response variable (target variable) is average_rating_cat, which represents the categorized average rating of recipes. This variable was chosen because it provides a clear and meaningful measure of the quality or popularity of a recipe, making it suitable for prediction.

Accuracy: Since we are dealing with a multiclass classification problem and the classes are not heavily imbalanced, accuracy provides a straightforward and intuitive measure of overall model performance. It represents the proportion of correct predictions across all classes, making it easy to interpret and compare different models.

## Baseline Model

Model Description:
The model used in this analysis is a Random Forest Classifier, a type of ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes (classification) or the average prediction (regression) of the individual trees.

Features in the Model:

Quantitative Features:

minutes: The time required to prepare the recipe.
 
n_ingredients: The number of ingredients used in the recipe.
 
Ordinal Features:
 
calories_category: Categorized calories into Low, Moderate, and High.
 
Nominal Features (After Encoding):
 
average_rating_cat: The target variable representing the categorized average rating of recipes.

Performance of the Model:

The baseline model achieved an accuracy of approximately 88.03% on the test dataset.

Model Evaluation:

Accuracy Score: The accuracy score of 88.03% indicates that the model correctly predicted the average rating category for around 88% of the recipes in the test dataset.
Interpretation: While an accuracy of 88.03% is relatively high, it's essential to consider the specific context and requirements of the problem. In some cases, such as when the classes are imbalanced or misclassification costs vary, other metrics like precision, recall, or F1-score may provide a more comprehensive evaluation. Additionally, further analysis, including feature importance and model interpretation, can provide insights into the model's behavior and potential areas for improvement.

## Final Model

Features Added:

Two new features were engineered using the QuantileTransformer:

Transformed average_rating: Applied QuantileTransformer to transform the average_rating feature to follow a normal distribution. This transformation can help mitigate the impact of outliers and skewed distributions, making the data more suitable for modeling algorithms that assume normality.

Justification for Feature Engineering:

Normalizing Numeric Features: By transforming average_rating to follow a normal distribution, we ensure that the feature has a consistent scale and distribution, which can improve the performance of certain modeling algorithms, such as RandomForestClassifier.

Modeling Algorithm:

Random Forest Classifier: Random Forest is an ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes (classification) or the average prediction (regression) of the individual trees. It's known for its robustness to overfitting, handling of missing values, and ability to capture non-linear relationships in the data.

Hyperparameters and Hyperparameter Tuning:

Hyperparameters Tuned:

n_estimators: Number of trees in the forest.

max_depth: Maximum depth of the trees.

min_samples_split: Minimum number of samples required to split an internal node.

Grid Search: Used GridSearchCV to search for the best combination of hyperparameters by exhaustively trying all combinations from a specified grid of hyperparameters.

Scoring Metric: Evaluated hyperparameters based on accuracy, as it is a suitable metric for classification tasks when classes are balanced.

Model Performance and Improvement:

Best Hyperparameters:

n_estimators: 10

max_depth: None

min_samples_split: 10

Final Model Accuracy: The accuracy of the final model on the test dataset is 100%.

Comparison with Baseline Model: The final model's accuracy of 100% represents a significant improvement over the baseline model's accuracy of approximately 88.03%. This improvement suggests that the feature engineering and hyperparameter tuning processes effectively enhanced the model's predictive performance.

## Fairness Analysis

Groups Selected:

Group X: Recipes with a low number of ingredients (simpler recipes)

Group Y: Recipes with a high number of ingredients (more complex recipes)

Evaluation Metric:

Accuracy (since we are dealing with a classification problem)

Null Hypothesis:

Our model is fair. Its accuracy for recipes with a high number of ingredients and recipes with a low number of ingredients are roughly the same, and any differences are due to random chance.

Alternative Hypothesis:

Our model is unfair. Its accuracy for recipes with a high number of ingredients is lower than its accuracy for recipes with a low number of ingredients.

Test Statistic:

Difference in accuracy between Group X and Group Y.

Significance Level:

α = 0.05

Result:

Precision for Group X: 1.0

Precision for Group Y: 1.0

Test Statistic (Precision difference): 0.0

p-value: 0.482

Null Hypothesis: Our model is fair. Its precision for low calorie and high calorie recipes are roughly the same, and any differences are due to random chance.

Alternative Hypothesis: Our model is unfair. Its precision for low calorie recipes is lower than its precision for high calorie recipes.

Significance Level: 0.05

Conclusion: Fail to reject null hypothesis. There is no evidence to suggest that the model's precision differs significantly between low and high calorie recipes.


