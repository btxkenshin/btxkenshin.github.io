# heihei_server #

# v 2.0.0

### IM消息类型

 1. 消息字段

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|tips| 默认不支持的消息提示 | |
|msgtype| 消息类型 | **text\|audio\|gift\|systopic\|dueChat\|sysnotify\|image\|video** |
|content| 消息正文 | |
|jump| 跳转链接 | |
|img| 图片地址 | |
|icon| 小图标地址 | |

 2. 消息类型

* text 文本消息

```json?linenums
{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "text",
        "content": {
          "text": "hello word!"
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【文本消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
    }
```

* systopic 

```json?linenums
{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "systopic",
        "content": {
          "text": "#有试过同时跟两个人交往吗#"
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【系统消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
    }
```

* audio

```json?linenums
{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "audio",
        "content": {
          "audio": "http://cdn.wmlives.com/record/2017-03-04/50_995b139c-ba50-4525-8b35-29815edfb6c9.m4a",
          "length": 15
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【声音消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
    }
```

* gift

```json?linenums
{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "gift",
        "content": {
          "text": "我送你kiss雨",
          "giftId": 113
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【礼物消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
    }
```


* dueChat

```json?linenums
{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "dueChat",
        "content": {
          "chatStatus": 1,
          "chatLength": 1200
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【约聊消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
}
```

>约聊消息需要客户端做特殊处理，根据**fromUserId**显示不一样的文案。

* sysnotify

```json?linenums
{
    "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "sysnotify",
        "content": {
          "text": "我在话题#接口对接#里给你送了小花花，",
          "img": "http://cdn.wmlives.com/static/img/heihei/gift/gift-5.png",
          "icon": "http://cdn.wmlives.com/static/img/heihei/gift/105_icon.png"
        },
        "jump": {
          "text": "查看",
          "link": "wmlivesheihei://topic/1111"
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【通知消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
    }
}

{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "sysnotify",
        "content": {
          "text": "我在话题#接口对接#里给你点赞了，",
          "img": "http://cdn.wmlives.com/static/img/heihei/gift/gift-5.png"
        },
        "jump": {
          "text": "查看",
          "link": "wmlivesheihei://topic/1111"
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【通知消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
    }
```


* image

```json?linenums
{   
    "msgType": "IM",
     "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "image",
        "content": {
          "img": "http://cdn.wmlives.com/static/img/heihei/gift/gift-5.png"
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【图片消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
}
```

* video

```json?linenums
{
      "msgType": "IM",
      "msg": {
        "toUserId": 10034,
        "fromUserId": 10045,
        "msgType": "video",
        "content": {
          "video": "http://he.yinyuetai.com/uploads/videos/common/8811015A2320B1AD2B3DBE8A431ED2E3.mp4"
        },
        "msgId": 1234567890123456,
        "createTime": 1348831860,
        "tips": "【视频消息】不支持的消息类型，请升级最新客户端。"
      },
      "users": {
        "10045": {
          "id": 10032,
          "displayName": "",
          "heiNum": "",
          "coverUrl": "",
          "level": 0,
          "gender": "",
          "honours": [],
          "isFollowed": false
        }
      }
}
```

### 获取用户配置和其他服务端设置数据

* URL

`getConfig:/api/user/get-config` 

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |

  
* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|countings| 帖子或回复的计数数据 | |

* Error Response

    `700:参数错误`
    `720:token无效`
    `TODO`
    ``
    
* data

```json?linenums
{
    errorcode：0,
    errormsg:"success",
    configuration:{
       user:{
       
       },
       sys:{
        
       }
    }
}
```

### 拉取单个subject的数据

* URL

`getSubject:/api/topic/get-subject` 
**Method:POST**

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| subjectId |        |   int   |      | Y     |      |

  
* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|countings| 帖子或回复的计数数据 | |

* Error Response

    `700:参数错误`
    `720:token无效`
    `TODO`
    ``
    
* data

```json?linenums
{
    errorcode：0,
    errormsg:"success",
    subject:{
          "id":123,
          "replyText":"",
          "replyPath":"",
          "replyLength":12,
          "samples":"[2,3,44,5,0,0,2,3]",
          "topicId":122,
          "replyId":12,
          "replyUserId":10045,
          "creatorId":10032
          "timeTip":"2分钟前",
          "isLike":true,
          "countings":{
              "viewCount": 0,
              "replyCount": 0,
              "likeCount": 0,
              "giftCount":0
          }
    },
    users:{
        "10032":{
            "id": 10032,
            "displayName": "",
            "heiNum": "",
            "coverUrl": "",
            "level": 0,
            "birthDay": "",
            "gender": "",
            "honours": [],
            "isFollowed":false
        },
        "10045":{
            "id": 10045,
            "displayName": "",
            "heiNum": "",
            "coverUrl": "",
            "level": 0,
            "birthDay": "",
            "gender": "",
            "honours": [],
            "isFollowed":false
        }
    }
}
```


### 参与话题

* URL

`createSubject:/api/topic/create-subject` 
**Method:POST**

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| topicId |        |   int   |      | Y     |      |
| sign |        |   string   |      | Y     |  上传的文件签名  |
| samples |        |  string |      | Y     |  文件采样    |
| title |        |  string |      | Y     |  标题    |
| length |        |  int |      | Y     |  长度    |

  
* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|| ||
|| ||

* Error Response
    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    `100：话题或帖子不存在`
    `102:文件验证失败`
    
* data

```json?linenums
{
  "errorcode": 0,
  "errormsg": "success",
  "users": {
    "41": {
      "displayName": "相坤手机号",
      "level": 1,
      "gender": "Female",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-8-108.png",
      "heiNum": 1000134,
      "birthDay": "2016-03-25",
      "honours": [],
      "id": 41,
      "isFollowed": false
    }
  },
  "subject": {
    "topicId": 3,
    "countings": {
      "viewCount": 0,
      "replyCount": 0,
      "giftCount": 0,
      "likeCount": 0
    },
    "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
    "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
    "id": 14,
    "replyUserId": 0,
    "title": "非阿什顿飞111",
    "createTime": "2017-03-10 18:30:30",
    "length": 5,
    "mainSubjectId": 0,
    "replySubjectId": 0,
    "creatorId": 41
  }
}
```

### 回复

* URL

`replySubject:/api/topic/reply-subject` 
**Method:POST**

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| subjectId |        |   int   |      | Y     |      |
| sign |        |   string   |      | Y     |  上传的文件签名  |
| samples |        |  string |      | Y     |  文件采样    |

  
* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|| ||
|| ||

* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    `100：话题或帖子不存在`
    `102:文件验证失败`
    
* data

```json?linenums
{
    errorcode：0,
    errormsg:"success",
    subject:{
          "id":123,
          "replyText":"",
          "replyPath":"",
          "replyLength":12,
          "samples":"[2,3,44,5,0,0,2,3]",
          "topicId":122,
          "replyId":12,
          "replyUserId":10045,
          "creatorId":10032
          "timeTip":"2分钟前",
          "isLike":true,
          "countings":{
              "viewCount": 0,
              "replyCount": 0,
              "likeCount": 0,
              "giftCount":0
          }
    },
    users:{
        "10032":{
            "id": 10032,
            "displayName": "",
            "heiNum": "",
            "coverUrl": "",
            "level": 0,
            "birthDay": "",
            "gender": "",
            "honours": [],
            "isFollowed":false
        },
        "10045":{
            "id": 10045,
            "displayName": "",
            "heiNum": "",
            "coverUrl": "",
            "level": 0,
            "birthDay": "",
            "gender": "",
            "honours": [],
            "isFollowed":false
        }
    }
}
```

### 修改话题

* URL

`updateSubject:/api/topic/update-subject`
**Method:POST**

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| subjectId |        |int  |      | Y     |      |
| title |        |string  |      | Y     |      |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|| ||
|| ||

* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**

    
* data

```json?linenums
{
    errorcode：0,
    errormsg:"success",
    subject:{
          "id":123,
          "replyText":"",
          "replyPath":"",
          "replyLength":12,
          "samples":"[2,3,44,5,0,0,2,3]",
          "topicId":122,
          "replyId":12,
          "replyUserId":10045,
          "creatorId":10032
          "timeTip":"2分钟前",
          "isLike":true,
          "countings":{
              "viewCount": 0,
              "replyCount": 0,
              "likeCount": 0,
              "giftCount":0
          }
    },
    users:{
        "10032":{
            "id": 10032,
            "displayName": "",
            "heiNum": "",
            "coverUrl": "",
            "level": 0,
            "birthDay": "",
            "gender": "",
            "honours": [],
            "isFollowed":false
        },
        "10045":{
            "id": 10045,
            "displayName": "",
            "heiNum": "",
            "coverUrl": "",
            "level": 0,
            "birthDay": "",
            "gender": "",
            "honours": [],
            "isFollowed":false
        }
    }
}
```


### 收听帖子

* URL

`listenSubject: /api/topic/listen-subject`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| subjectId  |        | int |      | Y     |      |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|| ||
|| ||

* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    `100：话题或帖子不存在`
    
* data

``` json?linenums
{
  "errorcode": 0,
  "errormsg": "success",
  "subjectCountings": {
    "viewCount": "5",
    "replyCount": 0,
    "subjectId": 14,
    "giftCount": 0,
    "likeCount": 0
  },
  "topicCountings": {
    "viewCount": "15",
    "topicId": 3,
    "replyCount": "2",
    "likeCount": 0
  }
}
```


### 帖子点赞

* URL

`likeSubject:/api/topic/like-subject`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| subjectId     |        | int |      | Y     |      |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|| ||
|| ||

* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    ``
    
* data

``` json?linenums
{
  "errorcode": 0,
  "errormsg": "success",
  "subjectCountings": {
    "viewCount": "5",
    "replyCount": 0,
    "subjectId": 14,
    "giftCount": 0,
    "likeCount": 0
  },
  "topicCountings": {
    "viewCount": "15",
    "topicId": 3,
    "replyCount": "2",
    "likeCount": 0
  }
}
```


### 话题详情页

* URL

`topicDetail:/api/topic/topic-detail`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| type      |        | string| 0:hot,1:new| Y     |      |
| offset    |        | int    |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|| ||
|| ||

* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    `100：话题或帖子不存在`
    
* data

```json?linenums

{
  "errormsg": "success",
  "errorcode": 0,
  "topic": {
    "countings": {
      "viewCount": 0,
      "replyCount": 0,
      "likeCount": 0
    },
    "name": "话题222",
    "img": "http://ycl-bucket-01.oss-cn-beijing.aliyuncs.com/static/img/heihei/banner/20170101.png",
    "content": "瞎聊下吧",
    "catName": "瞎聊",
    "isTop": 0,
    "type": 0,
    "id": 3
  },
  "users": {
    "41": {
      "displayName": "相坤手机号",
      "level": 1,
      "gender": "Female",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-8-108.png",
      "heiNum": 1000134,
      "birthDay": "2016-03-25",
      "honours": [],
      "id": 41,
      "isFollowed": false
    }
  },
  "pageSize": 11,
  "subjects": [
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "非阿什顿飞111",
      "creatorId": 41,
      "createTime": "2017-03-10 18:30:30",
      "length": 5,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 14,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:24:57",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 13,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:23:10",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 12,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:22:06",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 11,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:21:12",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 10,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:18:41",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 9,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:16:58",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 8,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:16:40",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 7,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:16:14",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 6,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:13:08",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 5,
      "isLike": false
    },
    {
      "topicId": 3,
      "repliesTotal": 0,
      "countings": {
        "viewCount": 0,
        "replyCount": 0,
        "giftCount": 0,
        "likeCount": 0
      },
      "replyUserId": 0,
      "title": "hello",
      "creatorId": 41,
      "createTime": "2017-03-10 18:11:05",
      "length": 14,
      "mainSubjectId": 0,
      "replySubjectId": 0,
      "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
      "replies": [],
      "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
      "id": 4,
      "isLike": false
    }
  ],
  "offset": 11
}
```



### 帖子详情

* URL

`subjectDetail:/api/topic/subject-detail`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| subjectId     |        | int |      | Y     |      |
| offset     |        | int |      | Y     |      |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|   |       |   |
|   |       |   |

* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    `100：话题或帖子不存在`

* data

```json?linenums
{
    errorcode： 0，
    errormsg: "",
        topic: {
            "name": "约聊专区",
            "img": "beijing.aliyuncs.com/static/img/heihei/banner/20170101.png",
            "content": "营同学人工后台改变顺序、置顶",
            "catName": "约聊专区",
            "isTop": 0,
            "type": 0,
            "id": 2,
            "countings": {
                "replyCount": 0,
                "viewCount": 0,
                "likeCount": 0
            }
            shareInfo: {}
        },
        subject: {
            "topicId": 3,
          "repliesTotal": 0,
          "countings": {
            "viewCount": 0,
            "replyCount": 0,
            "giftCount": 0,
            "likeCount": 0
          },
          "replyUserId": 0,
          "title": "hello",
          "creatorId": 41,
          "createTime": "2017-03-10 18:11:05",
          "length": 14,
          "mainSubjectId": 0,
          "replySubjectId": 0,
          "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
          "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
          "id": 4,
          "isLike": false,
          "shareInfo":{
            
          }
        },
        pageSize: 20,
        "replys": [{
            "topicId": 3,
          "repliesTotal": 0,
          "countings": {
            "viewCount": 0,
            "replyCount": 0,
            "giftCount": 0,
            "likeCount": 0
          },
          "replyUserId": 0,
          "title": "hello",
          "creatorId": 41,
          "createTime": "2017-03-10 18:11:05",
          "length": 14,
          "mainSubjectId": 0,
          "replySubjectId": 0,
          "samples": "1,2,3,4,5,6,7,66,45,32,34,98,44,3,2,33,0",
          "path": "http://cdn.wmlives.com/data/record/2017031017_41_nwFo6TAXa4.mp3",
          "id": 4,
          "isLike": false,
          "shareInfo":{
            
          }
        }],
        users: {
            "10032": {
                "id": 10032,
                "displayName": "",
                "heiNum": "",
                "coverUrl": "",
                "level": 0,
                "birthDay": "",
                "gender": "",
                "honours": [],
                "isFollowed": false
            },
            "10045": {
                "id": 10045,
                "displayName": "",
                "heiNum": "",
                "coverUrl": "",
                "level": 0,
                "birthDay": "",
                "gender": "",
                "honours": [],
                "isFollowed": false
            }
        }
}

```



### 黑聊列表topic-list

* URL

 `topicList:/api/topic/topic-list`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| offset     |        | int |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|type| 话题类型| 0：普通 1：约聊|
|content| 内容| |
|isTop| 是否置顶| |


* Error Response

   **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    ``
    
* data


```json?linenums
{
    "errorcode": 0,
    "errormsg": "success",
    "dueChat": {
        topic: {
            "name": "约聊专区",
            "img": "beijing.aliyuncs.com/static/img/heihei/banner/20170101.png",
            "content": "营同学人工后台改变顺序、置顶",
            "catName": "约聊专区",
            "isTop": 0,
            "type": 0,
            "id": 2,
            "countings": {
                "replyCount": 0,
                "viewCount": 0,
                "likeCount": 0
            }
        },
        users: [
            {
                "id": 0,
                "displayName": "",
                "heiNum": "",
                "coverUrl": "",
                "level": 0,
                "birthDay": "",
                "gender": "",
                "honours": [],
                "isFollowed": false,
                "timeTip": "2分钟前"
            },
            {
                "id": 0,
                "displayName": "",
                "heiNum": "",
                "coverUrl": "",
                "level": 0,
                "birthDay": "",
                "gender": "",
                "honours": [],
                "isFollowed": true,
                "timeTip": "2分钟前"
            }
        ]
    },
    topics: [
        {
            "name": "约聊专区",
            "img": "beijing.aliyuncs.com/static/img/heihei/banner/20170101.png",
            "content": "营同学人工后台改变顺序、置顶",
            "catName": "约聊专区",
            "isTop": 0,
            "type": 0,
            "id": 2,
            "countings": {
                "replyCount": 0,
                "viewCount": 0,
                "likeCount": 0
            }
        },
        {
            "name": "话题测试",
            "img": "http://ycl-bucket-01.oss-cn-beijing.aliyuncs.com/static/img/heihei/banner/20170101.png",
            "content": "更让人悲观的，往往不是生活的艰难，而是生活的难以改变。一个人的生活，很大程度上受到家庭经济状况、接受教育程度、社会习俗、成长环境、社会大背景等等因素的制约。个人的力量与这些因素一比，太为弱小。",
            "catName": "生活",
            "isTop": 0,
            "type": 0,
            "id": 1,
            "countings": {
                "replyCount": 0,
                "viewCount": 0,
                "likeCount": 0
            }
        }
    ]
}
```


