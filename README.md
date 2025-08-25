# Comment-Robert

## Overview

The **CommentR Interaction Dataset** is a large-scale collection of human-LLM interactions from Weibo, focusing on posts where users actively mention the LLM agent account `@CommentR`. This dataset contains **557,645** posts, along with the corresponding **304,400** unique users and all related comments, enabling research into user engagement patterns, demographic traits, and language behaviors in public interactions with a social media AI agent.

Here's a sample dataset containing 1,000 posts, along with their associated users and comments, available directly in this repository.

The full dataset can be accessed via [Google Drive](https://drive.google.com/file/d/1mqXO9mLObt2UcMa8y9ZPvfPuwRBaiSyS/view?usp=sharing). 

Please apply for access by contacting [skgu24@m.fudan.edu.cn](skgu24@m.fudan.edu.cn) or [yjyin24@m.fudan.edu.cn](skgu24@m.fudan.edu.cn) with your **institutional email address** and clearly **state your institution**, your **research advisor (if any)**, and your use case of **CommentR Interaction Dataset**.

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
| User profile    | User ID, nickname, avatar URL, verification status, bio, followers/friends count, statuses count, gender, location, membership rank/type, birthday, account creation time, IP location, sunshine credit, label description |
| Post metadata    | Post ID, mblogid, creation time, geo, IP location, reposts count, comments count, likes count, source, content, image URLs/number, isLongText, is_retweet, user info|
| Comment metadata | Comment ID, root post ID, root comment ID, creation time, likes count, IP location, content, comment user info, replied comment info (if exists)|




## Data Sample

### users.json
```json
{
    "_id": "db8a21761a96b75c86eec09bb46adf7a",
    "avatar_hd": "https://tvax2.sinaimg.cn/crop.0.0.512.512.1024/007OtLHVly8hag5b1x4i1j30e80e83z0.jpg?KID=imgbed,tva&Expires=1728599961&ssig=HrDFcBRqIk",
    "nick_name": "df9f8405e90dfa096f1866b7a4705047",
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
    "desc_text": "",
    "ip_location": "IP属地：上海",
    "sunshine_credit": "信用极好",
    "label_desc": [
        "视频累计播放量1.9万"
    ]
}
```
### posts.json 
```json
{
    "_id": "80a68086e638dc9eff231c2578e728aa",
    "mblogid": "8c24aa33e83fb3aed96fa8172f70c911",
    "created_at": "2025-01-11 21:50:32",
    "geo": null,
    "ip_location": "发布于 浙江",
    "reposts_count": 0,
    "comments_count": 3,
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
        "_id": "a9144436e7594f5e5c39ddcb24ef8097",
        "avatar_hd": "https://tvax2.sinaimg.cn/crop.0.0.1080.1080.1024/9c24ca47ly8hmbfx2bhv5j20u00u079d.jpg?KID=imgbed,tva&Expires=1746493182&ssig=6O4TqfBWoF",
        "nick_name": "369ea88d6dfb04ef113ebf1f0d6785d3",
        "verified": false,
        "mbrank": 3,
        "mbtype": 2
    },
    "likes_count": 12
}
```
### comments.json
```json
{
    "created_at": "2024-01-04 20:51:35",
    "_id": "3ef5e62367423d72a89b5a71704155e6",
    "ip_location": "来自湖南",
    "content": "怎么不愿意可恶",
    "comment_user": {
        "_id": "e1225d5574a287bff8a3b342ef633963",
        "avatar_hd": "https://tvax2.sinaimg.cn/crop.0.0.1080.1080.1024/008utg7kly8hts5dbp5v8j30u00u0n00.jpg?KID=imgbed,tva&Expires=1727493599&ssig=pLLJJu%2Bo4w",
        "nick_name": "9c5796d494700d20b9e2034ad9dbf927",
        "verified": true,
        "description": "点进我主页默认你点进我主页",
        "followers_count": 13996,
        "friends_count": 2915,
        "statuses_count": 17107,
        "gender": "f",
        "location": "海外",
        "mbrank": 6,
        "mbtype": 12,
        "verified_type": 0,
        "verified_reason": "微博原创视频博主"
    },
    "reply_comment": {
        "_id": "4ce4b22f1a2594415087bb5ee626d102",
        "text": "[偷笑][偷笑]",
        "user": {
            "_id": "7d25da456dd4d0ec9fc69b54073a9679",
            "avatar_hd": "https://tvax3.sinaimg.cn/crop.0.0.1080.1080.1024/007EUKxsgy1hu2hzozkzkj30u00u0gov.jpg?KID=imgbed,tva&Expires=1727493599&ssig=YzORDJhcRX",
            "nick_name": "718707e73d537ccc39399d7022ff47d4",
            "verified": true,
            "description": "只要你开心这条路怎么走都是对的",
            "followers_count": 39375,
            "friends_count": 1925,
            "statuses_count": 6401,
            "gender": "f",
            "location": "重庆",
            "mbrank": 1,
            "mbtype": 12,
            "credit_score": 80,
            "created_at": "2019-03-02 15:14:12",
            "verified_type": 0,
            "verified_reason": "超话粉丝大咖（徐璐超话） 超话粉丝大咖（徐艺洋超话）"
        }
    },
    "root_comment_id": "4ce4b22f1a2594415087bb5ee626d102",
    "root_post_mblogid": "6f9edc9c490c8ed693ae99bb5fd32ab3",
    "likes_count": 0
}
```

## Citation


