# Comment-Robert

## Overview

The **CommentR Interaction Dataset** is a large-scale collection of human-LLM interactions from Weibo, focusing on posts where users actively mention the LLM agent account `@CommentR`. The dataset enables research into user engagement patterns, demographic traits, and language behaviors in real-world public interactions with a social media AI agent.

## Data Collection

* **Time Span:**

  * Collected from December 1, 2023 to April 30, 2025
  * CommentR was launched on December 8, 2023
  * Data collection began in March 2024, backfilling earlier data, and was updated monthly
* **Collection Method:**

  * Queried Weibo Search for posts containing `@CommentR`
  * 1-second delay between requests to avoid server overload

## Dataset Scale and Demographics

* **Total posts mentioning `@CommentR`:** 557,645

* **Unique users:** 304,400

* **Reply statistics:**

  * 298,469 posts received at least one reply
  * 1,033,505 total replies (from both CommentR and human users)

## Data Structure

Each record in the dataset includes:

| Attribute     | Description                                                                                                                   |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| User profile  | User ID, nickname, profile photo URL, account type (verified/unverified)                                                      |
| Post metadata | Post ID, creation time, client device, IP location, likes/comments/retweets, flags for long text, retweet, and attached media |
| Content       | Full text of the post                                                                                                         |

## Citation