### 上传文件获取OSSTOKEN

* URL

`ossToken:/api/sys/oss-token`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| format  |        | string |  mp3,png,jepg,jpg,  | Y     |     |
| module  |        | string |'record', 'message',avatar| Y |  录音模块：record，消息：message, 头像：avator|
      
* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|Credentials| oss授权信息||
|FileInfo| 文件信息||
|path| 文件上传路径||


* Error Response

    **统一错误**
    `700:参数错误`
    `720:token无效`
    `400:业务失败`
    
    **特殊处理**
    ``

* Example

```json?linenums
{
  "errorcode": 0,
  "errormsg": "success",
  "Credentials": {
    "AccessKeySecret": "25Lgj3nKCahqq8Uqo85TJqVAJzZzSHDxC56WaC8Hc8y4",
    "SecurityToken": "CAISuwJ1q6Ft5B2yfSjIqfHtJMKAn7ts463ZVEnB0VpkSu1+26z4lDz2IHlLdHJvB+AasfU/nWBX6fcalqwqE8MbFRQS9Tn6J9cFnzm6aq/t5uZKhN5t0e9ccAr+Ihr/29CoLIedZdjBe/CrRknZnytou9XTfimjWFrXVv/sjoV8POwKQi6ybzdNGK1hRG1YpdQdKGHaONu0LxfumRCwNkdzvRdmgm4NwsaWy8aHuB3Flw+4mK1Hto/1Z5K5ZMphINInCpCv0edxbKaGinYJtEAQrPcv1psdoWuZ7uaDI2F6xha3K7CFtMFiPBNbHvFiRvAa8qKtyaIi4bWOx9TNpkwTbb0PYUP2X5u9xcbIIuStO+sieKzzU3a3iYnQZsKq7VN4PiNLbVMVJIt5MB55EQRpVSvbNqK3dNZVlpdr08EagAF/zyFvELqg7ghcUbChGFCKTtuEpeeKN/XBbifE9t4QSIR9F38n8qU+x4JZWDe9YqWDnQcTdVKEZcTdmsMlv8Hv8IK5Ckl9oU1Tl22Aw+iaGh0LZZOFXtMCt8mY7HN7pU2XYl+tEMEmXsiHOeAWfbGI/YYnyd8RwrPJKVuq8WGcjg==",
    "Expiration": "2017-02-08T05:51:21Z",
    "AccessKeyId": "STS.H2Xox4rdMTo2Vop5Z1FbR4iSv"
  },
  "FileInfo": {
    "fileName": "2017020812_10468_vHPCMkYp29.text",
    "path": "ycl-bucket-01/record/2017020812_10468_vHPCMkYp29.text",
    "sign": "d4c422e57b6d422bb0462c5e77295b9c"
  }
}

```

* 流程

>客户端直接上传OSS存储，先通过接口获取oss token，文件名为服务端限制，其他路径是无法通过该token上传的。
**sign** 为文件名签名，上传成功后通知服务端时应该携带该值，服务端将做验证，验证不通过则认为上传失败。


# v 1.5.0

### 获取钻石黑票

* URL

 `userGold: /api/user/user-gold` 

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |


* Response

| *名称*        | *参数说明* | *备注* |
| ----------- | ------ | ---- |
| gold |        |  钻石数     |
| allOutlayGold | 送出钻石    |       |
| allEarnPoint | 总黑票数   |       |
| point |   现有黑票 |       |



* Error Response

    `700:参数错误`
    `720:token无效`

* Example

```
{
  "errorcode": 0,
  "errormsg": "success",
  "user": {
    "gold": 9370721,
    "point": 402285,
    "userId": 10262,
    "pointWorth": 2011425,
    "allOutlayGold": 632919,
    "allEarnPoint": 407285
  }
}
```

### 上传配置

> 配置开关通过接口上传，获取通过userInfo接口获取，获取自己的user信息会带有**attribute**节点,**attribute**为用户配置开关，类型为字符串

```
{
  "errorcode": 0,
  "errormsg": "success",
  "result": {
    "followerCount": 25,
    "point": 1120421,
    "attribute": {
      "push_enable": "1"
    },
    "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-15-108.png",
    "user_type": "Anchor",
    "roomCount": 0,
    "postCount": 615557,
    "id": 10258,
    "user_status": "Published",
    "liveCount": 91,
    "description": "",
    "goldCount": 9,
    "heiNum": 1000419,
    "modifyCount": 0,
    "address": "",
    "honours": [
      {
        "honour_sign": "p",
        "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_daren_nan.png",
        "honour_desc": "达人-男"
      }
    ],
    "displayName": "蓝天白云该6",
    "modifyText": "(本次改名免费，下次修改费用10钻)",
    "level": 78,
    "gender": "Male",
    "region": "",
    "experience": 6146776,
    "birthDay": "1988-08-01",
    "followingCount": 11,
    "allEarnPoint": 1120421
  }
}
```

* URL

 `updateConfig: /api/user/update-config` 

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| push_enable    |        | str   |      | Y     | 0:关闭，1：打开 |


* Response

| *名称*        | *参数说明* | *备注* |
| ----------- | ------ | ---- |


* Error Response

    `700:参数错误`
    `720:token无效`

* Example

```
{
  "errorcode": 0,
  "errormsg": "success"
}
```

### 敲门状态

> 正在直播的房间是否进行敲门通过此接口返回数据判断，同时更新列表中的数据

* URL

 `knockStatus: /api/live/knock-status` 

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| liveId    |        | long   |      | Y     |      |


* Response

| *名称*        | *参数说明* | *备注* |
| ----------- | ------ | ---- |
| needKnock | 是否要敲门 | |
| roomUserCount | 房间人数上限 | |
| roomNowUserCount | 房间内人数 | |
| liveStatus | 直播状态 | 0：待开始，1：正在直播，2：直播结束，3：客服禁播, 4：删除 |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`

* Example

```
{
  "errorcode": 0,
  "needKnock": true,
  "roomUserCount": 8,
  "errormsg": "success",
  "roomNowUserCount": 4,
  "liveStatus": 2
}
```

### 心跳
* URL
>`heartBeat:https://api.wmlives.cn/api/live/heart-beat` 

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| liveId    |        | long   |      | Y     |      |
| isCreator |        | int    |      | Y     |      |


* Response

| *名称*        | *参数说明* | *备注* |
| ----------- | ------ | ---- |
| nextTimeout | 心跳时间间隔   | 秒    |

* Error Response

    `700:参数错误`
    `711:用户权限不足`
    `720:token无效`
    `731:直播无效`
    `506:您不在该队伍`

* Example

```
{
    errorcode:0,
    errormsg:"success",
    liveId:1121323,
    nextTimeout:15
}
```

> 心跳返回错误后退出直播间，结束心跳轮询。
> **buy-gift**,**buy-bullet**,**list-live-users**,**live-like**接口如果当前用户不在该房间会返回
**506:您不在该队伍**错误码，**get-live**接口如果当前正在直播并且当前请求用户不在该房间也会返回**506**

### 观看直播用户列表
* URL

`listLiveUsers:https://api.wmlives.cn/api/live/list-live-users`

* Parameters

| *名称*         | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*              |
| ------------ | ------ | ------ | ---- | ----- | ----------------- |
| token        |        | string |      | Y     |                   |
| liveId       |        | long   |      | Y     |                   |
| lastJoinTime |        | long   |      | N     | Default:0         |
| direction    |        | int    | 0,1  | N     | 0获取最新向右划，1获取之前向左划 |

* Response

|*名称*|*参数说明*|*备注*|
|------| -----|-----|
| totalCount | 房间内总人数，包括主播 |  |
| roomSeatCount | 房间座位数 | |
| roomLockedCount | 房间被锁座位数 | |

* Error Response

    `700:参数错误`
    `710:用户不存在`

* Example

```
{
    errorcode:0,
    errormsg:"success",
    expireTime:60,
    roomSeatCount:8,
    totalCount:3,
    roomLockedCount:2,
    users:[
      {
         id:1229,
         name:"倔强的白羊",
         isFollowed:true,
         coverUrl:"http://aab.ccc.com/img/12223",
         gender: "Male",
         birthDay: "1986-07-16",
         joinTime:1233214123
      },
      {
         id:1229,
         name:"倔强的白羊",
         isFollowed:true,
         coverUrl:"http://aab.ccc.com/img/12223",
         gender: "Male",
         birthDay: "1986-07-16",
         joinTime:1233214123
      },
      {
          id:1229,
         name:"倔强的白羊",
         isFollowed:true,
         coverUrl:"http://aab.ccc.com/img/12223",
         gender: "Male",
         birthDay: "1986-07-16",
         joinTime:1233214123
      }
    ]
}
```

* message

```
msg = {
    roomSeatCount:8,
    totalCount:3,
    roomLockedCount:2,
    users:[]
}

```

> 没有**users**节点表示只是人数或锁定的座位数发生了变化


### 加入直播

* URL

`joinLive:https://api.wmlives.cn/api/live/join-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |
| liveKey |        | string   |      | N     |  别邀请需要带liveKey   |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `725:live is not inactive`
    `737:无法观看该用户直播`
    `505:没座位了，敲门试试？`
    
* Example

```
```

### 创建直播
* URL

`createLive:https://api.wmlives.cn/api/live/create-live`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ----- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |      |
| title |        | string |      | Y     |      |

* Response

| *名称*         | *参数说明* | *备注* |
| ------------ | ------ | ---------------------------------------- |
| liveId       | 直播ID   |                                          |
| streamAddr   | 收听地址   |                                          |
| shareAddr    | 分享地址   |                                          |
| lookbackAddr | 回放地址   |                                          |
| roomId       | 房间号    |                                          |
| status       | 状态     | 0-to be start 1-playing  2-stoped  3-baned 4-delete（主播自己设置删除标识） |
|inefficientTime|防挂机时间| |
|countDownTime| 倒计时时间| | 


* Error Response

    `700:参数错误`
    `720:token无效`

* Example

```
{
    errorcode:0,
    errormsg:"success",
    live:{
        "status" : 0,
        "liveId" : 13456,
        "title" :  "title",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        visible:1
    },
    share:{
        wechat:{
            title:"嘿嘿直播",
            content:"xxx 正在直播",
            url:"",
            "coverUrl":""
        },
        weibo:{
            title:"嘿嘿直播",
            content:"xxx 正在直播",
            url:"",
            "coverUrl":""
        },
        friend:{
            title:"嘿嘿直播",
            content:"xxx 正在直播",
            url:"",
            "coverUrl":""
        }
    },
    liveOptions: {
        "inefficientTime": 1200,
        "countDownTime":60,
        "alertTitle" : "队长，你在吗？",
        "alertContent": "60秒内不点击‘在的’按钮将结束此次组队"，
        "helpLink": "www.baidu.com"
    }
}
```

### 更新用户信息
* URL

 `updateUser` `https://api.wmlives.cn/api/user/update`

* Parameters

| *名称*        | *参数说明* | *类型*   | *枚举*                          | *必要性* | *备注*              |
| ----------- | ------ | ------ | ----------------------------- | ----- | ----------------- |
| token       |        | string |                               | Y     |                   |
| displayName | 昵称     | string |                               | Y     |                   |
| gender      | 性别     | string | 'Male','Female','Unspecified' | Y     |                   |
| birthDay    | 生日     | string |                               | Y     | format YYYY-MM-dd |
| address     | 定位地址   | string |                               | N     |                   |
| latlng      | 经纬度    | string |                               | N     | \|分割              |
| description | 描述     | string |                               | N     |                   |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token 无效`
    `445:非法的名称`
    `447:名字太长`
    `501:未成年人禁止直播！`
    `721：用户账户异常`
    `740：余额不足`
    
### 获取用户信息
* URL

`userInfo:https://api.wmlives.cn/api/user/info`

* Error Response

    `700:参数错误`
    `720:token无效`
    
* Response

| *名称*           | *参数说明* | *备注* |
| -------------- | ------ | ---- |
| confStatus     |  1:连麦 2:连麦不可用 3:断开  4:接听    | 没有**userStatus**节点的话为正常的越聊按钮， 直播中状态有**jump**值|
| expireTime     |   当状态为2或4的话有倒计时时间 ，单位秒  |     |
| type     |   5:直播中 6:约聊中 |  没有**userStatus**节点的话为正常的约聊按钮， 直播中状态有**jump**值  |
| modifyText     |  改名收费提示 |                      |
|modifyCount     |       改名次数            |                       |


* Example

```
{
  "errorcode": 0,
  "errormsg": "success",
  "result": {
    "followerCount": 22,
    "point": 336487,
    "attribute": {
      "push_enable": "1"
    },
    "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19-108.png",
    "user_type": "Anchor",
    "roomCount": 30,
    "postCount": 193748,
    "id": 10001,
    "user_status": "Published",
    "liveCount": 123,
    "description": "有效防范休闲范。 你",
    "goldCount": 53443,
    "heiNum": 1000172,
    "modifyCount": 0,
    "address": "北京市",
    "honours": [],
    "displayName": "陌生人_再",
    "modifyText": "(本次改名免费，下次修改费用10钻)",
    "level": 54,
    "gender": "Male",
    "region": "",
    "experience": 1620440,
    "birthDay": "2016-09-29",
    "followingCount": 18,
    "allEarnPoint": 343787
  }
}
```



### 锁/解锁座位

* URL

 `lockLiveSeat:/api/live/lock-live-seat`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | string |      | Y     |      |
| unlock |        | boolean |  1:解锁 0：加锁 | Y   | 是否解锁|
      
* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `711:权限不足`
    `720:token无效`
    `731:直播无效或被删除`
    `502:请至少保留2个座位`

* Example

```
{
   "errorcode": 0, 
   "errormsg": "success"
}
```

### 邀请好友列表

* URL

 `inviteUsersList:/api/live/invite-user-list`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | string |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
|knocked|是否敲过门|    |

* Error Response

    `700:参数错误`
    `711:权限不足`
    `720:token无效`
    `731:直播无效或被删除`

* Example

```
{
  "errorcode": 0,
  "errormsg": "success",
  "users": [
    {
      "lastModified": 1481538170,
      "user_status": "Published",
      "displayName": "坏坏哒毛毛",
      "description": "温暖的你，是我最想遇见的风景。\n",
      "level": 1,
      "gender": "Male",
      "region": "",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-7-108.png",
      "user_type": "Normal",
      "experience": 0,
      "roomCount": 0,
      "heiNum": 1000206,
      "birthDay": "1970-04-16",
      "modifyCount": 0,
      "address": "",
      "knocked": false,
      "honours": [],
      "id": 10062,
      "isFollowed": true
    },
    {
      "lastModified": 1481538170,
      "user_status": "Published",
      "displayName": "樊_yuan",
      "description": "如果我没有什么可以帮到你，至少可以陪着你。\n",
      "level": 1,
      "gender": "Male",
      "region": "",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-11-108.png",
      "user_type": "Normal",
      "experience": 0,
      "roomCount": 0,
      "heiNum": 1000207,
      "birthDay": "1986-05-24",
      "modifyCount": 0,
      "address": "",
      "knocked": false,
      "honours": [],
      "id": 10063,
      "isFollowed": true
    }
  ]
 }
```

