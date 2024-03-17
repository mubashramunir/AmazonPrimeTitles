# AmazonPrimeTitles
The dataset amazon_prime_titles.csv appears to contain information about titles (such as movies and TV shows) available on Amazon Prime. Here's a summary of its structure and some insights:

Number of Entries: 9,668 titles.
Columns: It has 12 columns, including:
show_id: Unique identifier for each title.
type: Type of title, such as Movie or TV Show.
title: The name of the title.
director: Name of the director(s).
cast: List of main cast members.
country: The country of origin.
date_added: The date the title was added to Amazon Prime (only 155 non-null entries, suggesting many missing values).
release_year: The year the title was released.
rating: The content rating of the title.
duration: Duration of the title, in minutes for movies and seasons for TV shows.
genre: Categories or genres the title is listed under.
description: A brief description of the title.

 We observe a variety of content, including comedies, dramas, documentaries, and suspense titles, from different countries like Canada, India, the United States, and the United Kingdom. 
 The dataset also includes a mix of newer and older titles, with release years ranging from at least 1989 to 2018 among the first few entries.

# Difference between calculated columns and measures:
Calculated columns are computed at the row level and stored in the dataset, while measures are computed at the aggregated level and are dynamic based on the context of the visualization.
Calculated columns are best for static calculations that need to be used across multiple visualizations, while measures are best for aggregations and calculations that depend on filters and slicers.

# Total Titles:
Created a measure using DAX (Data Analysis Expressions) like Total Titles = COUNTROWS('Amazon Prime Dataset').

# Total Ratings:
Create a measure using DAX like Total Ratings = SUM('Amazon Prime Dataset'[Ratings]).

# Total Genres:
Created a measure using DAX like Total Genres = DISTINCTCOUNT('Amazon Prime Dataset'[Genres]).

# Total Directors:
Created a measure using DAX like Total Directors = DISTINCTCOUNT('Amazon Prime Dataset'[Directors]).

# The Start Date:
Used the MIN function in DAX to find the earliest date from the dataset.

# The End Date:
Used the MAX function in DAX to find the latest date from the dataset.

# Genres by total shows:
Used a clustered bar chart to display genres and their corresponding total shows.

# Ratings by total shows:
Used a clustered column chart to display ratings and their corresponding total shows.

# Total shows by country:
Used a map visual and a stacked bar chart to display total shows by country.

# The distribution of movies and TV shows:
Used a pie chart to show the distribution.

# Total shows by release year:
Used a line chart to display total shows by release year.


Visuals effectively communicate the information and insights. The dashboard is a mix of different types of visuals
Experimented with various visual types such as bar charts, line charts, pie charts, maps, etc., to provide a diverse representation of the data.
A comprehensive and visually appealing dashboard using the Amazon Prime dataset in Power BI.
