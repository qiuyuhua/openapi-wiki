微任务
=====




GetTodoCount
------------



 
    GET: CalendarGrid/Users/{userId}/Todos/Count	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId（Guid）|  
| beginTime  	| 是	        | beginTime（DateTime）	|   
| endTime	| 是	        | endTime（DateTime）	|  
####返回信息	
1. 成功：返回```json```   

***

GetTodos
------------



 
    GET: CalendarGrid/Users/{userId}/Todos	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| userId 	| 是	        | userId （Guid） |  
| beginTime  	| 是	        | beginTime（DateTime）	|   
| endTime	| 是	        | endTime（DateTime）	|  |  
####返回信息	
1. 成功：返回```json```   

***
CreateSyncEvents
------------



 



  
    GET: /InterCorporation/Corporations/{corporationId}/CreateSyncEvents	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId	| 是	        | corporationId（Guid） |   
####返回信息	
1. 成功：返回```json```   

***   
GetTask
------------ 
    GET: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}?taskTimestamp={taskTimestamp}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId	| 是	        | corporationId（Guid） |  
| taskUniversalId	| 是	        | taskUniversalId（Guid） |   
| taskTimestamp| 是	        | taskTimestamp（DateTime）	|     
####返回信息	
1. 成功：返回```json```   

***   

GetTaskLogs
------------ 
    GET: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}/Logs?taskTimestamp={taskTimestamp}&previousTaskTimestamp={previousTaskTimestamp}	
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId | 是	        | corporationId （Guid） |  
| taskUniversalId| 是	        | taskUniversalId（Guid） |   
| taskTimestamp| 是	        | taskTimestamp（DateTime）	| 
| previousTaskTimestamp| 是	        | previousTaskTimestamp（DateTime）	|      
####返回信息	
1. 成功：返回```json```   

***   

GetLogAttachment
------------ 
    GET: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}/Logs/Attachments/{attachmentId}
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId | 是	        | corporationId （Guid） |  
| taskUniversalId| 是	        | taskUniversalId（Guid） |   
| taskTimestamp| 是	        | taskTimestamp（DateTime）	| 
| previousTaskTimestamp| 是	        | previousTaskTimestamp（DateTime）	|      
####返回信息	
1. 成功：返回```json```   

***   

GetTaskLog
------------ 
    POST: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}/Logs/Add
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId | 是	        | corporationId （Guid） |  
| taskUniversalId| 是	        | taskUniversalId（Guid） |     
####返回信息	
1. 成功：返回```json```   

***   

GetTaskLogAttachment
------------ 
    POST: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}/Logs/Add
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId | 是	        | corporationId （Guid） |  
| taskUniversalId| 是	        | taskUniversalId（Guid） |  
| attachmentId | 是	        | attachmentId（Guid） |  
| mimeType  | 是	        | mimeType（string） |    
####返回信息	
1. 成功：返回```json```
2. 返回```-1```:```Cannot find the uploaded file.```   

***   

UpdateStatus
------------ 
    POST: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}/UpdateStatus/{taskStatus}
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId | 是	        | corporationId （Guid） |  
| taskUniversalId| 是	        | taskUniversalId（Guid） |  
| taskStatus| 是	        | taskStatus（object:class） |   
####返回信息	
1. 成功：返回```json```

***    

UpdateParticipantStatus
------------       
    POST: /InterCorporation/Corporations/{corporationId}/Tasks/{taskUniversalId}/Participants/{role}/{userId}/UpdateStatus/{taskParticipantStatus}
| 参数   	| 必选		| 说明		|
| ------------- | :------------ | :------------ |
| corporationId | 是	        | corporationId （Guid） |  
| taskUniversalId| 是	        | taskUniversalId（Guid） |  
| TaskParticipantRole| 是	        | TaskParticipantRole（object:class） |  
| userId | 是	        | userId（Guid） | 
| TaskParticipantStatus | 是	        | TaskParticipantStatus（object:class） |
####返回信息	
1. 成功：返回```json```