### 邀请好友

* URL

 `inviteUser:/api/live/invite-user`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | string |      | Y     |      |
| userId |        | string |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `711:权限不足`
    `720:token无效`
    `731:直播无效或被删除`

* Example

```
{
   "errorcode": 0, 
   "errormsg": "success"
}
```

* 消息
```
msg = {
            "msgType": "action",
            "action": "live-invite",
            "liveId": liveId,
            "liveKey": key,
            "text": "队长#name#想邀请你加入队伍，是否加入？",
            'link': u 'wmlivesheihei://live?id=1464245661396343070&liveKey=12ac58ef56ba51cf5dbee2dc9a4811b8',
            "fromUserId": userInfo["id"],
            "fromUserName": userInfo["displayName"],
            "gender": userInfo["gender"],
            "coverUrl": userInfo["coverUrl"],
            "birthDay": userInfo["birthDay"],
            "honours": userInfo.get("honours", [])
        }
```
>客户端收到此消息后，携带liveKey调用joinLive, 如果客户端没有启动,服务端会根据用户配置推送消息， 如果客户端在后台启动客户端需要把socket消息根据用户配置开关通知用户。

* 推送消息结构

> 通过link值进入直播间
```
{
    'fromUserId': 10001,
    'text': u '\u961f\u957f"\u964c\u751f\u4eba_\u518d"\u60f3\u9080\u8bf7\u4f60\u52a0\u5165\u961f\u4f0d\uff0c\u662f\u5426\u52a0\u5165\uff1f',
    'clientid': u '3c34858b82918f7e38b0f3f1f71677dd21f26bf37fed4fbc7a0eede57ee3c10d',
    'link': u 'wmlivesheihei://live?id=1464245661396343070&liveKey=12ac58ef56ba51cf5dbee2dc9a4811b8',
    'data': {},
    'fromUserName': u '\u964c\u751f\u4eba_\u518d',
    'title': u '\u961f\u957f"\u964c\u751f\u4eba_\u518d"\u60f3\u9080\u8bf7\u4f60\u52a0\u5165\u961f\u4f0d\uff0c\u662f\u5426\u52a0\u5165\uff1f',
    'gender': u 'Male',
    'deviceType': u 'ios',
    'msgId': 1305830658323863951 L,
    'action': u 'live-invite'
}
```

### 敲门

* URL

 `knockLiveRoom:/api/live/knock-live-room`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | string |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `711:权限不足`
    `720:token无效`
    `731:直播无效或被删除`
    `504:刚敲过门啦 歇会~`

* Example

```
{
   "errorcode": 0, 
   "errormsg": "success"
}
```

### 踢出直播间的用户

* URL

 `kickOutUser:/api/live/kick-out-user`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | string |      | Y     |      |
| userId |        | int |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `711:权限不足`
    `720:token无效`
    `731:直播无效或被删除`

* Example

```
{
   "errorcode": 0, 
   "errormsg": "success"
}
```

* Message
```
msg = {
            "msgType": "action",
            "action": "quit-live",
            "comment": "踢出房间动作消息",
            "liveId": live_id
        }
```
> 客户端收到此消息后调用quitLive接口

### 关注用户直播与回放

* URL

 `listLiveByFollow:/api/live/list-live-by-follow`

* Parameters

|*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
| roomUserCount | 房间人数上限 |  |
| roomNowUserCount | 房间人数|  |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example

```
{
  "expireTime": 60,
  "errormsg": "",
  "lives": [
    {
      "streamAddr": "rtmp://pili-live-rtmp.heihei-test.wmlives.com/heihei-test-0907/20170213-115710-10446",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-5-108.png",
      "visible": 1,
      "totalUsers": 0,
      "honours": [
        {
          "honour_sign": "v",
          "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
          "honour_desc": "认证"
        }
      ],
      "roomId": 3520846628452474100,
      "isFollowed": true,
      "slot": "z1.heihei-test-0907.20170213-115710-10446",
      "title": "浩浩汤汤",
      "deviceType": null,
      "shareAddr": "http://pili-live-hdl.heihei-test.wmlives.com/heihei-test-0907/20170213-115710-10446.flv",
      "hlsAddr": "http://pili-live-hls.heihei-test.wmlives.com/heihei-test-0907/20170213-115710-10446.m3u8",
      "status": 1,
      "userId": 10446,
      "endTime": null,
      "startTime": "2017-02-13 11:57:10",
      "address": "北京市",
      "onlineUsers": 0,
      "lookbackAddr": "",
      "createTime": "2017-02-13 11:57:10",
      "userName": "哇哇哇",
      "liveId": "3520846628452474100",
      "totalTickets": "0",
      "gender": "Male",
      "length": null,
      "birthDay": "2009-02-20",
      "messageAddr": "",
      "roomUserCount": 8,
      "roomNowUserCount":6
    }
  ],
  "lookbacks": [
    {
      "streamAddr": "rtmp://pili-live-rtmp.heihei-test.wmlives.com/heihei-test-0907/20170210-202311-10246",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-4-108.png",
      "visible": 1,
      "totalUsers": 11,
      "honours": [],
      "roomId": 4011389901595663277,
      "isFollowed": true,
      "title": "得得",
      "deviceType": null,
      "shareAddr": "http://pili-live-hdl.heihei-test.wmlives.com/heihei-test-0907/20170210-202311-10246.flv",
      "hlsAddr": "http://pili-live-hls.heihei-test.wmlives.com/heihei-test-0907/20170210-202311-10246.m3u8",
      "status": 2,
      "userId": 10246,
      "endTime": "2017-02-10 20:46:56",
      "startTime": "2017-02-10 20:23:13",
      "address": "北京市",
      "onlineUsers": 0,
      "lookbackAddr": "http://pili-media.heihei-test.wmlives.com/recordings/z1.heihei-test-0907.20170210-202311-10246/z1.heihei-test-0907.20170210-202311-10246.mp4",
      "createTime": "2017-02-10 20:23:11",
      "userName": "嘎嘎",
      "liveId": 4011389901595663277,
      "totalTickets": "0",
      "gender": "Female",
      "length": 1303,
      "birthDay": "2002-02-01",
      "messageAddr": "http://cdn.wmlives.com/message/message_4011389901595663277.txt.zip"
    },
    {
      "streamAddr": "rtmp://pili-live-rtmp.heihei-test.wmlives.com/heihei-test-0907/20170210-201753-10246",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-4-108.png",
      "visible": 1,
      "totalUsers": 11,
      "honours": [],
      "roomId": 1063142005052369222,
      "isFollowed": true,
      "title": "丰富的",
      "deviceType": null,
      "shareAddr": "http://pili-live-hdl.heihei-test.wmlives.com/heihei-test-0907/20170210-201753-10246.flv",
      "hlsAddr": "http://pili-live-hls.heihei-test.wmlives.com/heihei-test-0907/20170210-201753-10246.m3u8",
      "status": 2,
      "userId": 10246,
      "endTime": "2017-02-10 20:20:09",
      "startTime": "2017-02-10 20:17:55",
      "address": "北京市",
      "onlineUsers": 0,
      "lookbackAddr": "http://pili-media.heihei-test.wmlives.com/recordings/z1.heihei-test-0907.20170210-201753-10246/z1.heihei-test-0907.20170210-201753-10246.mp4",
      "createTime": "2017-02-10 20:17:53",
      "userName": "嘎嘎",
      "liveId": 1063142005052369222,
      "totalTickets": "0",
      "gender": "Female",
      "length": 34,
      "birthDay": "2002-02-01",
      "messageAddr": "http://cdn.wmlives.com/message/message_1063142005052369222.txt.zip"
    }
  ],
  "errorcode": 0
}
```


# v 1.4.1

### 获取连麦状态

* URL

`getChat:/api/chat/get-chat`

* Parameters

      |*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
      | ------ | ------ | ------ | ---- | ----- | ---- |
      | token  |        | string |      | Y     |      |
      | chatId  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`
    `733:房间无效`

* Example

```
{
  "errorcode": 0,
  "errormsg": "success",
  "chat": {
    "status": 3,
    "pushAddr": "",
    "title": "10244,10243",
    "streamAddr": "",
    "createrId": 10244,
    "visible": 1,
    "archiveFile": null,
    "startTime": "2017-02-06 16:32:05",
    "user": [
      {
        "lastModified": 1486370372,
        "user_status": "Published",
        "displayName": "Q",
        "description": "定哦咯",
        "level": 57,
        "gender": "Female",
        "region": "",
        "point": 153435,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-24-108.png",
        "user_type": "Anchor",
        "experience": 1752658,
        "heiNum": 1000410,
        "birthDay": "2016-12-11",
        "status": 3,
        "address": "北京市",
        "honours": [
          {
            "honour_sign": "v",
            "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
            "honour_desc": "认证"
          }
        ],
        "id": 10244,
        "isFollowed": false,
        "allEarnPoint": 153435
      },
      {
        "lastModified": 1486385883,
        "user_status": "Published",
        "displayName": "测试号广告分沟沟",
        "description": "",
        "level": 38,
        "gender": "Male",
        "region": "",
        "point": 187665,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-15-108.png",
        "user_type": "Anchor",
        "experience": 806234,
        "heiNum": 1000409,
        "birthDay": "2016-07-24",
        "status": 3,
        "address": "北京市",
        "honours": [
          {
            "honour_sign": "v",
            "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
            "honour_desc": "认证"
          }
        ],
        "id": 10243,
        "isFollowed": true,
        "allEarnPoint": 187665
      }
    ],
    "roomId": 3031623101663186248,
    "createTime": "2017-02-06 16:32:05",
    "chatId": 3031623101663186248
  }
}
```

# v 1.4.0

### 未关闭的直播查询

* URL

`unclosedLive:/api/live/unclosed-live`

* Parameters

      |*名称*|*参数说明*|*类型*|*枚举*|*必要性*|*备注*|
      | ------ | ------ | ------ | ---- | ----- | ---- |
      | token  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
如果有未关闭的Live
**同create-live接口返回的数据**，如果没有返回 
```
{
  "errorcode": 0,
  "errormsg": "success"
}
```

### 礼物消息更改
* 礼物

    ```
    msg : {
        msgType:"gift",
        amount:128,
        giftId:12,
        roomId:123, // client需判断当前roomid
        fromUserId:1233,
        fromUserName:"谁送的",
        gender: "Male",
        gift:{
            "id": 128,
            "name": 'asjkdfa',
            "type": 1,
            "desc": "啪啪啪"
        }
        totalTicket:123322,
        gift_uuid:"adfd32ffa424",
        msgId:12222221334124
    }
    ```
    
### 新增消息数消息

显示未读消息数，通过websocket下发。以服务端的计数为准，客户端不再维护未读消息数。

```
msg = {
            "msgType": "action",
            "action": "message-unread-count",
            "comment": "未读消息数",
            "count": 12
       }
```

### messageList

**新增未读消息数**

* URL

`messageList:/api/msg/message-list`

* Parameters

    | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
    | ------ | ------ | ------ | ---- | ----- | ---- |
    | token  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
  "errorcode": 0,
  "errormsg": "success",
  "messages": [
    {
      "fromUserId": 63,
      "fromUserName": "这里",
      "gender": "Male",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19.png",
      "data": {
        "count": 1,
        "type": "post"
      },
      "birthDay": "2014-09-25",
      "link": "wmlives_heihei://duechat?uid=63",
      "timeStamp": 1477557322,
      "action": "message",
      "msgType": "action",
      "text": null
    },
    {
      "fromUserId": 10031,
      "fromUserName": "小宋手机号1",
      "gender": "Female",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-2.png",
      "data": {
        "count": 5,
        "type": "calling"
      },
      "birthDay": "2016-01-01",
      "link": "wmlives_heihei://duechat?uid=10031",
      "timeStamp": 1477557274,
      "action": "message",
      "msgType": "action",
      "text": null
    }
  ],
  "unreadMsgCount":12
}
```

### 礼物资源下载
* URL

`giftResources:https://api.wmlives.cn/api/social/gift-resources`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*            |
| ----- | ------ | ------ | ---- | ----- | --------------- |
| token |        | string |      | Y     |                 |
| giftIds   |        | string   |      |N     |   礼物ID，以,隔开   |


* Response

| *名称*           | *参数说明* | *备注* |
| -------------- | ------ | ----  |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example

```
{
  "errorcode": 0,
  "errormsg": "success",
  "resources": [
    {
      "file_md5": null,
      "id": 101,
      "attr_file": "http://cdn.wmlives.com"
    },
    {
      "file_md5": null,
      "id": 102,
      "attr_file": "http://cdn.wmlives.com"
    }
  ],
  "historyGiftRes": [
    {
      "file_md5": 2323EFA,
      "id": 103,
      "attr_file": "http://cdn.wmlives.com/akdkdk/dd"
    }
  ]
}
```


### 获取用户信息
* URL

`userInfo:https://api.wmlives.cn/api/user/info`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*            |
| ----- | ------ | ------ | ---- | ----- | --------------- |
| token |        | string |      | Y     |                 |
| uid   |        | long   |      | Y     |                 |
| cuid  |        | long   |      | N     | 如果有值将会判断是否关注及拉黑 |
| liveId   |    | long   |      | N | 如果在直播间点击用户卡片传liveId|

* Response

| *名称*           | *参数说明* | *备注* |
| -------------- | ------ | ---- |
| confStatus     |  1:连麦 2:连麦不可用 3:断开  4:接听    | 没有**userStatus**节点的话为正常的越聊按钮， 直播中状态有**jump**值|
| expireTime     |   当状态为2或4的话有倒计时时间 ，单位秒  |     |
| type     |   5:直播中 6:约聊中 |  没有**userStatus**节点的话为正常的约聊按钮， 直播中状态有**jump**值  |


>~~如果请求的UID为自己，则会增加**heiNum**字段，作为黑号~~

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
    `736:无法查看该用户信息`

* Example
**直播返回**
```
{
    errorcode:0,
    errormsg:"success",
    result:{
        "followerCount": 5,
        "description": "hjjjjjH",
        "point": 0,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19-108.png",
        "user_type": "Anchor",
        "goldCount": 20000,
        "heiNum": 1000149,
        "postCount": 0,
        "address": "北京市",
        "honours": [
          {
            "honour_sign": "v",
            "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
            "honour_desc": "认证"
          },
          {
            "honour_sign": "p",
            "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
            "honour_desc": "专业"
          }
        ],
        "id": 65,
        "isFollowed": false,
        "isBlocked": false,
        "user_status": "Published",
        "displayName": "Gagaha",
        "level": 1,
        "gender": "Male",
        "region": "",
        "experience": 0,
        "birthDay": "2016-09-25",
        "lastModified": 1482479955,
        "followingCount": 1,
        "liveCount": 0,
        "allEarnPoint": 0
    },
    "userStatus":{
        "confStatus":2,
        "expireTime":30,
        "jump":"#link"
    }
}
```

**非直播返回**
```
{
    errorcode:0,
    errormsg:"success",
    result:{
        "followerCount": 5,
        "description": "hjjjjjH",
        "point": 0,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19-108.png",
        "user_type": "Anchor",
        "goldCount": 20000,
        "heiNum": 1000149,
        "postCount": 0,
        "address": "北京市",
        "honours": [
          {
            "honour_sign": "v",
            "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
            "honour_desc": "认证"
          },
          {
            "honour_sign": "p",
            "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
            "honour_desc": "专业"
          }
        ],
        "id": 65,
        "isFollowed": false,
        "isBlocked": false,
        "user_status": "Published",
        "displayName": "Gagaha",
        "level": 1,
        "gender": "Male",
        "region": "",
        "experience": 0,
        "birthDay": "2016-09-25",
        "lastModified": 1482479955,
        "followingCount": 1,
        "liveCount": 0,
        "allEarnPoint": 0
    },
    "userStatus":{
        "type":1,
        "jump":"#link"
    }
}
```

