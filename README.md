# YouTube Trending Videos - Exploratory Data Analysis (EDA)

## Project Overview
This project aims to analyze YouTube trending videos to identify key factors influencing their performance on the trending list. The analysis focuses on the relationship between various features such as views, likes, dislikes, comments, video description, and tags to determine their impact on trending.

## Objectives
- Identify the correlation between views and trending.
- Analyze the relationship between likes, dislikes, comments, description, and tags with trending.
- Determine the most popular video categories based on views and trending count.
- Find the optimal time to publish YouTube videos for maximum engagement.
- Understand data distributions and characteristics using statistical methods and visualizations.

## Dataset
The dataset consists of YouTube trending videos with key features such as:
- `video_id`: Unique ID for each video.
- `trending_date`: Date when the video was trending.
- `title`: Video title.
- `channel_title`: Channel name.
- `category_id`: YouTube category ID.
- `publish_time`: Timestamp of video publication.
- `tags`: Video tags.
- `views`: Number of views.
- `likes`: Number of likes.
- `dislikes`: Number of dislikes.
- `comment_count`: Number of comments.
- `description`: Video description text.
- `trending_count`: Number of times the video appeared on the trending list.

## Exploratory Data Analysis (EDA)
### 1. Data Cleaning and Preprocessing
- Removed missing or irrelevant data.
- Converted timestamps to proper date and time formats.
- Extracted relevant time-based features such as publish hour and trending duration.
- Tokenized and analyzed textual data (tags and description length).

### 2. Data Distribution Analysis
- **Histogram & Distribution Plots**:
  - Views are right-skewed, meaning most videos have relatively low views, with a few outliers having very high views.
- **Boxplots**:
  - Analyzed views distribution across different categories to identify top-performing genres.
- **QQ Plots**:
  - Confirmed that data is not normally distributed, justifying the use of Spearman correlation for analysis.

### 3. Correlation Analysis
- **Spearman correlation** was used due to non-normal data distribution.
- Correlation between features and trending count:
  - `likes` (0.426), `views` (0.424), `dislikes` (0.412), `comments` (0.387) → Moderate correlation.
  - `description length` (0.051) and `tags length` (-0.007) → Very weak correlation.
- **Heatmaps** were used to visualize feature correlations.

### 4. Most Popular Video Categories
- Median views per category:
  - **Gaming (1.3M views)**, **Music (1.1M views)**, **Film & Animation (910K views)** ranked highest.
- Most trending categories (based on trending score):
  - **Music (63.1%)**, **Entertainment (13.3%)**, **Film & Animation (5.3%)**.
- Recommendations:
  - For aspiring YouTubers, focusing on **Music, Entertainment, and Film & Animation** increases the chance of trending.

### 5. Best Time to Publish Videos
- Most frequent upload time: **16:00 (4 PM)**.
- Best performing time slots (highest views): **Evening (16:00-18:00) and Night (17:00-23:00).**
- Analyzed the significance of weekday uploads using **Chi-square hypothesis testing**:
  - No significant difference in upload frequency among weekdays.
  - All weekdays offer an equal chance for videos to trend.

## Visualizations
The following visualizations were used to support the analysis:
- **Histograms & Distribution Plots**: To understand data skewness.
- **Boxplots**: To compare views across categories.
- **Heatmaps**: To visualize correlations between features.
- **Scatterplots & Regression Lines**: To analyze relationships between views and other factors.
- **Bar Charts**: To display top trending categories and upload time distributions.

## Conclusion
- **Engagement (likes, views, comments, and dislikes) matters more than metadata (tags and description).**
- **Music, Entertainment, and Film & Animation** categories have the highest probability of trending.
- **Evening and Night uploads (4 PM - 11 PM) perform best in terms of views.**
- **Weekday uploads are equally effective, with no significant difference in performance.**

## Next Steps
- Perform **sentiment analysis** on video comments to gauge audience reactions.
- Use **predictive modeling** to estimate the probability of a video trending.
- Compare YouTube trending performance across **different countries**.

## Dependencies
This project uses the following Python libraries:
- `pandas` - for data manipulation.
- `matplotlib` & `seaborn` - for data visualization.
- `scipy.stats` - for statistical analysis.
- `statsmodels` - for hypothesis testing.

## Running the Code
1. Install dependencies using:
   ```bash
   pip install pandas matplotlib seaborn scipy statsmodels
   ```
2. Run the Jupyter Notebook or Python script containing the EDA steps.
3. Review the generated plots and statistical insights.

## Author
This project was conducted as part of an exploratory analysis of YouTube trending videos data. Further improvements and insights are welcomed!
