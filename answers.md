1) Find all the robots from Star Wars.

SELECT name FROM robots WHERE source = 'Star Wars';


2)Find the robot with an "anxious" personality.

SELECT name FROM robots WHERE personality = 'anxious';


3) Find all recipes that are nut free.

SELECT name FROM recipes WHERE nut_free = true


4) Count the number of recipes that are gluten free but not vegetarian.

SELECT COUNT(gluten_free = true AND vegetarian=false) FROM recipes;


5) Find the animal with the most legs.

SELECT name FROM animals WHERE number_of_legs = (SELECT MAX(number_of_legs) FROM animals);


6) Find the board game that takes the least amount of time to play.

SELECT name FROM board_games WHERE mins_to_play = (SELECT MIN(mins_to_play) FROM board_games)


7) Find the recipe that takes the most time to prepare.

SELECT name FROM recipes WHERE minutes_required = (SELECT MAX(minutes_required) FROM recipes);


8) Find all the robots whose name starts with the letter M.

SELECT name FROM robots WHERE name LIKE 'M%';


9) Count the number of board games that can be played by 8 people.

SELECT COUNT(max_players) FROM board_games WHERE max_players > 7;


10) Find all animals that are swimming and egg-laying.

SELECT name FROM animals WHERE swimming = true AND egg_laying = true;


11)Find all animals that are swimming and egg-laying but not flying.

SELECT name FROM animals WHERE swimming = true AND egg_laying = true AND flying = false;


12) Find the board game that supports the largest number of people.

SELECT name FROM board_games WHERE max_players = (SELECT MAX(max_players) FROM board_games); 