```json
  {
  "errorcode": 0,
  "errormsg": "success",
  "result": {
    "followerCount": 5,
    "description": "hjjjjjH",
    "point": 0,
    "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19-108.png",
    "user_type": "Anchor",
    "goldCount": 20000,
    "heiNum": 1000149,
    "postCount": 0,
    "address": "北京市",
    "honours": [
      {
        "honour_sign": "v",
        "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
        "honour_desc": "认证"
      },
      {
        "honour_sign": "p",
        "honour_img": "http://cdn.wmlives.com/static/img/heihei/common/hh_admin_vip.png",
        "honour_desc": "专业"
      }
    ],
    "id": 65,
    "isFollowed": false,
    "isBlocked": false,
    "user_status": "Published",
    "displayName": "Gagaha",
    "level": 1,
    "gender": "Male",
    "region": "",
    "experience": 0,
    "birthDay": "2016-09-25",
    "lastModified": 1482479955,
    "followingCount": 1,
    "liveCount": 0,
    "allEarnPoint": 0
  }
}

```
# v 1.3.0接口

## 黑聊

### 搜索
* URL

> 搜索初始化的文案在init接口返回 
```
    tips:{
            "pay-tips" : "领取红包请联系黑黑官方客服\n微信号：welines-wallet",
            "search-tips": "输入黑号或昵称搜索"
    }
```

`search:https://api.wmlives.cn/api/user/search`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*            |
| ----- | ------ | ------ | ---- | ----- | --------------- |
| token |        | string |      | Y     |                 |
| queryParameter   |        | string   |      | Y     |                 |


* Response

| *名称*           | *参数说明* | *备注* |
| -------------- | ------ | ---- |


* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
  "errorcode": 0,
  "errormsg": "success",
  "users": [
    {
      "lastModified": 1481538168,
      "user_status": "Published",
      "displayName": "邵晶微信号",
      "description": "",
      "level": 30,
      "gender": "Male",
      "region": "",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19-108.png",
      "user_type": "Anchor",
      "experience": 490792,
      "birthDay": "2016-09-27",
      "address": "",
      "id": 73,
      "isFollowed": false
    },
    {
      "lastModified": 1481538191,
      "user_status": "Published",
      "displayName": "邵晶",
      "description": "现在就开始",
      "level": 5,
      "gender": "Female",
      "region": "",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-20-108.png",
      "user_type": "Anchor",
      "experience": 2404,
      "birthDay": "1992-10-19",
      "address": "北京市",
      "id": 10442,
      "isFollowed": false
    },
    {
      "lastModified": 1481538167,
      "user_status": "Published",
      "displayName": "邵晶手机号",
      "description": "陌陌摸摸哦哦啦咯啦咯啦咯啦咯啦咯啦咯考虑考虑监控",
      "level": 1,
      "gender": "Female",
      "region": "",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-20-108.png",
      "user_type": "Anchor",
      "experience": 0,
      "birthDay": "1989-10-01",
      "address": "北京市",
      "id": 49,
      "isFollowed": false
    },
    {
      "lastModified": 1481538168,
      "user_status": "Published",
      "displayName": "邵晶手机号",
      "description": "",
      "level": 1,
      "gender": "Male",
      "region": "",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19-108.png",
      "user_type": "Anchor",
      "experience": 0,
      "birthDay": "2016-09-28",
      "address": "",
      "id": 75,
      "isFollowed": false
    }
  ]
}
```



### 刷新录音

* URL

 `refreshRecord` `https://api.wmlives.cn/api/record/refresh-record`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| score |        | int |      | Y   |  为0时默认为刷新当前页，加载最新   |


* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|


* Error Response

    `700:参数错误`
    `720:token无效`
    
* 流程
    
    属于自己的录音如果状态为0，则在听的时候先请求服务器，判断当前录音是否可听。
    其他人的录音可以先播放当前列表页的录音地址，再请求服务端做历史记录。

* Example


```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "data":{
     "mine":{
        recordId:1111,
        userId:1,
        recordPath:"",
        redordLength:5,
        status:1,
        createTime:"2016-12-07 14:54:44",
        userInfo:{
            displayName: "Victor Chou",
        	id: 3176111,
        	coverUrl: "http://aaa/bbb/ccc",
            region: "zh_CN",
        	gender: "Male",
        	birthDay: "1986-07-16",
            level:12
        }
     },
     records:[
        {
            recordId:1111,
            userId:1,
            recordPath:"",
            redordLength:5,
            status:1,
            createTime:"2016-12-07 14:54:44",
            score:1034232,
            timeTip:"1分钟前",
            userInfo:{
                displayName: "Victor Chou",
            	id: 3176111,
            	coverUrl: "http://aaa/bbb/ccc",
                region: "zh_CN",
            	gender: "Male",
            	birthDay: "1986-07-16",
                level:12,
                isFollow:true,
                status:{
                    type:1, # 1：直播中 ， 2：约聊中， 默认为可约聊状态
                    jump:"#link" ，# 如果为1的话有jump节点， 值为link值
                }
              }
        },
        {
            recordId:1111,
            userId:1,
            recordPath:"",
            redordLength:5,
            status:1,
            createTime:"2016-12-07 14:54:44",
            score:1034232,
            timeTip:"5分钟前",
            userInfo:{
                displayName: "Victor Chou",
            	id: 3176111,
            	coverUrl: "http://aaa/bbb/ccc",
                region: "zh_CN",
            	gender: "Male",
            	birthDay: "1986-07-16",
                level:12,
                isFollow:true
             }
        }
     ]
  }
}
```

### 上传录音

* URL

 `uploadRecord` `https://api.wmlives.cn/api/record/upload-record`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| file |        | file |      | Y   |  |
| fileName |        | string |      | Y   |  |
| fileMd5 |        | string |      | Y   |  |
| recordLength |        | int |      | Y   | 单位秒 |


* Response

| *名称*  | *参数说明* | *备注* |
|------|------|------|


* Error Response

    `700:参数错误`
    `720:token无效`
    `754:文件损坏,请重新上传。`
    `755:录音时间太短`
    `756:文件太大啦`
    
* Example

```
{
  "errorcode" : 0,
  "errormsg" :"success"
}
```

### 删除录音

* URL

 `deleteRecord` `https://api.wmlives.cn/api/record/delete-record`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| recordId |        | int |      | Y   |  |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|


* Error Response

    `700:参数错误`
    `720:token无效`
    `757:录音不存在`
    `757:无法删除不属于自己的录音`
    
* Example

```
{
  "errorcode" : 0,
  "errormsg" :"success"
}
```


### 听录音

* URL

 `readRecord` `https://api.wmlives.cn/api/record/read-record`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| recordId |        | int |      | Y   |  |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|


* Error Response

    `700:参数错误`
    `720:token无效`
    `757:录音不存在`
    
* Example

```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "record":{
            recordId:1111,
            userId:1,
            recordPath:"",
            redordLength:5,
            status:1,
            createTime:"2016-12-07 14:54:44",
            score:1034232,
            userInfo:{
                displayName: "Victor Chou",
            	id: 3176111,
            	coverUrl: "http://aaa/bbb/ccc",
                region: "zh_CN",
            	gender: "Male",
            	birthDay: "1986-07-16",
                level:12,
                isFollow:true
             }
        }
}
```


# v 1.2.0接口

## 对聊

### 申请连麦接口


* URL

 `callRequest` `https://api.wmlives.cn/api/live/call-request`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| liveId |        | string |      | Y     |     |
| userId |        | long |      | N    |  主播端约聊观看端时  |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|
|expireTime|失效时长 |  |

* Error Response

    `700:参数错误`
    `720:token无效`
    `722:您已被禁言`
    `731:无效的直播`
    `742:用户状态错误`
    
* 流程

    **客户端**
    客户端连麦主播，如果已被禁言，返回**722**错误，否则加入连麦队列，服务端通知客户端更新用户列表。30s后服务端在连麦队列中清除掉。
    **主播端**
    主播端连麦客户端，如果客户端已经在连麦队列中，则给双方下发加入连麦动作消息**join-conference**，如果主播邀请用户连麦，则服务端通知被连麦用户。30s后服务端在被邀请连麦队列中清除掉。
    
* Example

**客户端**
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "expireTime":30
}
```
  **主播端**  
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "expireTime":0
}
```

### 加入连麦接口

* URL

 `joinConference` `https://api.wmlives.cn/api/live/join-conference`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| liveId |        | string |      | Y     |     |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|
|expireTime| | token失效日期|

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    `742:用户状态错误`
    `750:哎呀，连线失败了`
* 流程
    客户端在收到 **join-conference**后调用joinConference接口，加入完成后服务端会对房间下发连麦状态消息**conference-status**，在连麦状态的房间下，如果有新的用户加入直播间内，也会收到此消息，客户端需要处理。接口返回加入rtc所需要的token，如果连麦过程中中断，或token失效，需要重新调用此接口获取token。
    如果此时连麦已结束，或连麦对象已不是当前用户，则返回**750**错误码；
    **joinConference** 至 **conferenceSuccess** 时间为6秒，超时则服务端会结束当前连麦。
    **客户端rtc连接失败的情况下要调用此接口**
* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "token":{
    "roomName": "12220030031",
    "roomToken": "sdsaassa",
    "expireTime": 1429933200
  },
  "confStatus":{
    "msgType": "action",
            "action": "conference-status",
            "comment": "连麦状态，0：连麦等待，1：已连麦 2:断开",
            "liveId": live_id,
            "status": 0,
            fromUserId:122,
            fromUserName:'张三',
            gender: "Male",
            birthDay: "1995-03-13",
            coverUrl: "http://aaa/bbb/ccc"
  }
}
```

### 接受连麦

* URL

 `acceptConference` `https://api.wmlives.cn/api/live/accept-conference`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| liveId |        | long |      | Y     |     |
| userId |        | long |      | N     |     |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|

* 流程
    

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    `742:用户状态错误`
    `739:您正在连麦中`
    `409:来晚了~`
* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "expireTime":5
}
```

### 拒绝连麦接口

* URL

 `refuseConference` `https://api.wmlives.cn/api/live/refuse-conference`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| liveId |        | long |      | Y     |     |
| userId |        | long |      | Y     |     |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|

* 流程
    主播拒绝观看段连麦，通知客户端更新用户列表状态。观看端拒绝主播，在邀请队列中清除。

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    `742:用户状态错误`

* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success"
}
```

### 退出连麦接口

* URL

 `quitConference` `https://api.wmlives.cn/api/live/quit-conference`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| liveId |        | string |      | Y     |     |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|


* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    `742:用户状态错误`
    
* 流程
    1.主播中断连麦，给连麦对象下发**stop-conference**消息；
    2.观看段中断给主播端下发**stop-conference**消息。
    同时给所有对象下发连麦状态消息**conference-status**，给所有客户端下发观看列表更新消息

* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success"
}
```

### 连麦成功

* URL

 `conferenceSuccess` `https://api.wmlives.cn/api/live/conference-success`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |     |
| liveId |        | string |      | Y     |     |

* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|


* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    
* 流程
    连麦用户连麦成功（rtc推流成功），通知服务端，当双方都成功后，服务端会给所有对象下发连麦状态消息**conference-status**。
* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "confStatus":{
    "msgType": "action",
    "action": "conference-status",
    "comment": "连麦状态，0：连麦等待，1：已连麦 2:断开",
    "liveId": live_id,
    "status": 0,
    fromUserId:122,
    fromUserName:'张三',
    gender: "Male",
    birthDay: "1995-03-13",
    coverUrl: "http://aaa/bbb/ccc"
  }
}
```


## 连麦消息


**conference-notify** 连麦邀请通知
```
msg = {
            "msgType": "action",
            "action": "conference-notify",
            "comment": "邀请连麦通知消息",
            "text": "主播邀你连线",
            "expireTime": 30,
            "liveId": live_id
        }
```

**join-conference** 加入连麦
```
 msg = {
     "msgType": "action",
     "action": "join-conference",
     "comment": "加入连麦动作消息",
     "liveId": live_id
 }
```

**conference-status** 连麦状态
```
 msg = {
            "msgType": "action",
            "action": "conference-status",
            "comment": "连麦状态，0：连麦等待，1：已连麦 2:断开",
            "liveId": live_id,
            "status": 0,
            fromUserId:122,
            fromUserName:'张三',
            gender: "Male",
            birthDay: "",
            coverUrl: "http://aaa/bbb/ccc"
        }
```

**连麦结束** 
```
msg = {
            "msgType": "action",
            "action": "stop-conference",
            "comment": "结束连麦",
            "liveId": live_id
        }
```

**tip消息** 
```
msg ={
            "msgType": "action",
            "action": "show-tip",
            "comment": "tip消息",
            "message":  {
                    "type": "alert",
                    "title": "alert test",
                    "desc": desc,
                    "jump":"",
                    "timeout":5,
                    "image":"",
                    "buttons":[{
                        "title":"ok",
                        "action":"wmlives_heihei://user?id=1221"
                        },
                        {
                        "title":"cancel",
                        "jump":""
                        }
                    ]
                }
            }

```
**type**:alert, toast, image
**jump**: 见 [link](#link)

### 获取用户信息
* URL

`userInfo:https://api.wmlives.cn/api/user/info`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*            |
| ----- | ------ | ------ | ---- | ----- | --------------- |
| token |        | string |      | Y     |                 |
| uid   |        | long   |      | Y     |                 |
| cuid  |        | long   |      | N     | 如果有值将会判断是否关注及拉黑 |
| liveId   |        | long   |      | N | 如果在直播间点击用户卡片传liveId|

* Response

| *名称*           | *参数说明* | *备注* |
| -------------- | ------ | ---- |
| confStatus     |  1:连麦 2:连麦不可用 3:断开  4:接听  5:直播中 6 约聊中   | 没有的话为正常的越聊按钮|
|expireTime     |   当状态为2或4的话有倒计时时间 ，单位秒  |     |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
    `736:无法查看该用户信息`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    result:{
        id:122223,
        displayName:"重千惠子",
        point:12222,
        goldCount:212,
        level:12
        coverUrl:"http://aab.ccc.com/img/12223"
        description:"自我描述",
        isFollowed:false,
        isBlocked:false,
        followerCount:1200,
        followingCount:1,
        userType:"",
        liveCount:0,
        postCount:2342,
        gender:"Male",
        birthDay:"2014-08-10"
    },
    "userStatus":{
        "confStatus":4,
        "expireTime":30,
        "jump":"#link"
    }
}
```

# 接口文档

## 模块

 * [初始化接口](#init)
 * [系统](#system)
 * [用户](#user)
 * [直播](#live)
 * [对聊](#chat)
 * [消息](#message)
 * [消息结构](#message-str)
 


### 初始化接口
<span id = "init">初始化接口：</span>
>客户端启动时应先调用此接口,接口的调用地址通过此接口返回;
>客户端根据key获取最终地址.

* URL

 `init` `https://api.wmlives.cn/api/init`

* Parameters

| *名称*        | *参数说明*      | *类型*   | *枚举*           | *必要性* | *备注*                         |
| ----------- | ----------- | ------ | -------------- | ----- | ---------------------------- |
| ap          | app name    | string | heihei         | Y     | value:heihei                 |
| version     | version     | string |                | Y     |                              |
| versionType | versionType | string |                | N     |                              |
| buildNumber |             | string |                | N     |                              |
| local       | 地区          | string | zh_CN;en_US    | Y     |                              |
| uuid        | 设备id        | string |                | Y     |                              |
| model       | 型号          | string |                | N     |                              |
| resolution  | 分辨率         | string |                | N     |                              |
| apiVersion  | api version | string |                | Y     | 1.0                          |
| osVersion   | os version  | string |                | N     | iOS 10,iOS 8.3 ...           |
| apnsType    |             | string | apns,gcm,getui | N     |                              |
| apnsToken   |             | string |                | N     | android 传个推cid,ios传apnstoken |
| deveiceType | 系统类型        | string | android;ios    | Y     |                              |
| token       | token       | string |                | N     |                              |
| channel     | 渠道          | string | AppStore,...   |       |                              |
| userId      |             | long   |                | N     |                              |

