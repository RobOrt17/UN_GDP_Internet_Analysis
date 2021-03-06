# UN_GDP_Internet_Analysis

A guided exploration of UN data (Gross Domestic Product and Internet Usage)
Create a data folder in your local project repository.

Download these two CSV files and place them in the data folder:

a. Gross Domestic Product (GDP) per capita http://data.un.org/Data.aspx?d=WDI&f=Indicator_Code%3aNY.GDP.PCAP.PP.KD DO NOT APPLY ANY FILTERS

rename the file to gdp_percapita.csv
open it with a text editor (not excel) and take a look
b. Percentage of Individuals using the Internet http://data.un.org/Data.aspx?d=ITU&f=ind1Code%3aI99H DO NOT APPLY ANY FILTERS

rename the file to internet_use.csv
open it with a text editor (not excel) and take a look
Launch a Jupyter Notebook.

IMPORTANT: You are likely to get errors along the way. When you do, read the errors to try to understand what is happening and how to correct it.
Use markdown cells to record your answers to any questions asked in this exercise. On the menu bar, you can toggle the cell type from Code to Markdown.
Import the required packages with their customary aliases as follows:

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

Use the %matplotlib inline magic command so that your plots show in the notebook without having to call plt.show() every time.

Using the pandas read_csv() method, read the GDP dataset into your notebook as a DataFrame called gdp_df. Take a look at the first 6 rows.

Repeat for the internet use dataset. Call this DataFrame internet_df. Take a look at the first six rows.

Look at the shape of each DataFrame - how many rows? How many columns?

Take a look at the datatypes for the columns in each DataFrame.

Take a look at the last 10 rows of each DataFrame in turn.

Drop the value footnotes column from both DataFrames. Check that this worked as expected.

Change the columns for the GDP Per Capita DataFrame to ‘Country’, ‘Year’, and ‘GDP_Per_Capita’.

Change the columns for the Internet Users DataFrame to ‘Country’, ‘Year’, and ‘Internet_Users_Pct’.

Merge the two DataFrames to one. Merge all rows from each of the two DataFrames. Call the new DataFrame gdp_and_internet_use.

Look at the first five rows of your new DataFrame to confirm it merged correctly.

Look at the last five rows to make sure the data is clean and as expected.

Subset the combined DataFrame to keep only the data for 2004, 2009, and 2014. Check that this happened correctly.

Create three new DataFrames, one for 2004, one for 2009, and one for 2014. Give them meaningful names that aren't too long.

Which country had the highest percentage of internet users in 2014? What was the percentage? (Try typing the first 3 letters of your DataFrame name and hitting the tab key for auto-complete options).

Which country had the lowest percentage of internet users in 2014? What was the percentage?

Repeat for 2004 and 2009.

Which country had the highest gdp per capita in 2014? What was the gdp per capita?

Which country had the lowest gdp per capita in 2014? What was the gdp per capita?

Create some scatterplots:
a. 2004 Percent Using the Internet vs GDP Per Capita
b. 2009 Percent Using the Internet vs GDP Per Capita
c. 2014 Percent Using the Internet vs GDP Per Capita

Are there differences across years? What do the plots tell you about any relationship between these two variables? Enter your observations as a markdown cell.

Look at the distribution of gdp per capita values for 2014. Is it unimodal?

Look at the distribution of Internet Use for 2014. Is it unimodal?

What are the top 5 countries in terms of internet use in 2014?

Create a DataFrame called top_5_internet from the combined DataFrame that has all three years for the 5 countries that had the greatest 2014 internet usage. You should have 15 rows. Check that this is true.

Create a seaborn FacetGrid to show the internet usage trend across the years 2004, 2009, and 2014 for these 5 countries (those with the highest reported internet use in 2014). Which country had the greatest growth between 2004 and 2014? Is there a plotting issue with Bermuda? Can you fix it?

Repeat the steps above to look at the trend for the 5 countries with the lowest 2014 internet usage. Which country has consistently had the least internet use?

Find the top 5 countries for 2014 in terms of GDP per capita; create a DataFrame to look at 10-year trends (use 2004, 2009, 2014 to look at the 10-year trend) in gdp per capita for the 5 countries with the highest 2014 GDP per capita. Use a seaborn facet grid for this.

Repeat this one more time to look at 10-year trend for the 5 countries for 2014 with the lowest GDP per capita.

Is there anything surprising or unusual in any of these plots? Searching on the internet, can you find any possible explanations for unusual findings?

