# PostgreSQL

*Much of the documentation here may not be PostgreSQL specific, and could work in other SQL environments*

## Accessing PostgreSQL

From computer: 
- PGAdmin; GUI for Postgres server and database interaction
- psql; cli tool for accessing postgres databases, must login and have different config (username, db, etc.) to enter

From app:
- Docker postgres; can use docker-compose to already set up all env files to easily exec and psql into the database;
  - Challenge of this approach: Need to have migrations that set this up
- From Golang; have to create a connect string that can then be wrapped within the built in DB library that go has

## Querying Tips

Creating prepared statements and preparing your database for queries is far more efficient than general querying, even if the database is open the whole time. Compiled languages can keep the database open without opening and closing (versus scripting languages like python) so this is also more efficient.

## Helpful Implementation Commands

**DESCRIBE (before other command)** - Postgres describes to you exactly what it will do to run each command and its plan to do so 

**EXPLAIN (before other command)** - Similar to describe, also displays general costliness of the particular function