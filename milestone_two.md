```yaml
milestone:
    iteration: 01
    title: "Design and Design Patterns"
    date: "March 2, 2021"
group:
    number: 03
    name: "Europa Report"
    members:
    - "Vincent Cheng"
    - "Amina Mahmood"
    - "Dishant Mishra"
    - "Aaron Wade Parker"
    - "Edward Riley"
```

# Development Book

## Team Members and Roles
- **Amina Mahmood**
    - _Code Reviewer_
- **Aaron Wade Parker**
    - _Configuration Manager_
- **Dishant Mishra**
    - _Software Architect_
- **Edward Riley**
    - _Team Coordinator_
- **Vincent Cheng**
    - _Documentartian_

## Background
Reddit is a social news aggregation, web content rating, and discussion website, recently including livestream content through Reddit Public Access Network. Registered members submit content to the site such as links, text posts, and images, which are then voted up or down by other members. A subreddit is a specific online community, and the posts associated with it, on the social media website Reddit. Subreddits are dedicated to a particular topic that people write about, and they're denoted by /r/, followed by the subreddit's name, e.g., /r/gaming.

## Project Description
The project serves to provide a statistical analysis to show the increase or decline of subreddit and content information per day. The project will assist us with the conclusion of whether the online presence on the Internet communities are growing or reducing per day.

## Project Requirement
- 24/7 Shared Server
- Relational Database 
- API Queries
- Object-Oriented Programming Language 

## Business Rules
- A day is between 12:00 PM - 11:59 AM
- Cron's job execute python file to retrieve data from Reddit's api.
- Store to the local database.
- User load up the webpage, Nodejs load data to the React's component.
- User Interface will display the chart of datas.



## Technologies Used
- Serverside Layers
    - Data Layer
      - **MySQL/MariaDB**
    - Business Layer
      - **NodeJS**
      - **ExpressJS**
- Client side 
    - Prensentation Layer
      -  **React.js** (Frontend Framework) 

## Design Patterns
- **Model, View, Controller (MVC)**
  - Model(Nodejs): responsible for represent data.
  - Controller(Nodejs): responsible for manipulation of data.
  - View(React): display data to the gui.
- **Single Page Application (SPA)**
  - All the interactives and swapping data will be in a single page.
- **Proxy**
  - Will be using python as proxy to retrieve data from Reddit's api.
- **Observer**
  - Using socket.io and react hook as event listener.
- **Compostion**
  - Using React's Component to generate another component.
## Timeline

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

## Tech stack

* ReactJS
* NodeJS
* ExpressJS
* MySQL/MariaDB
* Python
