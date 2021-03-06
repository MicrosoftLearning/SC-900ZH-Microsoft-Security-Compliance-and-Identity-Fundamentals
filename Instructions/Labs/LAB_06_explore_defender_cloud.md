---
lab:
    title: '探索 Microsoft Defender for Cloud'
    module: '模块 3 第 2 课：描述 Microsoft 安全解决方案的功能：描述 Azure 安全管理功能'
---

# 实验室：探索 Microsoft Defender for Cloud

## 实验室场景
在此实验室中，你将探索 Microsoft Defender for Cloud 并了解如何使用 Azure 安全功能分数来优化组织的安全状况。

**预计用时**：30 分钟

#### 任务 1：在此任务中，你将大致了解 Microsoft Defender for Cloud。
1.	打开 Microsoft Edge。在地址栏中，输入“**portal.azure.com**”。

1. 使用管理员凭据登录。
    1. 在“登录”窗口中，输入“**admin@WWLxZZZZZZ.onmicrosoft.com**”（其中，ZZZZZZ 是实验室托管提供商提供的唯一租户 ID），然后选择“**下一步**”。
    1. 输入管理员密码，该密码应由实验室托管提供商提供。选择“**登录**”。
    1. 在提示保持登录状态时，选择“**是**”。

1. 在屏幕左上角显示 Microsoft Azure 的位置旁边，选择“显示门户菜单”图标（这三条水平线也称为汉堡图标），然后在左侧导航面板中的“收藏夹”下，选择“**Microsoft Defender for Cloud**”。  如果“收藏夹”下未列出该项，则在搜索框中输入 **Microsoft Defender for Cloud**，然后在结果列表中，选择“**Microsoft Defender for Cloud**”。

1. 请注意 Microsoft Defender for Cloud 概述页面中提供的信息。  

1. 可能会在页面顶部看到一个蓝色信息框，这表示你可能在查看限制性信息。  选择“**单击此处**”。
    1. 为了确保获得租户范围的可见性，请向自己分配必要的角色。  选择“**安全管理员**”，然后选择页面底部的“**获取访问权限**”。
    1. 可能会看到消息“根管理组不存在”。  根据描述，系统将为你创建组。  最多可能需要 15 分钟才能完成（但通常会更快）。  授予权限后，选择页面左上角“获取权限”上方的“**Microsoft Defender for Cloud**”，然后刷新 Microsoft Defender for Cloud 概述页面。

1. 页面顶部的信息包括 Azure 订阅数、评估资源数、可用建议数和任何存在的安全警报。  在页面的正文中，有表示安全功能分数、法规合规性、见解等内容的卡片。  

1. 在页面顶部选择“**已评估的资源**”。  （请注意，这相当于在 Microsoft Defender for Cloud 主页的左侧导航面板中选择了“清单”）。
    1. 随后会转到“**清单**”页面，其中显示 Azure Pass 订阅。  选择“**Azure Pass - 赞助**”。
    1. “资源运行状况”页面提供建议列表。  在可用列表中，选择“**应向订阅分配多个所有者**”。
    1. 选择“修正”步骤旁的向下箭头。注意详细的修正步骤是如何与执行操作的选项一起提供的。  
    1. 选择屏幕左上角的“**Microsoft Defender for Cloud**”，返回 Microsoft Defender for Cloud 概述页面。

1. 在页面顶部选择“**可用建议**”。  （请注意，这相当于在 Microsoft Defender for Cloud 主页的左侧导航面板中选择了“建议”）。
    1. “建议”页面显示了安全功能分数仪表板。
    1. 安全功能分数仪表板下方有控制措施列表。每项安全控制措施都表示一项应该缓解的安全风险，其中还有与该控制措施相关的最高分数、当前分数、潜在分数增加和资源运行状况状态的信息。  
    1. 选择其中一项控制措施，例如“**启用 MFA**”。  选择其中一个子项，例如“**应在对订阅拥有所有者权限的帐户上启用 MFA**”。  在打开的页面中，你将看到一段描述、修正步骤和受影响的资源。选择屏幕右上角的“**X**”退出此页面。
    1. 选择屏幕右上角的“**X**”退出“建议”页面，返回到概述页面。

1. 在主页中选择“**法规合规性**”。“法规合规性”页面上提供了合规性控制措施列表。  每项控制措施下都有一组基于 Azure 安全基准的评估；该基准针对如何保护 Azure 上的云解决方案提供相关建议。
    1. 选择“**IM. 标识管理**”，然后选择“**IM-6 使用强身份验证控制**”。  列表显示了可用于改进合规性态势的客户责任操作。
    1. 选择屏幕右上角的“**X**”关闭页面，返回到 Microsoft Defender for Cloud 概述页面。 
    1. 使 Microsoft Defender for Cloud 概述页面保持打开状态，以便在下个任务中使用。


#### 任务 2：在本任务中，你将导航到 Azure 安全功能分数，并探索可提高安全功能分数的建议。 

1. 在 Microsoft Defender for Cloud 概述页面中，选择“**安全功能分数**”卡片。
1. 选择“**Azure Pass - 赞助**”。  记下安全功能分数。
1. 在“建议”页面中，选择“**实现安全最佳做法**”以展开列表。请注意，其资源运行状况显示为红色。
1. 选择项“**应向订阅分配多个所有者**”，它将资源运行状况显示为红色。 
1. 在“**受影响的资源**”下方，确保选中/标出运行不正常的资源，然后选择列出的 Azure 订阅。
1. 从“访问控制(IAM)”页面的顶部选择“**+ 添加**”，然后从下拉列表中选择“**添加角色分配**”。
    1. 在页面左侧，选择“**所有者**”（这应该是列出的第一个项），使该行以灰色突出显示，然后在页面底部选择“**下一步**”。
    1. 在“**成员**”旁边，选择“**+ 选择成员**”。 
    1. 在屏幕右侧打开的“选择成员”窗口中，选择“**Alex Wilber**”，然后按页面底部的“**选择**”。  
    1. 在“添加角色分配”页面中，验证 Alex Wilber 是否列为成员，然后依次选择“**下一步**”和“**查看 + 分配**”。
    1. 可能需要长达 24 小时的时间才会更新状态，之后，在满足“管理访问和权限”组中的所有项时，安全功能分数也将更新。
    1. 在页面左上角的“Azure Pass”上方，选择“**Microsoft Defender for Cloud**”，返回到 Microsoft Defender for Cloud 概述页面。
1. 将此页面保持在打开状态，以便执行后续任务。


#### 任务 3：  回想一下，Microsoft Defender for Cloud 支持两种模式：没有增强的安全功能（免费）和具有增强的安全功能（通过 Microsoft Defender for Cloud 计划提供）。在此任务中，你将了解如何启用/禁用各种 Microsoft Defender for Cloud 计划。

1.	在 Microsoft Defender for Cloud 概述页面的左侧导航面板中，选择“**环境设置**”。
1. 选择“租户根组”旁边的大于 **(>)** 符号以展开租户根组（不要直接选择“租户根组”，因为这会导航到其他页面），然后选择“**Azure Pass - 赞助**”
1.	在“Defender 计划”页面上，请注意如何选择启用全部计划或如何选择单个 Defender 计划。保留设置，所有计划都设置为禁用。
1.	现在可以关闭浏览器选项卡以退出 Azure 门户。


#### 回顾
在此实验室中，你探索了 Microsoft Defender for Cloud 并了解了如何使用 Azure 安全功能分数来优化组织的安全状况。