* Response

```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "user": {
        "getSMSVerificationCode" : "https://api-01.wmlive.cn/api/user/get-sms-verification-code",
        "signInCLByPhone" : "https://api-01.wmlive.cn/api/user/sign-in-cl-by-phone",
        "signIn" : "https://api-01.wmlive.cn/api/user/sign-in",
        "signOut" : "https://api-01.wmlive.cn/api/user/sign-out",
        "updateUser" : "https://api-01.wmlive.cn/api/user/update",
        "userInfo" : "https://api-01.wmlive.cn/api/user/info",

        "followUser" : "https://api-01.wmlive.cn/api/user/follow",
        "unfollowUser" : "https://api-01.wmlive.cn/api/user/unfollow",
        "listFollower" : "https://api-01.wmlive.cn/api/user/list-follower",
        "listFollowing" : "https://api-01.wmlive.cn/api/user/list-following",

        "listBlockedUser" : "https://api-01.wmlive.cn/api/user/list-blocked-user",
        "blockUser" : "https://api-01.wmlive.cn/api/user/block-user",
        "unblockUser" : "https://api-01.wmlive.cn/api/user/unblock-user",
        "listByType" : "https://api-01.wmlive.cn/api/user/list-user-byType",
        "listActiveUser" : "https://api-01.wmlive.cn/api/user/list-active-user",

        "registerPhone":"https://api-01.wmlive.cn/api/sms/register-phone",
        "verifyPhone":"https://api-01.wmlive.cn/api/sms/verify-phone",
        "usearch" : "https://api-01.wmlive.cn/api/user/usearch",
        "isinlive" : "https://api-01.wmlive.cn/api/user/isinlive",
        "reportUser" : "https://api-01.wmlive.cn/api/user/report-user",
        "bindPhone" : "https://api-01.wmlive.cn/api/user/bind-phone",
        "pushDeviceInfo" : "https://api-01.wmlive.cn/api/user/push-device-info"
  },
  "social": {
        "getBanner" : "https://api-01.wmlive.cn/api/social/get-banner"
  },
  "live" : {
        "createLive" : "https://api-01.wmlive.cn/api/live/create-live",
        "stopLive" : "https://api-01.wmlive.cn/api/live/stop-live",
        "changeLive" : "https://api-01.wmlive.cn/api/live/change-live",
        "deleteLive" : "https://api-01.wmlive.cn/api/live/delete-live",
        "setLiveVisible" : "https://api-01.wmlive.cn/api/live/set-live-visible",
        "getLive" : "https://api-01.wmlive.cn/api/live/get-live",
        "joinLive" : "https://api-01.wmlive.cn/api/live/join-live",
        "startLive" : "https://api-01.wmlive.cn/api/live/start-live",
        "heartBeat" : "https://api-01.wmlive.cn/api/live/heart-beat",
        "listLiveByFollow" : "https://api-01.wmlive.cn/api/live/list-live-by-follow",
        "listLiveByRecommend" : "https://api-01.wmlive.cn/api/live/list-live-by-recommend",
        "listLiveByUser" : "https://api-01.wmlive.cn/api/live/list-live-by-user",
        "giftInfo" : "https://api-01.wmlive.cn/api/live/gift-info",
        "buyGift" : "https://api-01.wmlive.cn/api/live/buy-gift",
        "buyBullet" : "https://api-01.wmlive.cn/api/live/buy-bullet",
        "liveLike" : "https://api-01.wmlive.cn/api/live/live-like",
        "listLiveUsers" : "https://api-01.wmlive.cn/api/live/list-live-users",
        "systemnotify" : "https://api-01.wmlive.cn/api/live/systemnotify",
        "shutupUser"  : "https://api-01.wmlive.cn/api/live/shutupuser",
        "shutupOpen"  : "https://api-01.wmlive.cn/api/live/shutupopen",
        "isshutup"  : "https://api-01.wmlive.cn/api/live/isshutup",
        "livemgr" : "https://api-01.wmlive.cn/api/live/livemgr",
        "getuser" : "https://api-01.wmlive.cn/api/live/getuser",
        "shareLive" : "https://api-01.wmlive.cn/api/live/share-live",
        "getmgruser" : "https://api-01.wmlive.cn/api/live/getmgruser",
        "pauseLive":"https://api-01.wmlive.cn/api/live/pause-live",
        "quitLive" : "https://api-01.wmlive.cn/api/live/quit-live",
        "continueLive":"https://api-01.wmlive.cn/api/live/continue-live",
        "listReplayUsers":"https://api-01.wmlive.cn/api/live/list-replay-users"
  },
  "message" : {
        "sendMsg" : "https://api-01.wmlive.cn/api/msg/send-msg",
        "historyMsg" : "https://api-01.wmlive.cn/api/msg/history-msg",
        "deleteMsg" : "https://api-01.wmlive.cn/api/msg/delete-msg",
        "readAllMsg" : "https://api-01.wmlive.cn/api/msg/read-all-msg",
        "readOneMsg" : "https://api-01.wmlive.cn/api/msg/read-one-msg",
        "channel" : "ws://123.56.0.31:8082/ws/channel",
        "messageList": "https://api-01.wmlive.cn/api/msg/message-list",
        "messageDel": "https://api-01.wmlive.cn/api/msg/message-del"
  },
  "payment" : {
        "createOrder" : "https://api-01.wmlive.cn/api/payment/create-order",
        "listPackage" : "https://api-01.wmlive.cn/api/payment/list-package",
        "orderNotify" : "https://api-01.wmlive.cn/api/payment/order-notify",
        "statistic" : "https://api-01.wmlive.cn/api/payment/statistic",
        "listP2gPackage" : "https://api-01.wmlive.cn/api/payment/list-p2g-package",
        "p2g" : "https://api-01.wmlive.cn/api/payment/p2g",
        "alipaycallback"  : "https://api-01.wmlive.cn/api/payment/alipaycallback",
        "wepaycallback" : "https://api-01.wmlive.cn/api/payment/wepaycallback",
        "getAlipayInfo" : "https://api-01.wmlive.cn/api/payment/get-alipay-info",
        "verifyAlipay" : "https://api-01.wmlive.cn/api/payment/verify-alipay",
        "payReq" : "https://api-01.wmlive.cn/api/payment/pay-req",
        "cash-info":"https://api-01.wmlive.cn/api/payment/cash-info",
        "payAgreement" :"http://api.heihei-test.wmlives.com/static/app/pay-agreement.html"
  },
  "chat" :{
        "matchChat" : "https://api-01.wmlive.cn/api/chat/match-chat",
        "stopMatchChat" : "https://api-01.wmlive.cn/api/chat/stop-match-chat",
        "joinChat" :  "https://api-01.wmlive.cn/api/chat/join-chat",
        "stopChat" : "https://api-01.wmlive.cn/api/chat/stop-chat",
        "buyGift" : "https://api-01.wmlive.cn/api/chat/buy-gift",
        "changeTopic" : "https://api-01.wmlive.cn/api/chat/change-topic",
        "dueChat" : "https://api-01.wmlive.cn/api/chat/due-chat",
        "cancelDueChat":"https://api-01.wmlive.cn/api/chat/cancel-due-chat",
        "acceptChat" :"https://api-01.wmlive.cn/api/chat/accept-chat",
        "getUserSig":"https://api-01.wmlive.cn/api/chat/get-user-sig",
        "heartBeat":"https://api-01.wmlive.cn/api/chat/heart-beat"
  },
  "aboutus":{
        "socialPact": "http://api.heihei-test.wmlives.com/static/app/social-pact.html",
        "serviceTerms": "http://api.heihei-test.wmlives.com/static/app/service-terms.html",
        "contactUs": "http://api.heihei-test.wmlives.com/static/app/contact-us.html"
  },
  "tips":{
        "pay-tips" : "提现请联系黑黑官方客服\n微信号：heiheiapp"
  },
  "sys":{
        "update" : "https://api-01.wmlive.cn/api/sys/update"
  },
  "function":{
        "chat":true
  },
  "imgPath": "http://cdn.wmlives.com",
  "actionCode": "0",
  "comment":"这里是注释"
}

```
* Error Response

    `700：参数错误`

* Example
    ```
    
    ```
    
## 系统
<span id="system"></span>

### 更新提示
* URL

 `update` `https://api.wmlives.cn/api/sys/update`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| versionCode |        | string |      | Y     |  eg：1.0.2   |
| devicesType |        | string |  android ios    | Y     |      |
| channel |        | string |    | N    |      |


* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|
|channel|渠道 |  |

* Error Response

    `700：参数错误`

* Example
有更新
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "info":{
    "force":true,
    "url":"http://cdn.wmlives.com/andoroid/heihei-1.0.4.apk",
    "title":"更新",
    "text":"新版本来了，更新吧！",
    "fileName":"heihei.apk",
    "versionCode":"1.0.4",
    "channel":"xiaomi"
  }
}
```
没有更新
```
{
  "errorcode" : 0,
  "errormsg" :"success"
}
```

### 上传日志
* URL

 `uploadLog` `https://api.wmlives.cn/api/sys/upload-log`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |    |
| log |        | string |     | Y     |      |


* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|

* Error Response

    `700：参数错误`
    
* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success"
}
```

## user
<span id="user"></span>

### 短信验证码
* URL

 `getSMSVerificationCode` `https://api.wmlives.cn/api/user/get-sms-verification-code`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| phoneNo |        | string |      | Y     |      |


* Response

| *名称*    | *参数说明* | *备注* |
|------|------|------|
|timeout| 时间| TODO |

* Error Response

    `700：参数错误`
    `400:短信发送太频繁`

* Example
```
{
  "errorcode" : 0,
  "errormsg" :"success",
  "timeout": 60 // TODO
}
```

### 微博微信登录
* URL

 `signIn` `https://api.wmlives.cn/api/user/sign-in`

* Parameters

| *名称*          | *参数说明* | *类型*   | *枚举*         | *必要性* | *备注*          |
| ------------- | ------ | ------ | ------------ | ----- | ------------- |
| accountSource | 类型     | string | Weibo,Wechat | Y     |               |
| accountToken  | token  | string |              | Y     | weibo token   |
| openId        | openId | string |              | Y     | wechat openid |
| unionId       |        | string |              | N     |               |


* Response

| *名称*        | *参数说明*            | *备注* |
| ----------- | ----------------- | ---- |
| coverUrl    | 头像                |      |
| displayName | 名字                |      |
| description | 描述                |      |
| needRegist  | 需要注册 true，否则false |      |

* Error Response

    `700: 参数错误`
    `701: weibo token无效`
    `702: openid无效`

* Example
```
{
    errorcode : 0,
    errormsg :"success",
    token:"token",
    needRegist:true,
    userInfo:{
    	id: 3176111,
        lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
    	gender: "Male",
    	birthDay: "1986-07-16",
    	level:12,
    	userType: "Normal",
    	address:"",
	    description: ""
    }
}
```


### 短信登录
* URL

 `signInCLByPhone` `https://api.wmlives.cn/api/user/sign-in-cl-by-phone`

* Parameters

| *名称*       | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ---------- | ------ | ------ | ---- | ----- | ---- |
| phoneNo    |        | string |      | Y     |      |
| verifyCode | 验证码    | string |      | Y     |      |


* Response

| *名称*        | *参数说明* | *备注* |
| ----------- | ------ | ---- |
| coverUrl    | 头像     |      |
| displayName | 名字     |      |
| description | 描述     |      |

* Error Response

    `700:参数错误`
    `401:验证码错误`

* Example

```
{
    errorcode : 0,
    errormsg :"success",
    token:"token",
    needRegist:true,
    userInfo:{
        lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
    	gender: "Male",
    	birthDay: "1986-07-16",
    	userType: "Normal",
    	address:"",
	    description: ""
    }
}
```

### 更新用户信息
* URL

 `updateUser` `https://api.wmlives.cn/api/user/update`

* Parameters

| *名称*        | *参数说明* | *类型*   | *枚举*                          | *必要性* | *备注*              |
| ----------- | ------ | ------ | ----------------------------- | ----- | ----------------- |
| token       |        | string |                               | Y     |                   |
| displayName | 昵称     | string |                               | Y     |                   |
| description | 描述     | string |                               | N     |                   |
| gender      | 性别     | string | 'Male','Female','Unspecified' | Y     |                   |
| birthDay    | 生日     | string |                               | Y     | format YYYY-MM-dd |
| address     | 定位地址   | string |                               | N     |                   |
| latlng      | 经纬度    | string |                               | N     | \|分割              |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token 无效`
    `445:非法的名称`
* Example
```
{
    errorcode:0,
    errormsg:"success",
    userId:100221
}
```

### 退出
* URL

`signOut:https://api.wmlives.cn/api/user/sign-out`
* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ----- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token 无效`

* Example

```
{
    errorcode:0,
    errormsg:"success"
}
```

### 获取用户信息
* URL

`userInfo:https://api.wmlives.cn/api/user/info`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*            |
| ----- | ------ | ------ | ---- | ----- | --------------- |
| token |        | string |      | Y     |                 |
| uid   |        | long   |      | Y     |                 |
| cuid  |        | long   |      | N     | 如果有值将会判断是否关注及拉黑 |

* Response

| *名称*           | *参数说明* | *备注* |
| -------------- | ------ | ---- |
| point          | 嘿票数    |      |
| goldCount      | 钻石数    |      |
| level          | 等级     |      |
| coverUrl       | 头像     |      |
| postCount      | 送出钻石数  |      |
| followerCount  | 粉丝数    |      |
| followingCount | 关注数    |      |
| liveCount      | 直播数    |      |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
    `736:无法查看该用户信息`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    result:{
        id:122223,
        displayName:"重千惠子",
        point:12222,
        goldCount:212,
        level:12
        coverUrl:"http://aab.ccc.com/img/12223"
        description:"自我描述",
        isFollowed:false,
        isBlocked:false,
        followerCount:1200,
        followingCount:1,
        userType:"",
        liveCount:0,
        postCount:2342,
        gender:"Male",
        birthDay:"2014-08-10"
    }
}
```

### 关注某人
* URL

`followUser:https://api.wmlives.cn/api/user/follow`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*       |
| ------ | ------ | ------ | ---- | ----- | ---------- |
| token  |        | string |      | Y     |            |
| userId |        | long   |      | Y     |            |
| liveId |        | long   |      | N     | 直播间内关注主播要加 |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 取消关注
* URL

`unfollowUser:https://api.wmlives.cn/api/user/unfollow`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| userId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 拉黑
* URL

`blockUser:https://api.wmlives.cn/api/user/block-user`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| userId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 取消拉黑
* URL

`unblockUser:https://api.wmlives.cn/api/user/unblock-user`

* Parameters

| *名称*     | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| -------- | ------ | ------ | ---- | ----- | ---- |
| token    |        | string |      | Y     |      |
| targetId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 粉丝列表
* URL

