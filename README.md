# FInd-A-Fan
Hackathon project for the Chirp Developer Challenge

## [Problem](https://chirpdevchallenge.devpost.com/?utm_source=devpost&utm_medium=alert&utm_campaign=20220624_allinterest)

Help us unlock new experiences for people on Twitter, and inspire other developers. We want to push the boundaries of what’s possible with our platform. We need your help to bring to life the experiences that will define this new frontier.

Build an app using the Twitter API v2 in one of the following categories:

- Content discovery apps
- Conversation safety tools
- Public good apps

## Proposal 

Have you ever been on a trip, away from your home-base bar, while your team is playing in a big game? Or maybe you are just new and town and looking for a bar with comrade fans as crazy as you are. Either way, what you are missing is our Find-a-fan twitter service. 

This application will be designed to query Twitter's tweets and metadata to find you the best restarants and bars to catch the game with fellow fans. You provide it with a city and a sports team and we do the rest.

All you have to do is show up with your best jersey on.

## Specs

### Team
- Colin Mills
- Matt Lieb
- Veeral Suthar
- Michah Griffin

[_Join us!_](https://devpost.com/software/464930/joins/kLh-GhP8YISD0kRDOZUDnQ)

### Content Discovery App Requirements

Help people discover content such as Lists, Spaces, or Tweets, on Twitter. We have built an open platform that allows you to give people more opportunities to discover content that’s relevant to them. While we built some discovery experiences ourselves (such as the Explore tab for Spaces), people will benefit from alternative discovery mechanisms that can complement ours or be an alternative to them. Another element of discovery is the ability to create different perspectives of the public conversation. Twitter’s developer platform enables you to build ways to filter content by a particular set of rules (for example, a specific topic), or to only surface content in a particular context (such as time of day). You can build tools to show relevant content based on those circumstances, such as apps that surface work-related content during the week, and fun content during the weekend.

Must use at least one of the following Twitter API v2 endpoints; 

1. [Bookmarks](https://developer.twitter.com/en/docs/twitter-api/tweets/bookmarks/introduction)
2. [Search](https://developer.twitter.com/en/docs/twitter-api/tweets/search/introduction)
3. [Spaces](https://developer.twitter.com/en/docs/twitter-api/spaces/overview)
4. [Manage Tweets](https://developer.twitter.com/en/docs/twitter-api/tweets/manage-tweets/introduction)
5. [Lists](https://developer.twitter.com/en/docs/twitter-api/lists/manage-lists/introduction)
6. [Timelines](https://developer.twitter.com/en/docs/twitter-api/tweets/timelines/introduction)
7. [Filtered Stream](https://developer.twitter.com/en/docs/twitter-api/tweets/filtered-stream/introduction)

### Design Summary

This project will require front-end and back-end development. 

#### Languages
Likely mostly Python.

#### User end-point
The customer will interact with our program with some sort of deployed, web-based end point. We could make this either a web page, or an app. Another idea, depending on if we actually need to build the front end is to have the user interact with this program by tagging it in a tweet. With this approach, we would have our application scan for mentions every x minutes and use that tweet to build the query. This would be cool because it uses Twitter's existing front-end and would provide a central location for fans to connect with each other and see past results.

_Example 1: The user opens and app and sees a search bar with two fields. The first field has a drop down for cities, the second prompts for a team name. Once the user submits a query, it will display the results in a table._

_Example 2: The user posts this tweet, "Hey @Find-a-fan I am in NYC looking to catch the Broncos NFL game, can you help a guy out?" A few minutes later a response to this tweet will come from our twitter page with the best 5 places to catch the game._

#### Query Listener
Regardless of the front-end UI, we will need some program to be periodically scanning or listening for a query to be submitted. Once this is triggered it could pass off the information to the query runner in a new thread.

#### Query Runner
This will take in the query information from the listener, build a new API rest query (or a series of them), and send out the request(s). It will receive this data, analyze it, format it, and pass it off to our Query Response class.

This will be the meat of our program here. I imagine there won't be too much data directly mentioning both the exact name of a sports team **and** a restaurant. To find more tweets related to a sports team I think we should design some sort of fuzzy search function that compiles a dictionary of words that could be related to the team. For example, it would populate with the team name, mascot, close mis-spellings or other slang, and even players' and coachs' names. We will use geolocation to restrict the location of these tweets to radius around a metro area.

Once we have a decently sized search set, we can find restaurants and bars by direct mentions, tags, or even geo-location hot spots.

#### Query Response
This will take in a either raw data or a pre-formatted response and either post a response in Twitter or on our app.


### Sequence Diagram

### Component Diagram

### TODO
#### Design
#### Font-end
#### Back-end
#### Deployment
#### Testing

