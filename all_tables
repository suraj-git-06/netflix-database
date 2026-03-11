CREATE TABLE Movies(
movie_id INT PRIMARY KEY,
title VARCHAR(100),
genre VARCHAR(50),
release_year INT,
duration INT
);

CREATE TABLE Users(
user_id INT PRIMARY KEY,
name VARCHAR(100),
country VARCHAR(50),
subscription_type VARCHAR(50)
);

CREATE TABLE Ratings(
rating_id INT PRIMARY KEY,
movie_id INT,
user_id INT,
rating INT,
rating_date DATE,
FOREIGN KEY(movie_id) REFERENCES Movies(movie_id),
FOREIGN KEY(user_id) REFERENCES Users(user_id)
);