`listFollower:https://api.wmlives.cn/api/user/list-follower`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*                                     |
| --------- | ------ | ------ | ---- | ----- | ---------------------------------------- |
| token     |        | string |      | Y     |                                          |
| userId    |        | long   |      | Y     |                                          |
| offset    |        | int    |      | N     | 开始数，default：0                            |
| limit     |        | int    |      | N     | 每页个数;默认10,max:20                         |
| curUserId |        | long   |      | N     | Optional; if have value, will check current user is already follow the user in result |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    totalSize:3,
    result:[{
    	lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
    	gender: "Male",
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: "",
    	isFollowed:false
	},
	{
    	lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
    	gender: "Male",
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: "",
    	isFollowed:false
	},
	{
    	lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
    	gender: "Male",
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: ""
	}]
}
```

### 关注列表
* URL

`listFollowing:https://api.wmlives.cn/api/user/list-following`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*                                     |
| --------- | ------ | ------ | ---- | ----- | ---------------------------------------- |
| token     |        | string |      | Y     |                                          |
| userId    |        | long   |      | Y     |                                          |
| offset    |        | int    |      | N     | 开始数，default：0                            |
| limit     |        | int    |      | N     | 每页个数;默认10,max:20                         |
| curUserId |        | long   |      | N     | Optional; if have value, will check current user is already follow the user in result |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |
* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
* Example
```
{
    errorcode:0,
    errormsg:"success",
    totalSize:3,
    reslut:[{
    	lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
        level:12,
    	gender: "Male",
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: "",
    	isFollowed:false
	},
	{
    	lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
        level:12,
    	gender: "Male",
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: "",
    	isFollowed:false
	},
	{
    	llastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
        level:12,
    	gender: "Male",
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: "",
    	isFollowed:false
	}]
}
```


### 黑名单
* URL

`listBlockedUser:https://api.wmlives.cn/api/user/list-blocked-user`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*             |
| ------ | ------ | ------ | ---- | ----- | ---------------- |
| token  |        | string |      | Y     |                  |
| offset |        | int    |      | N     | 开始数，default：0    |
| limit  |        | int    |      | N     | 每页个数;默认10,max:20 |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
* Example
```
{
    errorcode:0,
    errormsg:"success",
    totalSize:1,
    result:[
    {
    	lastModified: 1408780535000,
    	displayName: "Victor Chou",
    	id: 3176111,
    	coverUrl: "http://aaa/bbb/ccc",
        region: "zh_CN",
    	gender: "Male",
    	level:12,
    	birthDay: "1986-07-16",
    	attribute: {
    	},
    	description: ""
	}]
}
```
### 举报

* URL

    `reportUser:https://api.wmlives.cn/api/usr/report-user`

* Parameters

  | *名称*       | *参数说明* | *类型*   | *枚举*                        | *必要性* | *备注* |
  | ---------- | ------ | ------ | --------------------------- | ----- | ---- |
  | token      |        | string |                             | Y     |      |
  | userId     |        | long   |                             | Y     |      |
  | reportType | 举报类型   | int    | 1:性别不符;2:广告欺诈;3:骚扰谩骂;4:淫秽色情 | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    reportmsg:"举报成功!"
}
```

### 绑定手机号

* URL

    `bindPhone:/api/user/bind-phone`

* Parameters

  | *名称*       | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ---------- | ------ | ------ | ---- | ----- | ---- |
  | token      |        | string |      | Y     |      |
  | phone      | 手机号    | string |      | Y     |      |
  | verifyCode | 验证码    | int    |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `403:手机号已被其他账户绑定`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```
### 上传设备信息
* URL
  `pushDeviceInfo:https://api-01.wmlive.cn/api/user/push-device-info`

* Parameters

| *名称*        | *参数说明* | *类型*   | *枚举*                 | *必要性* | *备注*                       |
| ----------- | ------ | ------ | -------------------- | ----- | -------------------------- |
| token       |        | string |                      | Y     |                            |
| uuid        |        | string |                      | Y     |                            |
| apnsType    |        | string | "apns","getui","gcm" | Y     | 使用 ‘getui’                 |
| apnsToken   |        | string |                      | Y     | ios传apnstoken,android 传cid |
| deveiceType |        | string | "android,ios"        | Y     |                            |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```


## social

### 首页广告
* URL

`getBanner:https://api.wmlives.cn/api/social/get-banner`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ----- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |      |


* Response

| *名称*       | *参数说明* | *备注*                         |
| ---------- | ------ | ---------------------------- |
| expireTime | 有效期    | 单位秒                          |
| desc       | 标题     |                              |
| type       | int 类型 | 1-user 2-live 3-url          |
| link       | string | deep link for different type |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:84600,
    banners:[{
        desc:"desc",
        cover:"imgpath",
        type:1,
        link:"ycl://live/1232112"
    }]
}
```

## live
<span id="live"></span>

### 直播推荐列表
* URL

`listLiveByRecommend:https://api.wmlives.cn/api/live/list-live-by-recommend`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ----- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |      |

* Response

| *名称*         | *参数说明* | *备注*      |
| ------------ | ------ | --------- |
| expireTime   | 有效期    | 单位秒       |
| creatorCover | 封面     |           |
| streamAddr   | 流地址    |           |
| shareAddr    | 分享地址   |           |
| lookbackAddr | 回放地址   |           |
| status       | 状态     | 1:直播;2:回放 |
| onlineUser   | 在线数    |           |
| viewernum    | 观看人数   |           |
| roomId       | 房间号    | int       |
| liveskback   | 回放json |           |


* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:60,
    lives:[
      {
        "status": 1,
      "userName": "呵呵哒",
      "liveId": 1577899525,
      "title": "来听我直播~",
      "gender": "Male",
      "streamAddr": "http://back.wmlive.cn:8000/live/1577899525.flv?sign=1473418685-bacebe11090b31f1e01c18900920763e",
      "userId": 14,
      "totalTickets": "0",
      "totalUsers": 0,
      "visible": 1,
      "length": null,
      "birthDay": "2016-09-08",
      "deviceType": null,
      "shareAddr": "https://api-01.wmlive.cn/html/live.html?liveid=1577899525&sign=4c81b16486c463941fb745938849cf37",
      "address": "",
      "onlineUsers": 1,
      "lookbackAddr": "",
      "isrecomm": 0,
      "roomId": 1577899525,
      "createTime": "2016-09-09 14:48:06"
      }],
    liveskback:[
      {
       "status": 2,
      "userName": "回到家大家回电话",
      "liveId": 842017421,
      "title": "好多好多好多",
      "gender": "Female",
      "streamAddr": "http://back.wmlive.cn:8000/live/842017421.flv?sign=1473418023-62d4673652a9b32e8c41ab52f6b367c8",
      "userId": 9,
      "totalTickets": "0",
      "totalUsers": 0,
      "visible": 1,
      "length": null,
      "birthDay": "2015-07-03",
      "deviceType": null,
      "shareAddr": "https://api-01.wmlive.cn/html/live.html?liveid=842017421&sign=b23b1f5ddc7b9e7fe3e180f9781df68e",
      "address": "",
      "onlineUsers": 0,
      "lookbackAddr": "",
      "isrecomm": 0,
      "roomId": 842017421,
      "createTime": "2016-09-09 14:37:04"
      }
    ]
}
```

### 创建直播
* URL

`createLive:https://api.wmlives.cn/api/live/create-live`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ----- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |      |
| title |        | string |      | Y     |      |

* Response

| *名称*         | *参数说明* | *备注*                                     |
| ------------ | ------ | ---------------------------------------- |
| liveId       | 直播ID   |                                          |
| streamAddr   | 收听地址   |                                          |
| shareAddr    | 分享地址   |                                          |
| lookbackAddr | 回放地址   |                                          |
| roomId       | 房间号    |                                          |
| status       | 状态     | 0-to be start 1-playing  2-stoped  3-baned 4-delete（主播自己设置删除标识） |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    live:{
        "status" : 0,
        "liveId" : 13456,
        "title" :  "title",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        visible:1
    },
    share:{
        wechat:{
            title:"嘿嘿直播",
            content:"xxx 正在直播",
            url:"",
            "coverUrl":""
        },
        weibo:{
            title:"嘿嘿直播",
            content:"xxx 正在直播",
            url:"",
            "coverUrl":""
        },
        friend:{
            title:"嘿嘿直播",
            content:"xxx 正在直播",
            url:"",
            "coverUrl":""
        }
    }
}
```

### 更新直播
* URL

`changeLive:https://api.wmlives.cn/api/live/change-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |
| title  |        | string |      | Y     |      |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `711:用户权限不足`

* Example
```
{
    errorcode:0,
    errormsg:"success"
    live:{
        "status" : 1,
        "liveId" : 13456,
        "title" :  "title",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        visible:1
    }
}
```


### 结束直播
* URL

`stopLive:https://api.wmlives.cn/api/live/stop-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `711:用户权限不足`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    live:{
        "status" : 2,
       "liveId" : 13456,
        "title" :  "title",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        visible:1,
        totalUsers :  23213,     
        totalTickets :  123213,
        liveTotalTicket:232,
        onlineUsers:1221
    },
    share:{
        "weibo": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播"
        },
        "wechat": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播"
        },
        "friend": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播"
        }
    }
}
```


### 删除直播
* URL

`deleteLive:https://api.wmlives.cn/api/live/delete-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `711:用户权限不足`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    live:{
        "status" : 4,
        "liveId" : 13456,
        "title" :  "title",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        visible:1
    }
}
```

### 设置直播可见
* URL

`setLiveVisible:https://api.wmlives.cn/api/live/set-live-visible`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*       |
| ------- | ------ | ------ | ---- | ----- | ---------- |
| token   |        | string |      | Y     |            |
| liveId  |        | long   |      | Y     |            |
| visible |        | int    | 0；1  | Y     | 0：不可见；1：可见 |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `711:用户权限不足`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    live:{
        "status" : 2,
        "liveId" : 13456,
        "title" :  "title",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        visible:1
    }
}
```

### 获取直播
* URL

`getLive:https://api.wmlives.cn/api/live/get-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    "live": {
        "status": 1,
        "userName": "回到家大家回电话",
        "liveId": 842017421,
        "title": "好多好多好多",
        "streamAddr": "http://back.wmlive.cn:8000/live/842017421.flv?sign=1473418023-62d4673652a9b32e8c41ab52f6b367c8",
        "userId": 9,
        "totalTickets": "15",
        "totalUsers": 4,
        "expireTime": 10,
        "visible": 1,
        "length": null,
        "deviceType": null,
        "shareAddr": "https://api-01.wmlive.cn/html/live.html?liveid=842017421&sign=b23b1f5ddc7b9e7fe3e180f9781df68e",
        "address": "",
        "onlineUsers": 3,
        "lookbackAddr": "",
        "roomId": 842017421,
        "createTime": "2016-09-09 14:37:04",
        "livetotalticket": "15"
        },
      "userInfo": {
        "description": "",
        "isFollowed": false,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-14.png",
        "user_type": "Anchor",
        "address": "",
        "id": 9,
        "user_status": "Published",
        "displayName": "回到家大家回电话",
        "level": 0,
        "gender": "Female",
        "region": null,
        "birthDay": "2015-07-03",
        "lastModified": 1473584241
      }
}
```

### 加入直播
* URL

`joinLive:https://api.wmlives.cn/api/live/join-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `725:live is not inactive`
    `737:无法观看该用户直播`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    live:{
        "status" : 1,
        "liveId" : 13456,
        "title" :  "清水出芙蓉，天然去雕饰",
        "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
        "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
        "shareAddr" :  "http://live.wmlive.cn/s/?userid=38298237&liveid=1462006378736119&ctime=1462006378",
        "lookbackAddr" :  "",
        "userId" :  38298237,
        "roomId" :  123213,
        "status" :  2,
        "totalUsers" :  23213,     
        "totalTickets" :  123213,
        onlineUsers:1111
    },
    share:{
        "weibo": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播"
        },
        "wechat": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播"
        },
        "friend": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播"
        }
    }
}
```

### 开始直播
* URL

`startLive:https://api.wmlives.cn/api/live/start-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:直播无效`
    `711:用户权限不足`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 心跳
* URL
>TODO
>`heartBeat:https://api.wmlives.cn/api/live/heart-beat` 

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| --------- | ------ | ------ | ---- | ----- | ---- |
| token     |        | string |      | Y     |      |
| liveId    |        | long   |      | Y     |      |
| isCreator |        | int    |      | Y     |      |


* Response

| *名称*        | *参数说明* | *备注* |
| ----------- | ------ | ---- |
| nextTimeout | 时间间隔   | 秒    |

* Error Response

    `700:参数错误`
    `711:用户权限不足`
    `720:token无效`
    `731:直播无效`
    `725:live is not inactive`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    liveId:1121323,
    nextTimeout:15
}
```

### 我的/ta的直播
* URL

`listLiveByUser:https://api.wmlives.cn/api/live/list-live-by-user`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*                                     |
| ------ | ------ | ------ | ---- | ----- | ---------------------------------------- |
| token  |        | string |      | Y     |                                          |
| offset |        | int    |      | N     | 开始数，default：0                            |
| limit  |        | int    |      | N     | 每页个数;默认10,max:20                         |
| userId |        | long   |      | Y     | Option. if no userId,server will return the lives of operator |

* Response

| *名称*       | *参数说明* | *备注*          |
| ---------- | ------ | ------------- |
| isFollowed | 是否关注   | 查看ta的直播的时候起作用 |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:120,
    totalCount:2,
    lives:[
        {
            "creatorId" : 38298237,
            "creatorName" : "清风",
            "creatorCover" : "http://cdn.wmlive.cn/c/de343dab23423258.jpg",
            "liveId" : 23128979,
            "title" : "清风告诉你",
            "liveCity" : "长沙",
            "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
            "shareAddr" :  "http://live.wmlive.cn/s/?userid=38298237&liveid=1462006378736119&ctime=1462006378",
            "lookbackAddr" :  "",
            "roomId" :  1342467,
            "status" :  1,
            "onlineUser" :  1342
        },
        {
            "creatorId" : 382982,
            "creatorName" : "明月",
            "creatorCover" : "http://cdn.wmlive.cn/c/ed3443dab23423258.jpg",
            "liveId" : 333128979,
            "liveName" : "明月告诉你",
            "liveCity" : "武汉",
            "streamAddr" :  "http://pull.wmlive.cn/live/3362006378736119.flv",
            "shareAddr" :  "http://live.wmlive.cn/s/?userid=382982&liveid=333128979&ctime=1462008378",
            "lookbackAddr" :  "", 
            "roomId" :  1342469,
            "status" :  1,
            "onlineUser" :  13422
        }]
}
```

### 观看直播用户列表
* URL

`listLiveUsers:https://api.wmlives.cn/api/live/list-live-users`

* Parameters

| *名称*         | *参数说明* | *类型*   | *枚举* | *必要性* | *备注*              |
| ------------ | ------ | ------ | ---- | ----- | ----------------- |
| token        |        | string |      | Y     |                   |
| liveId       |        | long   |      | Y     |                   |
| lastJoinTime |        | long   |      | N     | Default:0         |
| direction    |        | int    | 0,1  | N     | 0获取最新向右划，1获取之前向左划 |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `710:用户不存在`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:60,
    users:[
      {
         id:1229,
         name:"倔强的白羊",
         isFollowed:true,
         coverUrl:"http://aab.ccc.com/img/12223",
         gender: "Male",
         birthDay: "1986-07-16",
         joinTime:1233214123
      },
      {
         id:1229,
         name:"倔强的白羊",
         isFollowed:true,
         coverUrl:"http://aab.ccc.com/img/12223",
         gender: "Male",
         birthDay: "1986-07-16",
         joinTime:1233214123
      },
      {
          id:1229,
         name:"倔强的白羊",
         isFollowed:true,
         coverUrl:"http://aab.ccc.com/img/12223",
         gender: "Male",
         birthDay: "1986-07-16",
         joinTime:1233214123
      }
    ]
}
```

### 礼物列表
* URL

`giftInfo:https://api.wmlives.cn/api/live/gift-info`

* Parameters

| *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ----- | ------ | ------ | ---- | ----- | ---- |
| token |        | string |      | Y     |      |

* Response

