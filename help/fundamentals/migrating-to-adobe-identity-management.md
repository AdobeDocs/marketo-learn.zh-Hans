---
title: 迁移到AdobeIdentity Management
description: 描述即将推出。
role: User
level: Beginner
hide: true
hidefromtoc: true
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: f6ae52b43770789c24237f0bc664d33541469a50
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---

# 迁移到AdobeIdentity Management

Adobe正在改进您管理Adobe Marketo Engage订阅和用户的方式。 通过将您的Marketo Engage订阅和用户迁移到Adobe Admin Console，我们可为您和您的组织带来更高的工作效率。

通过本教程，您可以导航迁移，以便在中心位置管理Adobe Marketo Engage以及其他Adobe帐户和产品。 迁移是必需的，并且不会影响您的营销工作流、内容、集成或资产。

## 面向Marketo Engage管理员的迁移前核对清单 {#pre-migration-checklist-for-marketo-engage-administrators}

为了确保您的组织能够将Adobe Marketo Engage迁移到Adobe Admin Console，我们建议您按照以下核对清单来管理即将进行的更改。

### 1.确定您的系统管理员，并讨论可能需要采取的操作 {#identify-your-system-administrators}

* 如果您不确定组织中的哪些系统管理员，请联系您的Adobe客户团队或联系Adobe支持`marketocares@marketo.com`。

* 确认您的Marketo Engage订阅将迁移到的Adobe Admin Console(或Adobe组织)。  Marketo Engage订阅必须部署在与Dynamic Chat相同的公司中，这是与Marketo Engage集成的一种本机对话自动化工具。
  `TBD LINK TO https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete`

* 在[示例电子邮件部分](#announce-the-migration-timeline)中了解有关如何与系统管理员通信的更多信息。

### 2.熟悉迁移到Adobe身份所带来的变化和影响 {#familiarize-yourself-with-the-changes}

在下面的视频中，Marketo Engage产品管理团队将指导您完成迁移历程和预期。

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?quality=12&learn=on){transcript=true}

面向Marketo Engage管理员的更多有关此主题的帮助可在以下帮助文章中找到：

* [用户设置核对清单](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [AdobeIdentity Management概述](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [了解Marketo订阅和用户迁移到Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [使用迁移控制台迁移到Adobe身份](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [了解如何使用Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/using/admin-console.html){target="_blank"}

### 3.公布内部团队所需的迁移时间表和准备工作 {#announce-the-migration-timeline}

* 安排后，在Marketo Engage管理员和用户的日历上标记迁移日期。

您可以在&#x200B;**管理员** > **迁移控制台** > **迁移前**&#x200B;中修改迁移日期，以更好地与内部时间线保持一致。 了解有关重新计划以及[修改迁移日期](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}的限制的更多信息。

* 发送电子邮件以与系统管理员进行通信。

以下是发送给系统管理员的示例电子邮件。 通常，您的IT部门会管理您的所有Adobe许可证。

`---------------------------------------------------`

**主题：需要支持 — 将Marketo Engage订阅迁移到Adobe Admin Console**

尊敬的`[IT Administrator/NAME]`：

我们的Marketo Engage订阅将很快迁移到AdobeIdentity Management System。 [营销运营团队]需要您的帮助，以便在用户迁移开始之前完成一些必需的步骤，从而最大限度地减少对Marketo Engage用户的影响

`1.`确认该组织是否已在Adobe Admin Console中管理其他Adobe产品，以及Marketo Engage是否会迁移到同一控制台。

* 请注意，Marketo Engage订阅必须与Dynamic Chat位于同一个机构中，后者是与Marketo Engage集成的本机对话自动化工具。

* 如果您对将Marketo Engage添加到的Admin Console有疑问或疑问，请通过`marketocares@marketo.com`联系支持团队并将我们包含在您的通信中。

`2.`在Adobe中查找主题行为“管理Adobe Marketo Engage `[Package Tier]`的用户访问权限所需的操作”的电子邮件。 此电子邮件是在我们Admin Console上配置Marketo Engage许可证后发送的。 只有系统管理员会收到此电子邮件。 收到请及时通知我们。

* Adobe可能会寻求您这位用户的系统管理员的同意，以自动将Admin Console迁移到我们组织的现有控制台。 在主题为“管理用户对Adobe Marketo Engage `[Package Tier]`的访问权限所需的操作”的电子邮件中，单击“开始”按钮以导航到同意页面。

`3.` **可选：**&#x200B;在Adobe Admin Console上设置SSO（单点登录）。

* 为了使用户能够使用SSO登录他们的Adobe标识，我们要求您在用户迁移前协助在Adobe Admin Console上设置SSO。
我们感谢你在此过渡期间给予的合作。 完成这些步骤后，请通知我，以便我可以通过Marketo Engage继续迁移用户。
致敬，

`[Your Name]`

`---------------------------------------------------`

* 向Marketo Engage用户发送电子邮件。

下面是一封示例电子邮件，可用于向没有管理员权限的Marketo Engage用户宣布即将进行的迁移。

`---------------------------------------------------`

**主题：重要更新 — 将Marketo Engage订阅迁移到Adobe Admin Console**

尊敬的Marketo Engage用户：

我们有一条关于我们的Marketo Engage实例以及如何登录的重要公告。 Adobe正在将Marketo Engage订阅和用户转移到Adobe Admin Console，以便其客户能够在一个位置集中管理其所有产品。 这不会影响营销工作流、内容、集成或资产。

关键详细信息：

* 迁移日期： [指定计划日期 — 请在&#x200B;**管理员** > **迁移控制台** > **预迁移**]&#x200B;下的Marketo Engage中找到此日期

* 时间：迁移大约从我们订阅的当地时间午夜开始。

* 影响：用户迁移期间不会丢失产品访问权限。 如果您在迁移帐户时登录，则在迁移后您将注销并提示您使用Adobe标识在几分钟内重新登录。

* 优势：使用单个Adobe身份(Adobe ID或AdobeFederated ID(SSO))验证Marketo Engage和其他Adobe产品。

您需要执行的操作：

`1.`准备：需要电子邮件验证才能将您迁移到Adobe身份。

i.您已收到一封包含链接的电子邮件验证请求电子邮件（有效期为3天）。 如果链接已过期，您可以转到&#x200B;**管理员** > **我的帐户** > **帐户设置**&#x200B;并单击&#x200B;**重新发送验证**来重新发送验证电子邮件。
二、 电子邮件验证成功需要活动用户会话。 请先使用您的身份提供程序(IdP) URL登录到您的Marketo Engage订阅。

`2.`载入：迁移用户帐户后，您将收到Adobe的电子邮件，邮件内容涉及对登录方法所做的更改。

i.通过单击“接受邀请”按钮并使用Adobe身份登录来接受新的邀请。
二、 在Adobe登录页面上，请使用现有的Adobe ID登录。

`3.`联系人：如果在迁移帐户后有任何问题或需要帮助，或者帐户未迁移且无法访问Marketo Engage，请通过[内部联系人电子邮件/电话]联系Marketo Engage迁移团队。

我们感谢你在此过渡期间给予的合作。 感谢您对确保系统安全的理解和承诺。

最好的，

[您的姓名]

`---------------------------------------------------`
