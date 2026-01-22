---
title: 迁移至 Adobe Identity Management
description: 本教程将帮助您完成将 Marketo Engage 订阅和用户迁移至 Adobe Admin Console 的全过程。
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: ht
source-wordcount: '1250'
ht-degree: 100%

---

# 迁移至 Adobe Identity Management

Adobe 正在升级您管理 Adobe Marketo Engage 订阅和用户的方式。通过将 Marketo Engage 的订阅和用户迁移至 Adobe Admin Console，Adobe 将帮助您的组织提升管理效率。

本教程将引导您顺利完成迁移，使您能够在一个集中位置统一管理用户的 Adobe Marketo Engage 以及其他 Adobe 帐户和产品。此次迁移为必要操作，不会影响您的营销工作流、内容、集成或资产。

## Marketo Engage 管理员迁移前检查清单 {#pre-migration-checklist-for-marketo-engage-administrators}

为确保您的组织能够顺利将 Adobe Marketo Engage 迁移至 Adobe Admin Console，我们建议按照以下检查清单来管理即将到来的变更。

### &#x200B;1. 确认系统管理员和 IT 团队，并讨论他们可能需要执行的操作 {#identify-your-system-administrators}

* 如果您不确定组织内的系统管理员是谁，请联系您的 Adobe 帐户团队，或联系 Adobe 支持团队：`marketocares@marketo.com`。