| *名称*  | *参数说明*                      | *备注*                           |
| ----- | --------------------------- | ------------------------------ |
| gold  | int                         | 购买价格                           |
| exp   | exp to reach the next level |                                |
| cl    | [int,int,int]               | backgroud color by RGB         |
| image | string                      | 动画图片                           |
| icon  | string                      | 列表图片                           |
| type  | 类型                          | 1-static show  2-movement show |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:60,
    gifts:[
      {
        id : 123,
        name : "小黄瓜",
        gold : 1,
        exp: 10,
        cl: [255,255,255],
        image : "231231231.jpg",
        icon:  "8abcd2345.jpg",
        type:  1
      },
      {
        id : 123,
        name : "小黄瓜",
        gold : 1,
        exp: 10,
        cl: [255,255,255],
        image : "231231231.jpg",
        icon:  "8abcd2345.jpg",
        type:  1
      }
    ]
}
```

### 赠送礼物
* URL

`buyGift:https://api.wmlives.cn/api/live/buy-gift`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性*         | *备注* |
| --------- | ------ | ------ | ---- | ------------- | ---- |
| token     |        | string |      | Y             |      |
| giftId    |        | int    |      | Y             |      |
| liveId    |        | string |      | Y             |      |
| amount    |        | int    |      | N             | 连送数  |
| gift_uuid |        | string | N    | 连送唯一标识，由客户端控制 |      |

* Response

| *名称* | *参数说明* | *备注* |
| ---- | ------ | ---- |
| gold | 剩余钻石数  |      |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
    `730:礼物不存在`
    `721:用户账户异常`
    `740:余额不足`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    gold:2
}
```

### 发送小喇叭消息
* URL

`buyBullet:https://api.wmlives.cn/api/live/buy-bullet`

* Parameters

| *名称*    | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------- | ------ | ------ | ---- | ----- | ---- |
| token   |        | string |      | Y     |      |
| liveId  |        | string |      | Y     |      |
| message |        | string |      | Y     |      |

* Response

| *名称* | *参数说明* | *备注* |
| ---- | ------ | ---- |
| gold | 剩余钻石数  |      |

* Error Response

    `700:参数错误`
    `720:token无效`
    `721:用户账户异常`
    `740:余额不足`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    gold:1
}
```

### 点亮
* URL

`liveLike:https://api.wmlives.cn/api/live/live-like`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举*        | *必要性* | *备注* |
| ------ | ------ | ------ | ----------- | ----- | ---- |
| token  |        | string |             | Y     |      |
| type   |        | int    | 1:a;2:b;3:c | Y     |      |
| liveId |        | string |             | Y     |      |


* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 直播分享

* URL

`shareLive:https://api.wmlives.cn/api/live/share-live`

* Parameters

| *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
| ------ | ------ | ------ | ---- | ----- | ---- |
| token  |        | string |      | Y     |      |
| liveId |        | long   |      | Y     |      |

* Response

|*名称*|*参数说明*|*备注*|
| --- | --- | --- |


* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success",
   share:{
        "weibo": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播",
          "coverUrl":""
        },
        "wechat": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播",
          "coverUrl":""
        },
        "friend": {
          "content": "嘿嘿直播 正在直播",
          "url": "https://api-01.wmlive.cn/html/live.html?liveid=1956641931&sign=657be2468beca3a2b0be99b987760102&uid=6",
          "title": "嘿嘿直播",
          "coverUrl":""
        }
   }
}
```

### 禁言

* URL

    `shutupUser:https://api.wmlives.cn/api/live/shutupuser`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |
  | userId |        | long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 取消禁言

* URL

    `shutupOpen:https://api.wmlives.cn/api/live/shutupopen`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |
  | userId |        | long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 是否禁言

* URL

    `isshutup:https://api.wmlives.cn/api/live/isshutup`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |
  | userId |        | long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    isshutup:1 # 1:是 2:否
}
```

### 暂停直播

* URL

    `pauseLive:https://api.wmlives.cn/api/live/pause-live`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    `711:用户权限不足`
    `735:直播已结束`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 继续直播

* URL

    `continueLive:https://api.wmlives.cn/api/live/continue-live`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    `711:用户权限不足`
    `735:直播已结束`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 退出直播 观看段退出调用

* URL

    `quitLive:https://api.wmlives.cn/api/live/quit-live`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 退出直播 观看段退出调用

* URL

    `quitLive:https://api.wmlives.cn/api/live/quit-live`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 回放观看用户列表

* URL

   `listReplayUsers:https://api.wmlives.cn/api/live/list-replay-users`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `731:无效的直播`
    

* Example
```
{
    errorcode:0,
    errormsg:"success",
    users:[
        {
          "description": "沟沟壑壑",
          "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-16.png",
          "user_type": "Anchor",
          "address": "北京市",
          "id": 57,
          "isFollowed": false,
          "user_status": "Published",
          "displayName": "婷婷手机号",
          "level": 0,
          "gender": "Female",
          "region": null,
          "birthDay": "2016-08-12",
          "lastModified": 1476247060
        },
        {
          "description": "没有什么不可以",
          "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-9.png",
          "user_type": "Anchor",
          "address": "北京市",
          "id": 30,
          "isFollowed": false,
          "user_status": "Published",
          "displayName": "shin1",
          "level": 0,
          "gender": "Male",
          "region": null,
          "birthDay": "1985-05-01",
          "lastModified": 1474960547
        },
        {
          "description": "",
          "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-2.png",
          "user_type": "Anchor",
          "address": "",
          "id": 10021,
          "isFollowed": false,
          "user_status": "Published",
          "displayName": "小宋手机号么么哒",
          "level": 0,
          "gender": "Female",
          "region": null,
          "birthDay": "2014-01-09",
          "lastModified": 1476243481
        }
    ]
}
```

## payment

<span id="payment"></span>

### 充值列表页

* URL

    `listPackage:https://api.wmlives.cn/api/payment/list-package` 

* Parameters

  | *名称*    | *参数说明* | *类型*   | *枚举*                    | *必要性* | *备注* |
  | ------- | ------ | ------ | ----------------------- | ----- | ---- |
  | token   |        | string |                         | Y     |      |
  | channel |        | string | “alipay”,”wechat”,”iap” | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    packages: [
        {
                id:120
                channel:"wechat"
                productId:"productId_60"
                desc:"描述",
                gold:60,
                payMoney:600
                originMoney:600
         },{
                id:121
                channel:"wechat"
                productId:"productId_380"
                desc:"描述",
                gold:380,
                payMoney:38000
                originMoney:38000
         },{
                id:122
                channel:"wechat"
                productId:"productId_980"
                desc:"送10钻",
                gold:980,
                payMoney:97000
                originMoney:98000
        }
    ]
}
```

### 创建订单

* URL

    `createOrder:/api/payment/create-order`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举*                    | *必要性* | *备注* |
  | --------- | ------ | ------ | ----------------------- | ----- | ---- |
  | token     |        | string |                         | Y     |      |
  | packageId |        | int    |                         | Y     |      |
  | channel   |        | string | “alipay”,”wechat”,”iap” | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `726:invalid packageId`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    order:"orderid",
    data:"userId=%s&packageId=%s&channel=%s&payMoney=%s",
    productId:"productId_980"
}
```

### 订单通知

* URL

    `orderNotify:/api/payment/order-notify`

* Parameters

  | *名称*   | *参数说明*                             | *类型*   | *枚举*           | *必要性* | *备注* |
  | ------ | ---------------------------------- | ------ | -------------- | ----- | ---- |
  | token  |                                    | string |                | Y     |      |
  | order  |                                    | string |                | Y     |      |
  | status |                                    | string | 1-支付成功  2-支付失败 | Y     |      |
  | data   | the info returned from payment SDK | string |                | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `727:invalid order`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    order:"orderid"
}
```

### 积分兑换钻石的package


* URL

    `listP2gPackage:/api/payment/list-p2g-package`

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    packages:[
        {
            id:122,
            desc:"miaoshu",
            point:100,
            gold:70
        },
        {
            id:122,
            desc:"miaoshu",
            point:100,
            gold:70
        }
    ]
}
```
### 积分兑换钻石


* URL

    `p2g:/api/payment/p2g`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | --------- | ------ | ------ | ---- | ----- | ---- |
  | token     |        | string |      | Y     |      |
  | packageId |        | int    |      | Y     |      |

* Response

  | *名称*  | *参数说明* | *备注*    |
  | ----- | ------ | ------- |
  | point | int    | 剩余point |
  | order | string | order   |

* Error Response

    `700:参数错误`
    `721:用户账户异常`
    `720:token无效`
    `741:积分不足`
    `726:invalid package`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    order:"23",
    point:12
}
```

### 我的账户资产

* URL

    `statistic:/api/payment/statistic`

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |

* Response

  | *名称*          | *参数说明*  | *备注* |
  | ------------- | ------- | ---- |
  | gold          | 钻石数     |      |
  | point         | 黑票      |      |
  | allOutlayGold | 全部钻石数   |      |
  | allEarnPoint  | 全部赚取的黑票 |      |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    gold:122,
    point:324223,
    pointWorth:324,
    allOutlayGold:2332,
    allEarnPoint:333
}
```

### 获取支付宝信息

* URL

    `getAlipayInfo:/api/payment/get-alipay-info`

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    info:{
        alipaycode:"wuyongwen",
        name:"张三",
        idcard:"10102189873432",
        phone:"13533221223"
    }
}
```

### 验证支付宝

* URL

    `verifyAlipay:/api/payment/verify-alipay`

* Parameters

  | *名称*       | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ---------- | ------ | ------ | ---- | ----- | ---- |
  | token      |        | string |      | Y     |      |
  | alipaycode |        | string |      | Y     |      |
  | username   |        | string |      | Y     |      |
  | idcard     |        | string |      | Y     |      |
  | phone      |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `726:验证不通过`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    alipayCode:"12912303"
}
```
### 提现金额

* URL

    `cash-info:/api/payment/cash-info`

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |

* Response

  | *名称* | *参数说明* | *备注* |
  | ---- | ------ | ---- |
  | cash | int    | 分    |

* Error Response

    `700:参数错误`
    `720:token无效`
    `721:用户账户异常`
    `740:余额不足`

* Example

```
{
    errorcode:0,
    errormsg:"success",
    point:1222,
    cash:1000,
    rule:"提现规则：..."
}
```

### 提现请求

* URL

    `payReq:/api/payment/pay-req`

* Parameters

  | *名称*       | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ---------- | ------ | ------ | ---- | ----- | ---- |
  | token      |        | string |      | Y     |      |
  | alipaycode |        | string |      | Y     |      |
  | payamount  |        | int    |      | Y     | 分    |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `726:invalid alipaycode`
    `721:用户账户异常`
    `740:余额不足`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    reqmsg:"提现申请已提交"
}
```

## chat

<span id="chat"></span>


### 开始匹配

* URL

`matchChat:/api/chat/match-chat`

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    "expireTime": 15,
    "errorcode": 0,
    "tips": [
        "相互勾搭的最好方式是送礼物，嘻嘻?",
        "我跟你说：聊骚不一定会被打死的?",
        "我脾气好多了，不然聊骚的现在都住院了?",
        "不好好说话，五姑娘永远陪伴?",
        "你说的对，但是我不听你的?",
        "碰到讨厌的人一定要拉出去枪毙?"
      ],
    "errormsg": "success"
}
```

### 停止匹配

* URL

`stopMatchChat:/api/chat/stop-match-chat`

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 加入对话

* URL

`joinChat:/api/chat/join-chat`

> 收到joinChat message后才可调用，其他情况不得调用

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId | 对话ID   | string |      | Y     |      |

* Response

  | *名称*   | *参数说明*     | *备注*     |
  | ------ | ---------- | -------- |
  | status | 用户是否已经进入房间 | 0:正在进入房间 |
  | roomId | 房间号        |          |

* Error Response

    `700:参数错误`
    `720:token无效`
    `chat无效`

* Example

```
{
   "errorcode": 0,
  "errormsg": "success",
  "chat": {
    "status": 0,
    "pushAddr": "",
    "title": "",
    "streamAddr": "",
    "initTopic": "快来相互调戏吧~",
    "visible": 1,
    "archiveFile": null,
    "startTime": "2016-09-23 20:26:00",
    "users": [
      {
        "status": 0,
        "description": "明年😖😘😘😘😍😍",
        "point": 1005325,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-9.png",
        "user_type": "Anchor",
        "address": "",
        "id": 13,
        "isFollowed": false,
        "user_status": "Published",
        "displayName": "一克拉金",
        "level": 1,
        "gender": "Male",
        "region": null,
        "birthDay": "2013-05-01",
        "lastModified": 1474258613
      },
      {
        "status": 0,
        "description": "",
        "point": 1253933,
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-14.png",
        "user_type": "Anchor",
        "address": "",
        "id": 50,
        "isFollowed": false,
        "user_status": "Published",
        "displayName": "太累了新狼围脖儿",
        "level": 0,
        "gender": "Female",
        "region": null,
        "birthDay": "2016-07-01",
        "lastModified": 1474788176
      }
    ],
    "roomId": 178400656888855408,
    "createTime": "2016-09-23 20:26:00",
    "chatId": 178400656888855408
  }
}
```

### 更换话题

* URL

`changeTopic:/api/chat/change-topic`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId | 对话ID   | long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 结束对话

* URL

`stopChat:/api/chat/stop-chat`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId |        | Long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 对话送礼物

* URL

`buyGift:/api/chat/buy-gift`

* Parameters

| *名称*      | *参数说明* | *类型*   | *枚举* | *必要性*         | *备注*        |
| --------- | ------ | ------ | ---- | ------------- | ----------- |
| token     |        | string |      | Y             |             |
| giftId    |        | int    |      | Y             |             |
| chatId    |        | long   |      | Y             |             |
| userId    |        | long   |      | Y             |             |
| amount    |        | int    |      | N             | 连送数,客户端自己记录 |
| gift_uuid |        | string | N    | 连送唯一标识，由客户端控制 |             |

* Response

| *名称* | *参数说明* | *备注* |
| ---- | ------ | ---- |
| gold | 剩余钻石数  |      |

* Error Response

    `700:参数错误`
    `720:token无效`
    `710:用户不存在`
    `730:礼物不存在`
    `721:用户账户异常`
    `740:余额不足`
    `732:无效的对话`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    gold:2
}
```

### 约聊

* URL

`dueChat:/api/chat/due-chat`

> 约聊对方如果对方正在直播，返回738错误码；如果对方正在约聊状态或正在被第三者约聊返回739错误码；
> 如果约聊的对方也正在约聊发起者则自动下发joinChat message,客户端收到后调用joinchat接口；
> 客户端发起约聊后进入等待倒计时状态，取消需要调用cancelDueChat接口，倒计时期间等待joinChat消息，倒计时结束后忽略此消息

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | userId |        | Long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `738:该用户正在直播`
    `739:对方太火，忙线中~`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:15,
    chatId:12324421341533
}
```

### 停止正在约聊

* URL

`cancelDueChat: /api/chat/cancel-due-chat`

> 客户端发起约聊后进入等待倒计时状态，取消需要调用cancelDueChat接口，倒计时期间等待joinChat消息，倒计时结束后忽略此消息

* Parameters

  | *名称*  | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ----- | ------ | ------ | ---- | ----- | ---- |
  | token |        | string |      | Y     |      |
  | chatId |        | long |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`
    `711:权限不足`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 前往约聊

* URL

`acceptChat:/api/chat/accept-chat`

>客户端发起请求后等待动作消息(joinChat message),客户端收到消息后调用joinChat接口


* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId |        | int    |      | Y     |      |
  | userId | 约聊对象   | int    |      | Y     |      |
  | type   |        | int    |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    expireTime:15
}
```

### 对聊心跳

* URL

`heartBeat:/api/chat/heart-beat`

