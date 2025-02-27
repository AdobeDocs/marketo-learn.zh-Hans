---
title: 迁移到Adobe Identity Management
description: 本教程将帮助您将Marketo Engage订阅和用户迁移到Adobe Admin Console。
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: 55341c3f44aaf01d746b6e3f9e241f8a75c64958
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 0%

---

# 迁移到Adobe Identity Management

Adobe正在改进您管理Adobe Marketo Engage订阅和用户的方式。 通过将您的Marketo Engage订阅和用户迁移到Adobe Admin Console，我们为您的组织带来了更高的工作效率。

本教程将帮助您导航迁移，这样您就可以在一个中心位置开始为用户管理Adobe Marketo Engage及其他Adobe帐户和产品。 迁移是必需的，并且不会影响您的营销工作流、内容、集成或资产。

## 面向Marketo Engage管理员的迁移前核对清单 {#pre-migration-checklist-for-marketo-engage-administrators}

为了确保您的组织能够将Adobe Marketo Engage迁移到Adobe Admin Console，我们建议遵循以下核对清单以管理即将进行的更改。

### 1.确定您的系统管理员和IT团队，并讨论他们可能需要采取的操作 {#identify-your-system-administrators}

* 如果您不确定组织中的哪些系统管理员，请联系您的Adobe客户团队或联系Adobe支持`marketocares@marketo.com`。

* 确认您的Adobe Admin Console订阅将迁移到的Adobe(或Marketo Engage组织)。 您可能有一个适用于[Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}的Adobe Admin Console，这是Marketo Engage中的本机对话自动化工具。 Marketo Engage订阅必须部署在与Dynamic Chat相同的组织中。

* 请与您的IT团队合作，允许列表本文顶部[列出的所有Adobe域](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}，以防止迁移到Adobe身份后Marketo Engage访问中断。

