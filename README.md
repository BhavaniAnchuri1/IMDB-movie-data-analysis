# IMDB-movie-data-analysis


## project overview
Conducted extensive exploration of IMDB movie datasets, delving into various attributes such as movie directors, IDs, gender, department, movie name . Utilized SQL queries to navigate and understand the structure of the IMDB database.Identifying key tables and relationships between them, Developed and optimized SQL queries to extract specific insights and information from the IMDB movie database.


## SQL Queries

```sql
use project_movie_database ;
select *from movies;
select*from directors;
select count(*)  as total_movie from movies;
select count(*) from directors
 where gender=1;
  select *from directors where name Like 'steven%';
 select * from directors where name in ('James Cameron', 'Luc Besson', 'John Woo');
  select name from directors
 where gender= 1
 order by uid desc
 limit 10 ;
 select original_title from movies
 order by popularity desc
 limit 3;
 select original_title from movies
 order by revenue desc
 limit 3;
```

## Key Insights and Observations
1. The dataset contains information about movies and directors, including details like movie titles, directors' names, gender, departments, movie popularity, revenue, and average vote count.

2. The total number of movies present in the dataset is obtained using the COUNT(*) query on the movies table.

3. The queries demonstrate how to retrieve specific directors' information, such as finding directors with names like 'James Cameron', 'Luc Besson', and 'John Woo', or directors whose names start with 'Steven'.

4. The analysis includes counting the number of female directors present in the dataset by filtering the directors table based on the gender column.

5. The query to find the 10th first woman director sorts the directors table by uid in descending order and limits the result to 10 rows, providing the name of the 10th female director.

6. The analysis identifies the three most popular movies and the three most bankable (highest revenue) movies by ordering the movies table by the popularity and revenue columns, respectively.

7. To find the most awarded movie since January 1st, 2000, the query filters the movies table based on the release_date and orders the result by the vote_count column in descending order, taking the first result.

8. The analysis demonstrates how to find movies directed by a specific director (e.g., Brenda Chapman) by joining the movies and directors tables based on the director_id column.

9. The query to identify the director who made the most movies groups the data by director's name and counts the number of movies for each director, ordering the result by the movie count in descending order and taking the first result.

10. Similarly, to find the most bankable director, the query groups the data by director's name and calculates the sum of revenue for each director, ordering the result by the total revenue in descending order and taking the first result.

These insights and observations showcase the power of SQL in performing data analysis on the IMDB movies dataset, enabling the retrieval of valuable information about movies, directors, and their associated metrics.