>在joinchat接口完成后调用，每次调用周期以'nextTimeout'值为准

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId |        | Long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`

* Example
```
{
    errorcode:0,
    errormsg:"success",
    nextTimeout：5
}
```

### 对聊暂停

* URL

`pauseChat:/api/chat/pause-chat`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId |        | Long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 对聊继续

* URL

`continueChat:/api/chat/continue-chat`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | chatId |        | Long   |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `732:对话无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

## message
<span id="message"></span>

### sendMsg

* URL
>直播间内发送普通消息

`sendMsg:/api/msg/send-msg`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | text   |        | string |      | Y     |      |
  | roomId |        | string |      | Y     |      |
  | liveId |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`
    `733:room无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### messageList

> websocket 重连后拉取全部消息，socket连接状态下，等待socket中action=message的消息，客户端自己处理

* URL

`messageList:/api/msg/message-list`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
  "errorcode": 0,
  "errormsg": "success",
  "messages": [
    {
      "fromUserId": 63,
      "fromUserName": "这里",
      "gender": "Male",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-19.png",
      "data": {
        "count": 1,
        "type": "post"
      },
      "birthDay": "2014-09-25",
      "link": "wmlives_heihei://duechat?uid=63",
      "timeStamp": 1477557322,
      "action": "message",
      "msgType": "action",
      "text": null
    },
    {
      "fromUserId": 10031,
      "fromUserName": "小宋手机号1",
      "gender": "Female",
      "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-2.png",
      "data": {
        "count": 5,
        "type": "calling"
      },
      "birthDay": "2016-01-01",
      "link": "wmlives_heihei://duechat?uid=10031",
      "timeStamp": 1477557274,
      "action": "message",
      "msgType": "action",
      "text": null
    }
  ]
}
```

### messageDel

> 删除对某人的约聊记录

* URL
`messageDel:/api/msg/message-del`
    
* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | userId   |        | long |      | Y     |      |
  

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### 已读全部消息

* URL
>直播间内发送普通消息

`messageReadAll:/api/msg/message-read-all`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`


* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### ~~historyMsg~~

>历史消息，分为已读消息与未读消息，已读消息最大返回100条，客户端应该在socket重连后调用该接口；
>通过socket接收到的未读消息，客户端自行处理未读消息数

* URL

`historyMsg:/api/msg/history-msg`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{ 
  "unReadCount": 2,
  "errormsg": "success",
  "errorcode": 0,
  "unReadMsg": [
    {
      "msg": {
        "comment": "约你私聊",
        "fromUserId": 47,
        "fromUserName": "嘿嘿一笑",
        "gender": "Male",
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-3.png",
        "needstore": true,
        "getuiAction": "duechat",
        "expireTime": 15,
        "birthDay": "2015-01-23",
        "msgType": "action",
        "msgId": 1865290063436513696,
        "action": "due-chat-notify",
        "type": 0,
        "chatId": 2627049573665376037
      },
      "timeStamp": 1476182076
    },
    {
      "msg": {
        "comment": "约你私聊",
        "fromUserId": 47,
        "fromUserName": "嘿嘿一笑",
        "gender": "Male",
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-3.png",
        "needstore": true,
        "getuiAction": "duechat",
        "expireTime": 15,
        "birthDay": "2015-01-23",
        "msgType": "action",
        "msgId": 2996271861006133716,
        "action": "due-chat-notify",
        "type": 0,
        "chatId": 1451567810014728454
      },
      "timeStamp": 1476181414
    }
  ],
  "readMsg": [
    {
      "msg": {
        "comment": "约你私聊",
        "fromUserId": 47,
        "fromUserName": "嘿嘿一笑",
        "gender": "Male",
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-3.png",
        "needstore": true,
        "getuiAction": "duechat",
        "expireTime": 15,
        "birthDay": "2015-01-23",
        "msgType": "action",
        "msgId": 2996271861006133716,
        "action": "due-chat-notify",
        "type": 0,
        "chatId": 1451567810014728454
      },
      "timeStamp": 1476181414
    },
    {
      "msg": {
        "comment": "约你私聊",
        "fromUserId": 47,
        "fromUserName": "嘿嘿一笑",
        "gender": "Male",
        "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-3.png",
        "needstore": true,
        "getuiAction": "duechat",
        "expireTime": 15,
        "birthDay": "2015-01-23",
        "msgType": "action",
        "msgId": 1865290063436513696,
        "action": "due-chat-notify",
        "type": 0,
        "chatId": 2627049573665376037
      },
      "timeStamp": 1476182076
    }
  ]
}
```

### ~~删除消息~~

* URL
>直播间内发送普通消息

`deleteMsg:/api/msg/delete-msg`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | msgId   |        | long |      | Y     |      |
  

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```


### ~~已读一条消息~~

* URL
>直播间内发送普通消息

`readOneMsg:/api/msg/read-one-msg`

* Parameters
 | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |
  | msgId   |        | long |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```


### ~~已读全部消息~~

* URL
>直播间内发送普通消息

`readAllMsg:/api/msg/read-all-msg`

* Parameters

  | *名称*   | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | ------ | ------ | ------ | ---- | ----- | ---- |
  | token  |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `720:token无效`


* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```


### ~~open room~~

* URL

`messageserver/api/msg/open-room.action`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | --------- | ------ | ------ | ---- | ----- | ---- |
  | roomId    |        | string |      | Y     |      |
  | signature |        | string |      | Y     |      |
  | liveId    |        | string |      | N     |      |
  | chatId    |        | string |      | N     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `701:signature错误`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### ~~close room~~

* URL

`messageserver/api/msg/close-room.action`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | --------- | ------ | ------ | ---- | ----- | ---- |
  | roomId    |        | string |      | Y     |      |
  | signature |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `701:signature错误`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### sever send message 

> 服务端接口

* URL

`messageserver/api/msg/send-msg.action`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | --------- | ------ | ------ | ---- | ----- | ---- |
  | signature |        | string |      | Y     |      |
  | data      | 见消息数据  | json   |      | Y     |      |

* request

    

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `701:signature错误`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### ~~start live broadcast~~

* URL

`messageserver/api/msg/start-live-broadcast.action`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | --------- | ------ | ------ | ---- | ----- | ---- |
  | liveId    |        | string |      | Y     |      |
  | roomId    |        | string |      | Y     |      |
  | signature |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `701:signature错误`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```

### ~~stop live broadcast~~

* URL

`messageserver/api/msg/stop-live-broadcast.action`

* Parameters

  | *名称*      | *参数说明* | *类型*   | *枚举* | *必要性* | *备注* |
  | --------- | ------ | ------ | ---- | ----- | ---- |
  | liveId    |        | string |      | Y     |      |
  | roomId    |        | string |      | Y     |      |
  | signature |        | string |      | Y     |      |

* Response

    |*名称*|*参数说明*|*备注*|
    | --- | --- | --- |

* Error Response

    `700:参数错误`
    `701:signature错误`

* Example
```
{
    errorcode:0,
    errormsg:"success"
}
```


### 消息数据定义

<span id="message-str"></span>


#### 消息服务器接受消息结构

* 发送给个人

  ``` json
    {
        timeStamp:1400939322323,
        type:'tosingle', 
        targetUserId:221,
        msg:{
           // 客户端消息结构
        }
    }
  ```

* 房间消息广播

>黑聊广播消息

``` 
    {
        timeStamp:1400939322323,
        type:'toChat',
        chatId:123,
        msg:{
            // 客户端消息结构
        }
    }
```

>直播广播消息

``` 
    {
        timeStamp:1400939322323,
        type:'toLive',
        liveId:123,
        msg:{
            // 客户端消息结构
        }
    }
```

#### 客户端接受消息结构

>客户端根据不同的消息类型做出不同的相应

* toast弹窗消息

    ```
    msg : {
        msgType:"toast",
        text:"弹窗提示内容 \n 我是黑黑",
        expireTime:3
    }
    ```
    
     **expireTime** ： 持续时间（秒）

* 礼物

    ```
    msg : {
        msgType:"gift",
        amount:128,
        giftId:12,
        roomId:123, // client需判断当前roomid
        fromUserId:1233,
        fromUserName:"谁送的",
        gender: "Male",
        totalTicket:123322,
        gift_uuid:"adfd32ffa424",
            "msgId":12222221334124
    }
    ```
* 普通消息

    ```
    msg : {
        msgType:"text",
        fromUserId:122,
        fromUserName:'张三',
        gender: "Male",
        coverUrl: "http://aaa/bbb/ccc",
        text:"hello",
            "msgId":12222221334124
        roomId:123 // client需判断当前roomid
    }
    ```
* 弹幕消息

    ```
    msg : {
        msgType:"barrage",
        fromUserId:122,
        fromUserName:'张三',
        gender: "Male",
        birthDay: "",
        coverUrl: "http://aaa/bbb/ccc",
        text:"hello",
        roomId:123,
        totalTicket:123322,
            "msgId":12222221334124
    }
    ```
* 弹幕消息

    ```
    msg : {
        msgType:"like",
        text:"hello",
        fromUserId:122,
        fromUserName:'张三',
        gender: "Male",
        birthDay: "",
        coverUrl: "http://aaa/bbb/ccc",
            "msgId":12222221334124
        roomId:123 // client需判断当前roomid
    }
    ```
* 系统通知消息

    ```
    msg : {
        msgType:"system",
        text:"hello",
            "msgId":12222221334124
    }
    ```
* 动作消息

    ```
    msg : {
        msgType:"action",
        action:"join-chat",
        comment:"加入对聊",
            "msgId":12222221334124
        chatId:123
    }
    ```
* 动作消息

    ```
    msg : {
        msgType:"action",
        action:"due-chat-notify",
        comment:"约聊通知消息",
        expireTime:15,  //  持续时常
        chatId:123,
        fromUserId:122,
        fromUserName:'张三',
        gender: "Male",
        birthDay: "",
        coverUrl: "http://aaa/bbb/ccc",
        "msgId":12222221334124
        type:1  // type 0:第一次约聊 1:反向约聊
    }
    ```
* 动作消息

    ```
    msg : {
        msgType:"action",
        action:"chat-user-status",
        comment:"对聊用户状态",
        chatId:122,
        "msgId":12222221334124
        
        "users": [
          {
            "status": 0,
            "description": "明年😖😘😘😘😍😍",
            "point": 1005325,
            "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-9.png",
            "user_type": "Anchor",
            "address": "",
            "id": 13,
            "isFollowed": false,
            "user_status": "Published",
            "displayName": "一克拉金",
            "level": 1,
            "gender": "Male",
            "region": null,
            "birthDay": "2013-05-01",
            "lastModified": 1474258613
          },
          {
            "status": 0,
            "description": "",
            "point": 1253933,
            "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-14.png",
            "user_type": "Anchor",
            "address": "",
            "id": 50,
            "isFollowed": false,
            "user_status": "Published",
            "displayName": "太累了新狼围脖儿",
            "level": 0,
            "gender": "Female",
            "region": null,
            "birthDay": "2016-07-01",
            "lastModified": 1474788176
          }
        ],
        status:0    // 0:正在进入,1：正常，2：离开，3：断线，4：...
    }
    ```
* 动作消息

    ```
     msg : {
            msgType:"action",
            action:"chat-topic",
            comment:"约聊话题消息",
            text:"说说你的第一次",
            "msgId":12222221334124,
            chatId:1221331 //判断是否在越聊
        }
    ```
* 动作消息

    ```
     msg : {
            msgType:"action",
            action:"stop-live",
            comment:"直播结束",
            roomId:122,
            live:{
                "liveId" : 13456,
                "title" :  "title",
                "streamAddr" :  "http://pull.wmlive.cn/live/1462006378736119.flv",
                "pushAddr" :  "rtmp://push.wmlive.cn/live/1462006378736119",
                "shareAddr" :  "http://live.wmlive.cn/static/share?userid=38298237&liveid=1462006378736119&ctime=1462006378",
                "lookbackAddr" :  "",
                "userId" :  38298237,
                "roomId" :  123213,
                totalUsers :  23213,     
                totalTickets :  123213,
                onlineUsers:1221
            },
            "msgId":12222221334124
        }
    ```

* 动作消息
    ```
    msg : {
            msgType:"action",
            action:"shutup-user",
            comment:"被禁言",
            userId:12112,
            roomId:123213,
            "msgId":12222221334124
    }
    ```
* 对聊暂停

    ```
     msg : {
         "msgType": "action",
         "action": "pause-chat",
         "comment": "暂停直播",
         "text": "对方离开一下",
         "chatId": chat_id
     }
    ```
* 对聊继续

    ```
     msg : {
         "msgType": "action",
         "action": "goon-chat",
         "comment": "暂停直播",
         "text": "对方回来了",
         "chatId": chat_id
     }
    ```    
* 动作消息
    ```
    msg : {
        msgType:"action",
        action:"shutup-open-user",
        comment:"取消禁言",
        userId:12112,
        roomId:123213,
        "msgId":12222221334124
    }
    ```

* 动作消息

    ```
    msg = {
            "msgType": "action",
            "action": "live-change",
            "comment": "修改直播标题",
            "liveId": live_id,
            "title": title,
            "msgId":12222221334124
    }
    ```

* 动作消息

    ```
    msg = {
            "msgType": "action",
            "action": "start-live-notify",
            "comment": "系统通知",
            "link": 'wmlives_heihei://live?id=xxxxxx',
            "text": text,
            "fromUserId":122,
            "fromUserName":'张三',
            "gender": "Male",
            "msgId":12222221334124,
            "text-head": "您关注的",
            "text-tail": "开播了",
            "getuiAction": "live"
    }
    ```

* 动作消息

**取消约聊**
    ```
    msg = {
            "msgType": "action",
            "action": "cancel-due-chat",
            "comment": "对方取消约聊",
            "chatId": chat_id,
            "fromUserId": 10031,
            "fromUserName": "小宋手机号1",
            "gender": "Female",
            "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-2.png",
            "birthDay": "2016-01-01",
            "msgId":12222221334124
    }
    ```

* 消息列表

**消息列表约聊消息**

```
    msg = {
              "fromUserId": 10031,
              "fromUserName": "小宋手机号1",
              "gender": "Female",
              "coverUrl": "http://cdn.wmlives.com/static/img/heihei/cover/cover-2.png",
              "data": {
                "count": 5,
                "type": "calling"
              },
              "birthDay": "2016-01-01",
              "link": "wmlives_heihei://duechat?uid=10031",
              "timeStamp": 1477557274,
              "action": "message",
              "msgType": "action",
              "text": null
    }
```
    
**action**: **message**
**data**: 需要的数据
  *type*: 
      `calling:约聊未接通`
      `call:通话`
      `post:约聊对方，对方未接通`
  *count*: 次数
**link**: 同link逻辑
    
>link值同个推push的link值 见 link的值


### push 

```
ret = {
    "title": "", 
    "text": "", 
    "action": "user", 
    "link": "wmlives_heihei://user?id=xxxx", 
    "msgId": 12123124,
    "fromUserName": info["fromUserName"],
    "fromUserId": info["fromUserId"],
    "gender": info["gender"],
    "data": {}
    "deviceType": info["deviceType"],
    "clientid": info["clientId"]
}
```

#### link的值

<span id="link"></span>


* 直播间
    action = "live"
    wmlives_heihei://live?id=xxxxxx

* 首页消息显示
    action = "message"
    wmlives_heihei://message

* 首页
    action = "homepage"
    wmlives_heihei://homepage

* web页
    action = "webview"
    wmlives_heihei://webview?url=xxxxxx&type=1
    (备注：type是指打开类型，0-内部浏览器打开，1-外部浏览器打开)

* 用户
    action = "user"
    wmlives_heihei://user?id=xxxx

* 回放
    action = "replay"
    wmlives_heihei://replay?id=xxxx

* 约聊push
    action = "duechat"
    wmlives_heihei://acceptchat?chatId=121223123&type=0&userId=221232&fromUserName=张三&gender=Male



​    