* 确认 Marketo Engage 订阅将迁移到哪个 Adobe Admin Console（或 Adobe 组织）。您很可能已经拥有一个用于 [Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"} 的 Adobe Admin Console。Dynamic Chat 是 Marketo Engage 中内置的对话自动化工具。Marketo Engage 的订阅必须与 Dynamic Chat 部署在同一个组织中。

* 请与您的 IT 团队协作，将[本文顶部](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}列出的所有 Adobe 域名加入允许列表，以防在迁移至 Adobe Identity 后影响 Marketo Engage 的访问。

* **可选：**[在用户迁移之前实施单点登录（SSO）](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"}。

  >[!NOTE]
  >
  >Marketo Engage 支持的 SSO 与 Adobe Admin Console 的 SSO 之间存在差异。因此，可能需要对您的现有配置进行相应调整。

* **可选：**&#x200B;在用户迁移之前，自定义[所需的最大会话生命周期](https://helpx.adobe.com/cn/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"}，以便 Marketo Engage 用户保持登录状态。

* 请参阅[示例电子邮件部分](#announce-the-migration-timeline)，了解需要向系统管理员传达的具体事项。

### &#x200B;2. 了解迁移至 Adobe Identity 所带来的变化与影响 {#familiarize-yourself-with-the-changes}

在下面的视频中，Marketo Engage 产品管理团队将带您了解迁移流程及可预期的变化。

>[!VIDEO](https://video.tv.adobe.com/v/3432363/?captions=chi_hans&t=170/?quality=12&learn=on){transcript=true}

有关该主题的更多帮助，Marketo Engage 管理员可参考以下帮助文档：

* [用户设置检查清单](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Adobe Identity Management 概述](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [了解 Marketo 订阅与用户迁移至 Adobe Admin Console](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [使用迁移控制台迁移至 Adobe Identity](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [了解如何使用 Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/using/admin-console.html){target="_blank"}

### &#x200B;3. 向内部团队公告迁移时间线及所需准备工作 {#announce-the-migration-timeline}

* 迁移日期一经确定，请将其标记在 Marketo Engage 管理员和用户的日程表中。

   * 您可以在&#x200B;**管理员** > **迁移控制台** > **迁移前**&#x200B;中修改迁移日期，以更好地配合内部时间安排。了解有关重新安排迁移时间以及[修改迁移日期](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}的限制的更多信息。

* **向系统管理员发送电子邮件**

以下是可发送给管理员的示例邮件。通常情况下，所有 Adobe 许可证均由您的 IT 部门统一管理。

+++ 发送给系统管理员的示例邮件

**主题：需要支持——将 Marketo Engage 订阅迁移至 Adobe Admin Console**

尊敬的 `[IT Administrator/NAME]`：

我们的 Marketo Engage 订阅即将迁移至 Adobe Identity Management 系统。`[Marketing Operation team]` 需要您的协助，在用户迁移开始之前完成一些必要步骤，以尽量减少对 Marketo Engage 用户的影响。

`1.`确认组织是否已在 Adobe Admin Console 中管理其他 Adobe 产品，以及 Marketo Engage 是否将迁移至同一个控制台。

* Marketo Engage 的订阅必须与 Dynamic Chat 位于同一组织中。Dynamic Chat 是与 Marketo Engage 集成的原生对话自动化工具。

* 如果您对 Admin Console 有任何疑问或顾虑，请联系 Adobe 支持团队：`marketocares@marketo.com`，并抄送我们。

`2.` 请留意来自 Adobe 的电子邮件，邮件主题为“需要采取行动来管理 Adobe Marketo Engage 的用户访问权限`[Package Tier]`”。该邮件将在 Marketo Engage 许可证配置到我们的 Admin Console 之后发送。只有系统管理员会收到此邮件。收到邮件后，请第一时间通知我们。

* Adobe 可能会向您（Admin Console 的系统管理员）请求同意，将用户自动迁移到我们组织现有的控制台中。在主题为“需要采取行动来管理 Adobe Marketo Engage 的用户访问权限 `[Package Tier]`”的邮件中，点击“开始”按钮以进入授权页面。

`3.` 迁移完成后，Marketo Engage 将从 experience.adobe.com 迁移至 Adobe Experience Cloud。请将[本文顶部](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}列出的所有 Adobe 域名加入允许列表，以避免影响我们对 Marketo Engage 的访问。

`4.` **可选：**&#x200B;在 Adobe Admin Console 中配置 SSO（单点登录）。

* 为方便未来使用 Adobe Identity 通过 SSO 登录的用户，请在用户迁移之前协助在 Adobe Admin Console 中完成 SSO 配置。

`5.` **可选：**&#x200B;在 Adobe Admin Console 中设置更长的[最大会话生命周期](https://helpx.adobe.com/cn/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"}。

* 为避免用户频繁登录，请在“高级设置”中将会话生命周期配置为更长的时长。

感谢您在此次过渡期间的配合与支持。请在完成上述步骤后告知我，以便我继续推进迁移工作。

此致
敬礼

`[Your Name]`

+++

* **向 Marketo Engage 用户发送电子邮件**

以下是发送给&#x200B;**不**&#x200B;具备管理员权限的 Marketo Engage 用户的示例邮件。

+++ 公告即将迁移的示例邮件

**主题：重要更新——Marketo Engage 订阅迁移至 Adobe Admin Console**

尊敬的 Marketo Engage 用户：

我们有一项关于 Marketo Engage 实例以及您登录方式的重要公告。Adobe 正在将 Marketo Engage 的订阅和用户迁移至 Adobe Admin Console，以便在一个集中位置统一管理所有产品。此举不会影响现有的营销工作流、内容、集成或资产。

**关键信息：**

* **迁移日期**：`[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **时间安排**：迁移将在本地时间午夜左右开始。

* **影响**：用户迁移过程中不会造成产品访问中断。如果在迁移期间您正处于登录状态，系统会将您登出，并在迁移完成后几分钟内提示您使用 Adobe Identity 重新登录。

* **优势**：通过单一 Adobe 身份（Adobe ID 或 Adobe Federated ID (SSO)）即可统一登录 Marketo Engage 及其他 Adobe 产品。

**您需要执行的操作：**

`1.` **准备**：迁移至 Adobe Identity 需要完成电子邮件验证。

i. 您将收到一封包含验证链接的“电子邮件验证请求”邮件（链接有效期为 3 天）。如果链接已过期，您可以在 Marketo Engage 中点击“我的轮廓”图标，然后前往&#x200B;**我的帐户** > **帐户设置** > **重新发送验证**，重新发送验证电子邮件。

ii. 成功完成电子邮件验证需要保持用户会话处于活动状态。请先通过您的身份提供方（IdP）URL 登录 Marketo Engage 订阅。

`2.` **加入**：用户帐户迁移完成后，您将收到一封来自 Adobe 的邮件，说明登录方式的变更。

i. 点击“接受邀请” 按钮，并使用 Adobe Identity 登录以接受新的邀请。

ii. 在 Adobe 登录页面，请使用已有的 Adobe ID 登录。

iii. 对于之前已加入书签的 engage-xx.marketo.com 域名下的任何 URL，您需要先登录 Marketo Engage 实例后才能访问。

`3.` **联系支持**：如果在帐户迁移完成后有任何疑问或需要协助，或如果您的帐户尚未迁移且无法访问 Marketo Engage，请联系 Marketo Engage 迁移团队：`[your internal contact email/phone]`

感谢您在此次过渡期间的配合与支持。感谢您在此次迁移过程中的配合与支持。

此致
敬礼

`[Your Name]`

+++
