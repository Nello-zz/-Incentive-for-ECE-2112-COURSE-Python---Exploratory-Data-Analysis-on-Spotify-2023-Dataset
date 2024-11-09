## Exploratory Data Analysis (EDA) on Music Track Dataset using Python

 **Introduction**

In this project, we’ll be diving into an exploratory data analysis (EDA) of a dataset containing information on top music tracks. Our goal is to gain insights into the data, identify trends, and explore relationships between different musical attributes and other important features like stream counts, release years, and chart rankings across platforms such as Spotify, Apple Music, Deezer, and Shazam.

Through this analysis, we will uncover patterns, trends, and potential outliers that could shed light on the factors influencing track popularity.


### Prerequisites

 ***Software Used:***
- Jupyter Notebook 
- GitHub
  
***Libraries Required:***
  - Pandas
  - Matplotlib
  - Seaborn

 ### Setup

***Install Necessary Libraries***
If you haven’t installed the required libraries yet, you can do so by running the following command in your Jupyter Notebook:

```
!pip install pandas matplotlib seaborn
```

***Load the Dataset***
Ensure that the dataset is available in your project directory. For this EDA, I’ve converted the CSV file into an Excel file for personal preference, but I’ll provide both the CSV and Excel versions.

Load the dataset using this code:

```
import pandas as pd
track_ds = pd.read_excel('spotify_2023.xlsx')
```

### EDA Sections

 **Overview of the Dataset**
 
We start by getting a quick overview of the data to understand its structure:

**Handling Missing Data**

Now, let's check for missing values. For this EDA, I’ve decided to drop the `speechiness_%` column, as it doesn’t add much value for this analysis. For other missing values, I’ll fill them with the median of that column’s data.

**Checking for Duplicates**

We also want to make sure that the data doesn't contain any duplicate rows. Since there’s a large volume of data, we'll use a code to check for duplicates.

**Descriptive Statistics**

Let's compute some basic statistics, like the mean, median, and standard deviation, for the numeric columns.

Additionally, we’ll look at the unique values in columns such as `release_year` and `artist_count` to understand the data distribution.

**Identifying Outliers**

Outliers can provide shows us data that standsout from the dataset. We’ll use the Interquartile Range (IQR) method to identify any extreme values in the numerical columns. This is how we detect outliers in the `stream_count` column.

**Top Performers**

Next, as what any platforms do for their charts, let’s focus on the top performers and tracks. We’ll find the 5 most streamed tracks and the most frequent artists in the dataset.

**Temporal Trends**

***Time(Month and Year) and Number of track***
We’ll explore trends over time, looking at how many tracks were released per month and year. This will help us understand if there’s any correlation between release time and the number of tracks released:


***Streams and Musical Attributes***

Now, let’s dive deeper into the relationship between streams and musical attributes such as danceability, energy, and valence, instrumentalness, acousticness, liveness. We’ll also check the correlations between these attributes.

**Platform Popularity**

Lastly, let’s analyze how the tracks are distributed across different platforms. We’ll compare the number of tracks in Spotify, Apple Music, Deezer, and Shazam.

 ### Last Note

This analysis has provided us with key insights into the dataset, including trends, outliers, and correlations. We’ve explored how musical attributes relate to streams, how tracks perform across platforms, and how the dataset has evolved over time. As a next step, you might want to build predictive models or further explore platform-specific trends. One possible improvement to the analysis would be to incorporate the genre of each track for a more comprehensive view of music trends.

 ### Troubleshooting

- Make sure the dataset is correctly loaded from the correct directory.
- Verify that column names in the code match those in the dataset.
- Ensure all necessary libraries (Pandas, Matplotlib, Seaborn) are installed and imported correctly.


