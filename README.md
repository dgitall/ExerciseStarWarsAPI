# ExerciseStarWarsAPI
 
## Introduction
For this exercise, we are creating a rudimentary Python ETL process to bridge 2 API data sources. Your supervisor has approved core Python and the OS, Requests, and JSON modules for this project.

## Part 1: Model Film API and Movie API
1. Register for a free Open Movie Database (OMDB) API key at http://www.omdbapi.com/.

2. Review the the Star Wars API and OMDB API.

3. Create an object model for Star Wars films that includes: "title","episode_id","opening_crawl", "director","producer","release_date" and a list for characters.

4. The model should also include plot, Rotten Tomatoes rating, and Box Office Gross from the OMDB database.

5. Create character object model. Each character should include: "name", "height", "mass", "hair_color", "skin_color", "eye_color","birth_year", and "gender".

6. Create an object model for the Star Wars Library. This library should include all the Star Wars movie objects with the following attributes:

  * List of Movies:
  * List of Shows:
  * Last Updated: Date
7. Include a method to sort the list of movies and shows to use when you are importing new Star Wars Movies.

8. Include methods in the Star Wars Library to later make API calls and build film objects.

## Part 2: Code the Object with a Data Class Decorator
1. Use a Data Class decorator to describe and code the Star Wars Film Object and Character Object.

2. Include metadata for any field that should have a unit measurement. For instance, Box Office Gross's unit is U.S. dollars, and mass fields' units in the Star Wars API are in kilograms.

3. For the Star Wars Film Class, include an Init function ensuring Episode ID is required. Override the magic functions for ">,=,>,>=" comparison operators based on an Episode ID to assist the sorting in the Star Wars Library object.

4. For the Characters class, implement a custom Str model that includes all of its attributes.

5. Code the Star Wars Library based on your model. While coding the sort when new movies are added, assume the Star Wars Film object has magic functions for ">,=,>,>=" comparison operators.
## Part 3: Query the Star Wars API and the Movie API
Create methods in the Star Wars Library that will query the Star Wars API and Movie API to fill in the fields you created in your model. For the characters, you will need to make multiple calls for each film API call.

For each character URL in each film object item, create a character object from a JSON call.

Hint: There may be no easy key between 2 API's and you may have to manually create a bridge or manually set up dictionaries to link one unique identifier to another.

## Part 4: Code Defensively
Use Try/Except blocks appropriately to keep your program from exiting if there are any exception issues.

## Part 5: Searching your Library for Films
Change your Library object to include a method to search for a Star Wars Movie based on Episode number or Movie Title.

Ask the user to input either a movie title or episode id. Search your library and return the result. Display the movie details.

## Part 6: Searching your Library for Characters
Change your library object to include a method to search for a character in all the movies based on the character name.

Ask the user to input a character. Return all movies a list of movies the character appears in and print the string representation of the character.

## Part 7: Beautify and Menu
1. Refactor your code to use extra files for your Star Wars Film code and library code.
2. Use imports to include these files into a run.py file.
3. Use the run.py to start the application.
4. In this run file, create a function or object with methods that create a menu system to allow the user to run multiple searches for the character, movie, or episode number.
5. Use and research the code: if __name__ == "__main__" :
6. Use this code to automatically start your menu function on load.
## Part 8: Stretch Goal, Auto-Initialize your Objects
Change your run.py file to check the state of the library when you load the file. If the library is empty, run the previously created methods to populate the library.

## Part 9: Stretch Goal, Save Work to Azure Cosmos DB
Research Azure Cosmos DB MongoDB API. Using the __dict__ magic function, create a list of dictionaries from your Library, and Film Objects. Save your list of dictionaries as a collection of documents on the Azure Cosmos DB MongoDB API. Create a new python file and query your collection on the Azure Cosmos DB MongoDB API.

Auto-Initialize your library directly from the Azure Cosmos DB.