# FInd-A-Fan
Hackathon project for the Chirp Developer Challenge

## Problem

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

#### Customer end-point
The customer will interact with our program with some sort of deployed, web-based end point. We could make this either a web page, or an app. Another idea, depending on if we actually need to build the front end is to have the user interact with this program by tagging it in a tweet. With this approach, we would have our application scan for mentions every x minutes and use that tweet to build the query. This would be cool because it uses Twitter's existing front-end and would provide a central location for fans to connect with each other and see past results.

_Example 1: The user opens and app and sees a search bar with two fields. The first field has a drop down for cities, the second prompts for a team name. Once the user submits a query, it will display the results in a table.

_Example 2: The user posts this tweet, "Hey @Find-a-fan I am in NYC looking to catch the Broncos NFL game, can you help a guy out?" A few minutes later a response to this tweet will come from our twitter page with the best 5 places to catch the game. 

### Activity Diagram

### Component Diagram

### TODO

#### Font-end
-[ ]
-[ ]
#### Back-end
-[ ]
-[ ]
