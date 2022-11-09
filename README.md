# Movie-Recommendation-System

* In this case study I have built a movie recommendation system that analyze the users movie watching patterns and based on that it recommends movies to users.
<br/>
for example - Big websites like Netflix, Amazon prime, YouTube, etc uses movie recommendation systems.
<br/>
I always wonder that how do they recommend movies to their users and for that did some research on it, I find out that they have their own movie recommendation systems.

### Mostly movie recomendation systems are of three types - 
> 1. _**Content based movie recommendation system**_ - In this type recommendation system analyze what kind of content user is watching based on that it will recommend movies to you. for example if you watch a lot of **Superhero movies** recommendation system will recommend you Superhero movies and similar to such movies.
> 2. _**Popularity based movie recommendation system**_ - In this type recommendation system recommend movies based on how popular a perticular movie is. if certain movies are the most populars then it will recommend you these movies.
> 3. _**Collaboration based movie recommendation system**_ - In this type movies are recommended based on users watching pattern.

## To build such a machine learning model I used following steps - 
> 1. Ask
> 2. Prepare
> 3. Process
> 4. Analyze
> 5. Cosine similarity
> 6. Build model
> 7. result

* Required dependencies are Numpy, Pandas, Sklearn, difflib.

1. _**Ask**_ - In this Phase I ask questions such as 1)Which type of data we require?, 2)How we going to collect the data?, 3) What kind of features we need?, etc.
2. _**Prepare**_ - In this phase I collect the movies data
3. _**Process**_ - In this phase I process the data means. First I load the csv data to pandas DataFrame after that check how many rows and columns this dataset contains, after that I select the required features for the movie recommendation system. \nWe allready know that the text data contains null values so replace the null values with the null string "", combine all the selected features, convert the text data to feature vectors using 'TfidfVectorizer()' it converts text data into numerical values.
4. _**Analyze**_ - In this Phase I analyze the data.
5. _**Cosine similarity**_ - Use cosine similarity to find the similarities and from this we get the similarity score.
6. _**Build model**_ - get the movie name from the user and create a list with all the names in the dataset using tolist() function of pandas. then find a match for the movie name given by the user and from that find a close match i.e. first element of the list. after this step I find index of the movie with title getiing the list of similar movies. sort the list in descending order as higher the similarity score movie recommendation will be accurate.
7. __**result**_ - and finally using a for loop we only recommend 30 movies to user from the sorted list.

#### In this way this model recommends movies
