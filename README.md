# Machine-Learning
Recommend system

### 1. Dataset
'googleplaystore.csv' file of "https://www.kaggle.com/datasets/lava18/google-play-store-apps"
; explanation ; details of the applications on Google Play(2019)
This information is scraped from the Google Play Store.
The Play Store apps data has enormous potential to drive app-making businesses to success.
Actionable insights can be drawn for developers to work on and capture the Android market.


* columns
 * (1)  : App: Application name
 * (2)  : category: Category the app belongs to -FAMILY, GAME, TOOLS, BUSINESS
 * (3)  : rating: Overall user rating of the app (as when scraped)
 * (4)  : Reviews: Number of user reviews for the app (as when scraped)
 * (5)  : Installs: Number of user downloads/installs for the app (as when scraped)
 * (6)  : Type : Paid / Free
 * (7)  : Price : Price of the app (as when scraped)
 * (8)  : Content rating : Age group the app is targeted at - Everyone /Teen / Mature 17+
 * (9)  : Last Updated ; Date when the app was last updated on Play Store (as when scraped)
 * (10) : Current Ver ; Current version of the app available on Play Store (as when scraped)
 보통 버전 번호는 반드시 X.Y.Z
X는 주(主, Major)버전 번호이고, Y는 부(部, Minor)버전 번호이며, Z는 수(修, Patch)버전 번호이다. 각각은 반드시 증가하는 수여야 한다
 * (11) : Android Ver ; Min required Android version (as when scraped)
 * (12) : Size: Size of the app (as when scraped)
 * (13) : Genre: An app can belong to multiple genres (apart from its main category). For eg, a musical family game will belong to -Tools/ Entertainment / Education/ Business


### 2. Objectives of analysis
**Main objectives**: Find out which categories were popular in the year and recommend apps based on them.
**Sub objectives**: 
1. Find out what properties popular applications have.
2. Find out the correlation between Rating, Review count, and Install count.(Because it is difficult to evaluate apps only with Rating.)
3. Afterwards, popular apps such as "Category", "Age", and "Paid/Free" are recommended based on the measured "Popularity" criteria.


### 3. Dataset discription
1. Statics
  *   df.shape
  *   df.index
  *   df.dtypes
  *   df.describe()
  *   df.columns
  *   df.info()
2. Tables
  *   df.info()
3. Plots: plot 'category', 'Installs', 'Rating', 'Price' and 'Size'.
  *   plt.scatter()
  *   plt.plot(x_value, y)
4. Missing values
  *  If 'numerical', replace with the average value of each column.
  *  'Null' value of Rating is replaced with a value similar to the number of installations.
5. Outliers
  *  If you have 100 or less reviews, report it as Outlier and drop it.
