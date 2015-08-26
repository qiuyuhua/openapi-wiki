微会议
=====




Index
------------



  
    GET: /CDP/	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| url 	| 是	        | url（string）|  
####返回信息	
1. 成功：返回```json```   

***

QueryFriend
------------



 
    GET: /Users/{userId}/Friends/Query?friendUserId={friendUserId}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId （Guid） |  
| friendUserId	| 是	        | friendUserId（Guid）	|   
####返回信息	
1. 成功：返回```json```   

***

GetFriends
------------



 
    GET: /Users/{userId}/Friends	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId （Guid） |  
####返回信息	
1. 成功：返回```json``` 

***

CreateFriend
------------



 
    POST: /Users/{userId}/Friends/Create	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId （Guid） |    
####返回信息	
1. 成功：返回```json```   
2. 返回 ```-10```:```The friend has been exists.```

***
  
***

DeleteFriend
------------



 
    POST: /Users/{userId}/Friends/{friendId}/Delete	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId （Guid） |    
| friendId 	| 是	        | friendId （Guid） |  
####返回信息	
1. 成功：返回```json```   

***

UpdateFriend
------------



 
    POST: /Users/{userId}/Friends/{friendId}/Update	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId （Guid） |    
| friendId 	| 是	        | friendId （Guid） |  
####返回信息	
1. 成功：返回```json```   

***

CreateMessage
------------



 
    POST: Corporations/{corporationId}/Users/{userId}/Talks/{talkId}/Messages/Create	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId	| 是	        | corporationId（Guid） |    
| userId	| 是	        | friendId （Guid） |  
| talkId	| 是	        | talkId （Guid） |  
####返回信息	
1. 成功：返回```json```   

***

CreateMessage
------------



 
    POST: POST: /Talks/{talkId}/Messages/Create	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| talkId	| 是	        | talkId （Guid） |  
####返回信息	
1. 成功：返回```json```   

***

GetMessage
------------



 
    GET: /Talks/{talkId}/Messages/{messageId}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| talkId	| 是	        | talkId （Guid） | 
| messageId     | 是            | messageId （Guid）| 
####返回信息	
1. 成功：返回```json```   

***

GetTalkMessages
------------



 
    GET: Users/{userId}/Talks/{talkId}/Messages?start={start}&count={count}&timestamp={timestamp}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId	| 是	        | userId （Guid） | 
| talkId	| 是	        | talkId （Guid） | 
| timestamp| 是            | timestamp（DateTime）| 
| start  |  否            | start（int），默认值为```0```| 
| count  | 否           | count（int），默认值为```20```| 
####返回信息	
1. 成功：返回```json```   

***

GetTalkMessageCount
------------



 
    GET: Users/{userId}/Talks/{talkId}/Messages/Count	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId	| 是	        | userId （Guid） | 
| talkId	| 是	        | talkId （Guid） | 
####返回信息	
1. 成功：返回```json```   

***
MarkRead
------------



  
    GET: Users/{userId}/Talks/{talkId}/Messages/Count	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId	| 是	        | userId （Guid） | 
| talkId	| 是	        | talkId （Guid） | 
| timestamp     | 是	        | timestamp（DateTime） | 
####返回信息	
1. 成功：返回```json```   
2. 返回```-1```:```Failed to mark read.```

***

SyncTalkMessages
------------



 
    GET: Users/{userId}/Talks/{talkId}/Messages/Sync?lastSyncMessagesTimestamp={lastSyncMessagesTimestamp}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId	| 是	        | userId （Guid） | 
| talkId	| 是	        | talkId （Guid） | 
| lastSyncMessagesTimestamp| 是	        | lastSyncMessagesTimestamp（DateTime） | 
####返回信息	
1. 成功：返回```json```   

***

AddMessagesAttachment
------------



 
    POST:Talks/{talkId}/Messages/Attachments/Add?mimeType={mimeType}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| talkId	| 是	        | talkId （Guid） | 
| mimeType | 是	        | mimeType （string） | 
| attachmentFile | 是	        | attachmentFile（HttpPostedFileBase） | 
####返回信息	
1. 成功：返回```json```   

***

GetMessagesAttachment
------------




    GET: Talks/{talkId}/Messages/Attachments/{attachmentId}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| talkId	| 是	        | talkId （Guid） | 
| attachmentId | 是	        | attachmentId （Guid） | 
####返回信息	
1. 成功：返回```json```   

***

GetMessagesAttachmentPreview
------------ 
    GET:Talks/{talkId}/Messages/Attachments/{attachmentId}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| talkId	| 是	        | talkId （Guid） | 
| attachmentId | 是	        | attachmentId （Guid） | 
| width | 是	        | width（int） | 
| height| 是	        | height（int） | 
####返回信息	
1. 成功：返回```json```   

***


