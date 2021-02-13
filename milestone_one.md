```yaml
milestone:
    iteration: 01
    title: "requirements"
    date: "February 12, 2021"
group:
    number: 03
    name: "Europa Report"
    members:
    - "Amina Mahmood"
    - "Aaron Wade Parker"
    - "Dishant Mishra"
    - "Edward Riley"
    - "Vincent Cheng"
```

## Glossary

* __Subreddit__ - A Subreddit is a sub community within Reddit. It usually follows a well-defined theme and people interested in the topic/theme can join it to share content with other members of the community.

* __Redditor__ - A Reddit user.

* __Upvote__ - It is vote used to show agrrement with a comment or a post.

* __Downvote__ - A vote used to show disagreement with a comment or a post.

* __Comment__ - A response to a post or another comment.

* __Post__ - A post constitutes one of the following: A link to an external source, a crosspost which links to another post, rich media, or pain text.


## Current System

Reddit in its current form can be rather infuriating to use. Any edit made to a comment or a post is hidden and the original content cannot be seen again. It is also hard to visualize a lot of user generated data like votes due to Reddit's various obfuscation rules on it's frontend. It's API is also very cluttered and hard to use for the purpose of research.


## Goals

Our goal is to make a new facade for Reddit with archival features and a better, more uniform API. This is how we plan to accomplish it:

* Goal #1: Accumulate and track the numbers of the subreddit  communities from the beginning of semester to the end of the semester by each day.
* Goal #2: Accumulate and track the numbers of the users from the beginning of semester to the end of the semester by each day.
* Goal #3: Accumulate and track the numbers of the posts communities  from the beginning of semester to the end of the semester by each day.
* Goal #4: Identify the factors supporting the growth or decline of subreddit communities.
* Goal #5: Create a consistent realtime data visualiztion.


## Stakeholders

* Data scientists
    * We plan to tailor our exposed API and front-end to fit the needs of people in this field so minimal work is required to extract relevant information.


## Scope

* An ETL script that will fetch data from reddit every day.
* A NodeJS backend for our API to connect to the database.
* A ReactJS front-end for users to interact with the API.


## Anticipated Input

* JSON


## Processing

* A diff utility will be used to create low cost archives of content in our database.

* Any user input will be cleaned and standardized in accordance with Reddit's markdown before being stored in our database.

* Searches will be based on time, tags, and votes.



## Anticipated Output

* JSON


## Data Sources

* [Reddit API](https://www.reddit.com/dev/api/) 

## Tech Stack

* ReactJS
* NodeJS
* ExpressJS
* MySQL/MariaDB
* Python
