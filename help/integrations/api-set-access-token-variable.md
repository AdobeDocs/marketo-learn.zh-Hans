---
title: Marketo如何API视频 — 如何在变量中设置访问令牌
description: 了解如何设置Postman应用程序以及如何利用变量将数据保存到变量中以便可重复使用。
feature: REST API
role: Admin, Developer
level: Beginner
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00Z
jira: KT-15548
source-git-commit: dfe4f1d9737cb0c69bbd96aedf6c61953315fa9b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# API帮助 — 如何在变量中设置访问令牌

了解如何设置Postman应用程序并利用变量将数据保存到变量中以便可重复使用。 您还将了解如何进行首次Marketo EngageREST API调用以获取访问令牌。

>[!PREREQUISITES]
>
>在开始播放本视频之前，请创建具有AOI角色的仅API用户名并创建Launchpad服务。 请按照以下文章中的步骤进行操作：
>
>* [创建仅API用户角色](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [创建仅API用户](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [创建用于REST API的自定义服务](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

此视频中使用的&#x200B;**引用：**

* Marketo身份验证端点： `{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* 用于从响应主体获取access_token的JS脚本（位于脚本：选项卡下方）：

```
var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);
```

* [Marketo Engage开发人员文档](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
