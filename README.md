# Movie Recommendation System

A content-based movie recommendation system that analyzes users' movie-watching patterns and recommends similar movies. Platforms like Netflix, Amazon Prime, and YouTube all rely on systems like this to guide users to content they're likely to enjoy - this project is a case study exploring how one works under the hood.

## Types of recommendation systems

**Content-based** - recommends movies similar in content/genre to what a user already watches. A user who watches a lot of superhero movies gets more superhero recommendations.

**Popularity-based** - recommends whatever is most popular overall, regardless of individual taste.

**Collaborative** - recommends movies based on patterns across many users' watching behavior.

## Approach

Built following a standard analytics workflow: Ask, Prepare, Process, Analyze, Model, Result.

**Ask** - define what data is needed, how to collect it, and which features matter.

**Prepare** - collect the movies dataset.

**Process** - load the CSV into a pandas DataFrame, inspect its shape, select the relevant features, fill missing text values with an empty string, combine the selected features into one text field, and convert it to numerical feature vectors using `TfidfVectorizer()`.

**Analyze** - explore the processed data.

**Similarity scoring** - compute cosine similarity between movies based on their feature vectors.

**Build model** - take a movie title from the user, match it against the dataset (using `difflib` for close matches), and rank other movies by similarity score.

**Result** - return the top 30 most similar movies.

**Dependencies:** NumPy, Pandas, scikit-learn, difflib
