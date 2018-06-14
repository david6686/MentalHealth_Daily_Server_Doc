FORMAT: 1A
HOST: http://api.mentaldaily.kaiyeee.tw:8080/

# 心憂日記API
心憂日記API

## API 資訊 [/info]

### 顯示出API資訊 [GET]

+ Response 200 (application/json)

    + Body

            
            {
                "version": "v1.1"
            }
            



## 取得日記列表 [/v1/daily/{username}]
<!--+ Headers-->
+ Parameters
    + username: username (string) - 使用者名稱

### 列出使用者日記列表 [GET]

+ Request (application/json)
    + Headers
    
            X-User: {"displayName": "asdasd", "email": "chris@quiver.is", "emailVerified": false, "isAnonymous": false, "photoURL": null, "providerData":{    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}, "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}
        
+ Response 200 (application/json)

    + Body

            [
                {
                    "uuid": "SD651GW6EG65W1EG651WERG",
                    <!--"username": "username",-->
                    "userID": "userID",
                    "title" : "hello world"
                    "content": "content",
                    "Mood" : [{0.87,0.78}]
                },
                {
                    "uuid": "SD651GW6EG65W1EG651WERG",
                    <!--"username": "username",-->
                    "userID": "userID",
                    "title" : "hello world"
                    "content": "content",
                    "Mood" : [{0.87,0.78}]
                }
            ]

        
## 操作日記 [/v1/daily/{username}/{id}]
<!--{-->
<!--    X-User: {   "displayName": "test", -->
<!--                "email": "chris@quiver.is", -->
<!--                "emailVerified": false, -->
<!--                "isAnonymous": false, -->
<!--                "photoURL": null, -->
<!--                "providerData":{    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca…", -->
<!--                                    "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}, -->
<!--                                    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca…", -->
<!--                                    "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}-->
<!--            }-->

<!--}-->
+ Parameters
    + username: username (string) - 使用者名稱，當為空的時候，拿到列表
    + id: uuid (number) - 日記編號


### 拿到特定日記 [GET]

+ Request (application/json)
    + Headers
    
            X-User: {"displayName": "asdasd", "email": "chris@quiver.is", "emailVerified": false, "isAnonymous": false, "photoURL": null, "providerData":{    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}, "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}




+ Response 200 (application/json)

    + Body
    
            
            {
                "uuid": "SD651GW6EG65W1EG651WERG",
                <!--"username": "username",-->
                "userID": "userID",
                "title" : "hello world"
                "content": "content",
                "Mood" : [{0.87,0.78}]
            }
            

### 修改日記 [PUT]

+ Request (application/json)
    + Headers
    
            X-User: {"displayName": "asdasd", "email": "chris@quiver.is", "emailVerified": false, "isAnonymous": false, "photoURL": null, "providerData":{    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}, "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}


    + Body
    
            {
                "title": "中文測試",
                "content": "感謝各位大神不懈的努力<(_ _)>\n 特別感謝 kaiyeee 大神教我 uri 的語法 QQ \n 特別感謝 kaiyeee 大神 幫我們架設了 Latex Server QQ"
            }


+ Response 200 (application/json)

    + Body
    
            
            {
                "uuid": "SD651GW6EG65W1EG651WERG",
                <!--"username": "username",-->
                "userID": "userID",
                "title" : "hello world"
                "content": "content",
                "Mood" : [{0.87,0.78}]
            }
            

### 刪除日記 [DELETE]

+ Request (application/json)
    + Headers
    
            X-User: {"displayName": "asdasd", "email": "chris@quiver.is", "emailVerified": false, "isAnonymous": false, "photoURL": null, "providerData":{    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}, "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}
            
       
+ Response 200 (application/json)

    + Body
    
            
            {
                "uuid": "SD651GW6EG65W1EG651WERG",
                <!--"username": "username",-->
                "userID": "userID",
                "title" : "hello world"
                "content": "content",
                "Mood" : [{0.87,0.78}]
            }
            
            

## 新增日記 [/v1/daily/{username}/new]

+ Parameters
    + username: username (string) - 使用者名稱，當為空的時候，拿到列表

### 新增日記 [POST]

+ Request (application/json)
    + Headers
    
            X-User: {"displayName": "asdasd", "email": "chris@quiver.is", "emailVerified": false, "isAnonymous": false, "photoURL": null, "providerData":{    "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}, "refreshToken": "ANflqpEVNvT4iOyKVVRyybjcuwKqnca", "uid": "P1yjH4GgcFQcJUHULmTgMLC68w64"}
            
            
    + Body
    
            {
                "title": "中文測試",
                "content": "感謝各位大神不懈的努力<(_ _)>\n 特別感謝 kaiyeee 大神教我 uri 的語法 QQ \n 特別感謝 kaiyeee 大神 幫我們架設了 Latex Server QQ"
            }

+ Response 200 (application/json)

    + Body
    
            
            {
                "uuid": "SD651GW6EG65W1EG651WERG",
                "username": "username",
                "userID": "userID",
                "title" : "hello world"
                "content": "content",
                "Mood" : [{0.87,0.78}]
            }