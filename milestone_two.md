```yaml
milestone:
    iteration: 02
    title: "Design and Design Patterns"
    date: "March 05, 2021"
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
- **Vincent Cheng**
    - _Documentarian_
- **Amina Mahmood**
    - _Code Reviewer_
- **Dishant Mishra**
    - _Software Architect_
- **Aaron Wade Parker**
    - _Configuration Manager_
- **Edward Riley**
    - _Team Coordinator_


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
- A day is between 12:00 PM - 11:59 AM.
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
- GitHub
    - GitHub URL: https://github.com/europa-report 

## Design Patterns
- **Model, View, Controller (MVC)**
  - Model (Nodejs) is responsible for represent data.
  - Controller (Nodejs) is responsible for manipulation of data.
  - View (React) displays data to the GUI.
- **Single Page Application (SPA)**
  - The single page application design pattern will fit all the interactives and swapping data will be in a single page.
- **Proxy**
  - This proxy design pattern will be using python as proxy to retrieve data from Reddit's api.
- **Observer**
  - The observer design pattern will be using socket.io and react hook as event listener.
- **Compostion**
  - The composition design pattern will be using the React's Component to generate another component.


## Timeline

| Milestones                               | Planned Meeting Date | Start         | Deadline     |
|------------------------------------------|----------------------|---------------|--------------|
| Milestone 01 - Requirements              | Feb 5, 2021          | Feb 5, 2021   | Feb 12, 2021 |
| Milestone 02 - Design & Design Patterns  | Mar 4, 2021          | Mar 2, 2021   | Mar 5, 2021  |
| Milestone 03 - Layering                  | Mar 10, 2021         | Mar 10, 2021  | Mar 12, 2021 |
| Milestone 04 - Exception Handling        | Mar 24, 2021         | Mar 24, 2021  | Mar 26, 2021 |
| Milestone 05 - Performance & Refactoring | Apr 7, 2021          | Apr 7, 2021   | Apr 9, 2021  |
| Milestone 06 - Testing                   | Apr 21, 2021         | Apr 21, 2021  | Apr 23, 2021 |
| Milestone 07 - Deploying & Packaging     | Apr 28, 2021         | Apr 28, 2021  | Apr 30, 2021 |
--------------------------------------------------------------------------------------------------

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

Our overall goal is to make a new facade for Reddit with archival features and a better but with selected subreddit communities, more uniform API. This is how we plan to accomplish it:

* ~~Goal #1: Accumulate and track the numbers of the subreddit communities from the beginning of semester to the end of the semester by each day.~~
* Revised Goal #1: Each member of the group will select the 2 subreddit communities to use for this course.
* Goal #2: Accumulate and track the numbers of the users in the selected subreddit communities from the beginning of semester to the end of the semester by each day.
* Goal #3: Accumulate and track the numbers of the posts in the selected subreddit communities from the beginning of semester to the end of the semester by each day.
* Goal #4: Identify the factors supporting the growth or decline of selected subreddit communities.
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