* **可选：** [在用户迁移之前实施单点登录(SSO)](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"}。

  >[!NOTE]
  >
  >Marketo Engage支持的SSO与Adobe Admin Console SSO之间存在差异。 因此，可能需要实施对配置的更改。

* **可选：**&#x200B;在用户迁移之前自定义[所需的最长会话生命周期](https://helpx.adobe.com/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"}以使Marketo Engage用户保持身份验证。

* 在[示例电子邮件部分](#announce-the-migration-timeline)中了解要与系统管理员通信的内容。

### 2.熟悉迁移到Adobe Identity所带来的变化和影响 {#familiarize-yourself-with-the-changes}

在下面的视频中，Marketo Engage产品管理团队将指导您完成迁移历程和预期。

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?t=170/?quality=12&learn=on){transcript=true}

在下面的帮助文章中，可以找到面向Marketo Engage管理员的更多有关此主题的帮助：

* [用户设置核对清单](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Adobe Identity Management概述](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [了解Marketo订阅和用户迁移到Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [使用迁移控制台迁移到Adobe Identity](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [了解如何使用Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/using/admin-console.html){target="_blank"}

### 3.公布内部团队所需的迁移时间表和准备工作 {#announce-the-migration-timeline}

* 安排后，在Marketo Engage管理员和用户的日历上标记迁移日期。

   * 您可以在&#x200B;**管理员** > **迁移控制台** > **迁移前**&#x200B;中修改迁移日期，以更好地满足内部时间线的要求。 了解有关重新计划以及[修改迁移日期](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}的限制的更多信息。

* **向系统管理员发送电子邮件**

以下是发送给管理员的示例电子邮件。 通常，您的IT部门会管理您的所有Adobe许可证。

+++ 要发送给系统管理员的示例电子邮件

**主题：需要支持 — 将Marketo Engage订阅迁移到Adobe Admin Console**

尊敬的`[IT Administrator/NAME]`：

我们的Marketo Engage订阅将很快迁移到Adobe Identity Management System。 `[Marketing Operation team]`需要您的帮助才能在用户迁移开始之前完成一些必需的步骤，从而最大限度地减少对Marketo Engage用户的影响。

`1.`确认该组织是否已在Adobe Admin Console中管理其他Adobe产品，以及是否会将Marketo Engage迁移到同一控制台。

* Marketo Engage订阅必须与Dynamic Chat位于同一组织中，后者是与Marketo Engage集成的本机对话自动化工具。

* 如果您对Admin Console有任何疑问或担忧，请通过`marketocares@marketo.com`联系Adobe支持部门并抄送我们。

`2.`在Adobe中查找主题为“管理Adobe Marketo Engage `[Package Tier]`的用户访问权限所需的操作”的电子邮件。 此电子邮件是在我们的Admin Console上配置Marketo Engage许可证后发送的。 只有系统管理员会收到此电子邮件。 收到请及时通知我们。

* Adobe可能会征求您这位身为Admin Console系统管理员的同意，以自动将用户迁移到我们组织的现有控制台。 在主题行为“管理用户对Adobe Marketo Engage `[Package Tier]`的访问权限所需的操作”的电子邮件中，单击“开始”按钮以导航到同意页面。

`3.`迁移后，Marketo Engage将从experience.adobe.com提供给Adobe Experience Cloud。 请允许列表本文顶部列出[的所有Adobe域](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}，以防止我们的Marketo Engage访问中断。

`4.` **可选：**&#x200B;在Adobe Admin Console中设置SSO（单点登录）。

* 为了帮助使用SSO登录Adobe身份的用户，请在迁移用户之前协助在Adobe Admin Console中设置SSO。

`5.` **可选：**&#x200B;在Adobe Admin Console中设置更长的[最长会话生命周期](https://helpx.adobe.com/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"}。

* 要避免用户频繁登录，请在“高级设置”中自定义较长的会话时长。

我们感谢你在此过渡期间给予的合作。 完成这些步骤后，请通知我，以便我继续进行迁移。

致敬，

`[Your Name]`

+++

* **向Marketo Engage用户发送电子邮件**

以下是&#x200B;**不**&#x200B;具有管理员权限的Marketo Engage用户的电子邮件示例。

+++ 宣布即将进行迁移的示例电子邮件

**主题：重要更新 — 将Marketo Engage订阅迁移到Adobe Admin Console**

尊敬的Marketo Engage用户：

我们有一条关于我们的Marketo Engage实例以及如何登录的重要公告。 Adobe正在将Marketo Engage订阅和用户移动到Adobe Admin Console，以便我们能够将他们的所有产品管理集中到一个位置。 这不会影响营销工作流、内容、集成或资产。

**键详细信息：**

* **迁移日期**： `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **计时**：迁移将在当地时间午夜前后开始。

* **影响**：用户迁移期间不会丢失产品访问权限。 如果您在迁移帐户时登录，则在迁移后您将注销并提示您使用Adobe Identity在几分钟内重新登录。

* **优势**：使用单个Marketo Engage身份(Adobe ID或Adobe Federated ID (SSO))验证Adobe和其他Adobe产品。

**您需要执行的操作：**

`1.` **准备**：需要电子邮件验证才能将您迁移到Adobe身份。

i.您已收到一封包含链接的电子邮件验证请求电子邮件（有效期为3天）。 如果您的链接已过期，则可以从Marketo Engage中重新发送验证电子邮件，方法是单击“我的个人资料”图标，然后导航到&#x200B;**我的帐户** > **帐户设置** > **重新发送验证**。

二、 电子邮件验证成功需要活动用户会话。 请先使用您的身份提供程序(IdP) URL登录到您的Marketo Engage订阅。

`2.` **板载**：迁移用户帐户后，您将收到Adobe的电子邮件，邮件内容涉及对登录方法所做的更改。

i.通过单击“接受邀请”按钮并使用Adobe Identity登录来接受新邀请。

二、 在Adobe登录页面上，请使用现有的Adobe ID登录。

三、 您必须先登录到Marketo Engage实例，才能访问您导航到的engage-xx.marketo.com域上任何之前已添加书签的URL。

`3.` **联系人**：如果在迁移帐户后有任何问题或需要帮助，或者帐户未迁移且无法访问Marketo Engage，请通过`[your internal contact email/phone]`联系Marketo Engage迁移团队。

我们感谢你在此过渡期间给予的合作。 感谢您对确保系统安全的理解和承诺。

致敬，

`[Your Name]`

+++