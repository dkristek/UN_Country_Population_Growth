# DB Script for creating initial database and agregate data
## Create Populations Table

CREATE TABLE populations (
record_key VARCHAR(5) NOT NULL,
country_id VARCHAR(1) NOT NULL,
mid_year VARCHAR(4) NOT NULL,
population VARCHAR(40) NOT NULL,
PRIMARY KEY (record_key)
);

## Create Country Table
CREATE TABLE countries (
country_id VARCHAR(1) NOT NULL,
country_name VARCHAR(30) NOT NULL,
PRIMARY KEY (country_id)
);

## Create DB Join
CREATE TABLE countries_populations AS
(SELECT populations.record_key, populations.country_id, countries.country_name, populations.mid_year, populations.population
FROM countries
INNER JOIN populations
ON countries.country_id = populations.country_id);

# Database tables
countries

 - country_id varchar pk

 - country_name varchar

populations

 - record_key varchar pk

 - country_id varchar fk - countries.country_id

 - mid_year int

 - population int

countries_populations

- record_key varchar pk

- country_id varchar fk - populations.country_id

- country_name varchar fk - countries.country_name

- mid_year int fk - populations.mid_year

- population int fk - populations.population
