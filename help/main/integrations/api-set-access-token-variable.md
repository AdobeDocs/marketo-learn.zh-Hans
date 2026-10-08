---
title: Marketo如何API视频 — 如何在变量中设置访问令牌
description: 了解如何设置Postman应用程序以及如何利用变量将数据保存到变量中以便可重复使用。
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00.000Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
product_v2:
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: dca84292-69e9-4116-a575-667d31fa060d
    internal-label: APIs
subfeature_v2:
  - id: cf1396d8-ab85-4e93-b35d-d9b573024abf
    internal-label: REST APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 4768ecb20d4d9c70452ae084256928261f3a80eb
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 27%
---
# API 帮助 - 如何在变量中设置访问令牌

了解如何设置 Postman 应用程序并利用变量将数据保存到变量中以实现可重用性。 还了解如何发起首次Marketo Engage REST API调用以获取访问令牌。

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

* [Marketo Engage开发人员文档](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
