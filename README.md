# simpledata
Simple data analysis with IMDB data
Libraries used: NumPy (for linear algebra), matplotlib (for data visualization), pandas (for reading and analyzing data)

df = pd.read_csv('IMDB-Movie-Data.csv') # imported the csv file using pandas. and created a dataframe named "df"
print("Highest Rated Movie:",df.Title[max(df.Rating)],max(df.Rating)) # printed the rating and name of the highest rated movie using pandas

plt.hist(df.Rating) # learned the graph distribution using the "hist" method
plt.title("Ratings") # titled the graph "Ratings"
plt.show() # used the "show" method to make the graph appear on the screen.

#Graph with metascores
meta_score = df.Metascore.dropna() # deleted the data that is empty or NaN with the "dropna" method.
plt.hist(meta_score) # learned the graph distribution using the "hist" method
plt.show()

# movies with runtimes
plt.hist(df["Runtime (Minutes)"]) # learned the graph distribution using the "hist" method and pandas.
plt.title("Movie's Runtime in minutes") # titled the graph 
plt.xlabel("Number of movies with runtime") # created the title of the x-axis
plt.show()

#Movies released by years
plt.title("Movies released by year") # titled the graph 
plt.xticks(range(2005,2017)) #  changing the labels on the x-axis.
plt.hist(df.Year,30) # The value "30" determines the size of the graph bar
plt.show()
