# SQL_Assessment

insert into movies(title, runtime, genre, imdb_score, rating) values('The Titanic', 120, 'Drama', 9.0, 'PG'),  ('Scary Movie', 80, 'Comedy', 7.6, 'R');

select * from movies where genre = 'sci-fi';

select * from movies where imdb_score >= 6.5;

select * from movies where rating = 'G' or rating = 'pg' and runtime < 100;

select genre,avg(runtime) from movies where imdb_score < 7.5 group by genre;

update movies set rating = 'R' where title ='starship troopers';

select title, rating from movies where genre = 'horror' or genre ='documentary';

select rating, avg(imdb_score), max(imdb_score), min(imdb_score) from movies group by rating;

select rating, avg(imdb_score), max(imdb_score), min(imdb_score) from movies group by rating having count(*) > 1;

mysql> delete from movies where rating = 'R';

drop table movies;

drop database movies_db;
