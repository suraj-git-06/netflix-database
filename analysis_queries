-- View all Movies
SELECT * FROM Movies;

-- View all Users
SELECT * FROM Users;

-- View all Ratings
SELECT * FROM Ratings;

-- Show movie ratings with user names
SELECT u.name, m.title, r.rating
FROM Ratings r
JOIN Users u ON r.user_id = u.user_id
JOIN Movies m ON r.movie_id = m.movie_id;

-- Highest rated movies
SELECT m.title, AVG(r.rating) AS avg_rating
FROM Movies m
JOIN Ratings r ON m.movie_id = r.movie_id
GROUP BY m.title
ORDER BY avg_rating DESC;

-- Movies count by genre
SELECT genre, COUNT(*) AS total_movies
FROM Movies
GROUP BY genre;

-- Most active users
SELECT user_id, COUNT(*) AS ratings_count
FROM Ratings
GROUP BY user_id
ORDER BY ratings_count DESC;

-- Movies longer than average duration
SELECT title
FROM Movies
WHERE duration > (SELECT AVG(duration) FROM Movies);

-- Movies released after 2010
SELECT title, release_year
FROM Movies
WHERE release_year > 2010;

-- Average rating per genre
SELECT m.genre, AVG(r.rating) AS avg_rating
FROM Movies m
JOIN Ratings r ON m.movie_id = r.movie_id
GROUP BY m.genre;

-- Premium subscription users
SELECT name
FROM Users
WHERE subscription_type = 'Premium';

-- Movies with rating 5
SELECT m.title
FROM Movies m
JOIN Ratings r ON m.movie_id = r.movie_id
WHERE r.rating = 5;

-- Top 3 highest rated movies
SELECT m.title, AVG(r.rating) AS avg_rating
FROM Movies m
JOIN Ratings r ON m.movie_id = r.movie_id
GROUP BY m.title
ORDER BY avg_rating DESC
LIMIT 3;

-- Number of users per country
SELECT country, COUNT(*) AS total_users
FROM Users
GROUP BY country;

-- Movies released before 2010
SELECT title, release_year
FROM Movies
WHERE release_year < 2010;

-- Average movie duration by genre
SELECT genre, AVG(duration) AS avg_duration
FROM Movies
GROUP BY genre;
