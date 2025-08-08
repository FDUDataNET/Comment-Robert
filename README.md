# Comment-Robert

## Overview

The **CommentR Interaction Dataset** is a large-scale collection of human-LLM interactions from Weibo, focusing on posts where users actively mention the LLM agent account `@CommentR`. This sample dataset contains 1,000 posts, along with the corresponding users and all related comments, enabling research into user engagement patterns, demographic traits, and language behaviors in public interactions with a social media AI agent.

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

  * 298,173 posts received at least one reply
  * 1,028,364 total replies (from both CommentR and human users)

## Data Structure

Each record in the dataset includes:

| File          | Attributes                                                                 |
| ------------- | -------------------------------------------------------------------------- |
| users.json    | User ID, nickname, avatar URL, verification status, bio, followers/friends count, statuses count, gender, location, membership rank/type, birthday, account creation time, IP location, sunshine credit, label description |
| posts.json    | Post ID, mblogid, creation time, geo, IP location, reposts count, comments count, likes count, source, content, image URLs/number, isLongText, is_retweet, user info, post URL, keyword |
| comments.json | Comment ID, root post ID, creation time, likes count, IP location, content, comment user info, replied comment info |


## Data Sample

### users.json
```json
{
    "_id": "7158841527",
    "avatar_hd": "https://tvax2.sinaimg.cn/crop.0.0.512.512.1024/007OtLHVly8hag5b1x4i1j30e80e83z0.jpg",
    "nick_name": "小霖月要开心",
    "verified": false,
    "description": "震魂",
    "followers_count": 1518,
    "friends_count": 607,
    "statuses_count": 932,
    "gender": "f",
    "location": "山西",
    "mbrank": 3,
    "mbtype": 2,
    "birthday": "天秤座",
    "created_at": "2019-05-24 23:53:19",
    "ip_location": "IP属地：上海",
    "sunshine_credit": "信用极好",
    "label_desc": ["视频累计播放量1.9万"]
}

### posts.json 
```json
{
    "_id": "5121748373090268",
    "mblogid": "P97M1cXV2",
    "created_at": "2025-01-11 21:50:32",
    "geo": null,
    "ip_location": "发布于 浙江",
    "reposts_count": 0,
    "comments_count": 3,
    "attitudes_count": 12,
    "source": "iPhone 14",
    "content": "#评论罗伯特总结我的2024# @评论罗伯特 总结我的2024 ",
    "pic_urls": [
        "https://wx1.sinaimg.cn/orj960/9c24ca47gy1hxh5r0mq5pj22c03404qq",
        "https://wx1.sinaimg.cn/orj960/9c24ca47gy1hxh5r1xww8j23402c0b2a",
        "https://wx1.sinaimg.cn/orj960/9c24ca47gy1hxh5rs3osvj22sn253kjo"
    ],
    "pic_num": 3,
    "isLongText": false,
    "is_retweet": false,
    "user": {
        "_id": "2619656775",
        "avatar_hd": "https://tvax2.sinaimg.cn/crop.0.0.1080.1080.1024/9c24ca47ly8hmbfx2bhv5j20u00u079d.jpg",
        "nick_name": "Doing_W_W",
        "verified": false,
        "mbrank": 3,
        "mbtype": 2
    },
    "url": "https://weibo.com/2619656775/P97M1cXV2",
    "keyword": "@评论罗伯特"
}

### comments.json
```json
{
    "root_tweet_id": "NAjTd4i2B",
    "created_at": "2024-01-04 20:51:35",
    "_id": 4986562862911462,
    "rootid": 4986562762251608,
    "like_counts": 0,
    "ip_location": "来自湖南",
    "content": "怎么不愿意可恶",
    "comment_user": {
        "_id": "7779326206",
        "avatar_hd": "https://tvax2.sinaimg.cn/crop.0.0.1080.1080.1024/008utg7kly8hts5dbp5v8j30u00u0n00.jpg",
        "nick_name": "海島拾薇札記",
        "verified": true
    },
    "reply_comment": {
        "_id": 4986562762251608,
        "text": "[偷笑][偷笑]",
        "user": {
            "_id": "7017508530",
            "avatar_hd": "https://tvax3.sinaimg.cn/crop.0.0.1080.1080.1024/007EUKxsgy1hu2hzozkzkj30u00u0gov.jpg",
            "nick_name": "-xuan宣-",
            "verified": true
        }
    }
}


## Citation


