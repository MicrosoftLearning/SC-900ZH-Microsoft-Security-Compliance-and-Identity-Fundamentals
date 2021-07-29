﻿---
lab:
    title: '探索 Azure AD 中的 Privileged Identity Management 标识治理。'
    module: '模块 2 第 4 课：描述 Azure AD 的标识保护和治理功能：描述 Azure 标识保护。'
---


# 实验室：探索 Azure AD 中的 Privileged Identity Management 标识治理。

## 实验室场景
在本实验室中，你将探索 Privileged Identity Management (PIM) 的一些基本功能。PIM 需要 Azure AD Premium P2。  在本实验室中，你将以管理员身份通过 Privileged ID management (PIM) 为其中一位用户 Diego Siciliani 配置 Azure AD 用户管理员角色。   通过用户管理员权限，Diego 将能够创建用户和组来管理许可证等。  管理员和用户 Diego 都必须针对 Azure AD Premium P2 许可进行配置。

**预计用时**：30-45 分钟

#### 任务 1：在此任务中，你将以管理员身份重置用户 Diego Siciliani 的密码。此步骤需要完成，以便首次以后续任务中的用户身份登录。

1. 打开 Microsoft Edge。  在地址栏中，输入 **“portal.azure.com”**。

2. 使用管理员凭据登录。
    1. 在“登录”窗口中，输入 **“admin@WWLxZZZZZZ.onmicrosoft.com”** （其中，ZZZZZZ 是实验室托管提供商提供的唯一租户 ID），然后选择 **“下一步”**。
    1. 输入管理员密码，该密码应由实验室托管提供商提供。选择 **“登录”**。
    1. 在提示保持登录状态时，选择 **“是”**。

3. 选择 **“Azure Active Directory”**。  

4. 从左侧导航面板中，选择 **“用户”**。

5. 从用户列表中选择 **“Diego Siciliani”**。

6. 从页面顶部选择 **“重置密码”**。由于你之前没有以 Diego 的身份登录，因此不知道他的密码，需要重置密码。

7. 当密码重置窗口打开时，请选择 **“重置密码”**。  重要说明：请记下新密码，因为你在下一个任务中需要使用该密码才能以用户身份登录。

8. 选择页面右上角的 **“X”** 关闭密码重置窗口。

9. 选择页面右上角的 **“X”** 关闭 Diego 的配置文件窗口。

10. 选择页面右上角的 **“X”** 关闭“所有用户”窗口。你现在应位于“Contoso Azure Active Directory”页面。

11. 请将浏览器页面保持在打开状态，因为后续任务中要使用该页面。


#### 任务 2：在此任务中，你将以管理员身份在 Privileged Identity Management 中为 Diego 分配 Azure AD 角色。

1. 转到打开的浏览器选项卡（标记为“Contoso - Microsoft Azure”）。   如果之前关闭了该浏览器选项卡，请打开 Microsoft Edge，在地址栏中输入“portal.azure.com”，使用管理员凭据进行登录，然后选择“Azure Active Directory”。  

2. 从左侧导航面板中，选择 **“标识治理”**。

3. 在主窗口中，确保 **“入门”** 带有下划线，然后选择屏幕右侧中间部分的 **“管理角色分配”**。  或者，从左侧导航面板的“Privileged Identity Management”下，选择 **“Azure AD 角色”**。

4. 你现在位于 Privileged Identity Management“快速启动”窗口。  选择 **“管理访问权限”**。

5. 你现在位于“Contoso 角色”页面。  在页面顶部的搜索栏中，输入 **“用户”**。  从搜索结果中，选择 **“用户管理员”**。

6. 从页面顶部选择 **“+ 分配”**。

7. 在“添加分配”页面中，确保 **“成员”** 带有下划线。  在这里，你将为 PIM 中的用户管理员角色配置成员资格设置。

8. 将“范围”类型设置为其默认值“目录”。  

9. 在“选择成员”下，选择 **“未选择任何成员”**。这会打开“选择成员”窗口。 

10. 在搜索栏中，输入 **“Diego”**。  从搜索结果中，选择 **“Diego Siciliani”**，然后按页面底部的 **“选择”**。  

11. 在“选择成员”下，你将看到已选中 1 位成员 (Deigo Siciliani) 以及所选成员的姓名和电子邮件。从“添加分配”页面底部，选择 **“下一步”**。  

12. 现在位于“设置”页面。  将“分配类型”设为默认设置“符合条件”。

13. 如果选中了“永久符合条件”框，请选择 **“永久符合条件”** 以取消选中标记。

14. 在“分配开始”字段中，保留默认日期和时间，即当天和当前时间。

15. 在“分配结束”字段中，将日期更改为当天日期（注意，默认设置是从当天算起的一年后，因此需要更改年份）。对于时间，将时间设置为当前时间加上两小时后的时间。  为“分配结束”的时间设置时间字段后，按键盘上的 Tab 键并选择页面底部的 **“分配”**。  

16. 这将返回“分配”窗口。  几秒钟后，你应该会看到“用户管理员”表中列出的 Diego Siciliani，以及分配的详细信息。  如果几秒钟后仍未看到更新，请按页面顶部的 **“刷新”**。

17. 从页面顶部选择 **“设置”**。

18. 在“用户管理员”的“角色”设置详细信息中，注意各种选项。  注意，“激活时需要理由”设置和“激活时需要 Azure MFA”设置均设为“是”。  当 Diego 激活角色时，你将在下一个任务中看到这两个设置。  另请注意，“需要获得批准才能激活”设置为“否”。将所有设置均设为相应的默认值。  选择屏幕右上角的 **“X”** 关闭页面。

19. 通过选择屏幕右上角电子邮件地址旁边的用户图标并选择 **“注销”** 进行注销。然后关闭所有浏览器窗口。


#### 任务 3：任务 3：  在此任务中，你将以 Diego Siciliani 的身份登录 Azure 门户，访问 Azure Active Directory 的 Privileged Identity Management 功能，从而激活以用户管理员身份执行的分配。  激活后，将对现有用户进行一些配置更改。备注：对于此任务，你需要访问可立即使用且可接收短信的移动设备。

1. 打开 Microsoft Edge。  在浏览器的地址栏中，输入 **“portal.azure.com”**。

1. 以 Diego Siciliani 的身份登录。
    1. 在“登录”窗口中，输入 **“DiegoS@WWLxZZZZZZ.onmicrosoft.com”**（其中，ZZZZZZ 是实验室托管提供商提供的唯一租户 ID），然后选择 **“下一步”**。
    1. 输入在上一个任务中记下的临时密码，然后选择 **“登录”**。选择 **“登录”**。
    1. 由于输入的密码只是临时密码，现在需要更新。输入当前密码。  对于新密码和确认密码字段，输入 **“SC900-Lab”**。
    1. 在提示保持登录状态时，选择 **“是”**。

1. 你应该已成功登录到 Azure 门户。
1. 在“欢迎使用”主页的“Azure 服务”下，选择 **“Azure Active Directory”**。
1. 从左侧导航面板中，选择 **“标识治理”**。
1. 在左侧导航面板中的“Privileged Identity Management”下，选择 **“Azure AD 角色”**。
1. 从左侧导航面板中，选择 **“我的角色”**。  你现在可以看到 Azure AD 角色的信息。  你将看到，你以 Diego 的身份获得了用户管理员角色。  
1. 在表的最后一列“已标记的操作”，选择 **“激活”**。
1. 这将出现一个警告图标，指示需要附加验证。  选择 **“单击以继续”**。  回想一下，用户管理员角色的 PIM 设置需要多重身份验证。  此外，由于之前未配置用于 MFA（身份验证方法）的 Diego 联系人信息，因此他必须注册自己的信息才能使用 MFA。  尽管他在任何时候以用户管理员身份登录时都必须进行 MFA，但在分配期内，MFA 注册过程只需执行一次。
1. 系统通知你需要更多信息，选择 **“下一步”**。
1. 输入密码 **“SC900-Lab”**。
1. 从“Microsoft Authenticator”窗口的左下角，选择 **“我想设置其他方法”**。
1. 系统会提示你选择“选择其他方法”。  选择 Authenticator 应用旁边的向下键。   依次选择 **“手机”**、**“确认”**。
1. 系统会提示你输入要使用的电话号码。对于电话号码的国家/地区代码，确保国家/地区正确无误。  输入电话号码，确保选择了 **“通过短信向我发送验证码”**，然后选择 **“下一步”**。
1. 输入在手机上收到的 6 位数验证码，然后选择 **“下一步”**。 
1. 你将看到表示手机已注册成功的通知。选择 **“下一步”**，然后选择 **“完成”**。
1. 系统会询问你是否要保持登录状态。选择 **“是”**。
1. 此时出现“激活用户管理员”窗口。  你需要输入激活原因。  在出现的框中，输入你需要的任何原因（最多 500 个字符），然后选择 **“激活”**。
1. 处理激活后，将会显示状态（进度为第 3 个阶段）。
1. 激活完成后，将返回到“我的角色” | Azure AD 角色页面，其中会显示一条通知，表示刚刚激活了一个角色。  选择 **“单击此处”** 以查看可用角色。  如果发现结束时间与最初配置时间不同，请按页面顶部的刷新键（刷新可能需要几分钟）。 
1. 选择屏幕右上角的 **“X”** 关闭窗口。
1. 关闭 Privileged Identity Management | 选择屏幕右上角的 **“X”** 关闭“快速启动”窗口。
1. 选择屏幕右上角的 **“X”** 关闭“标识治理”窗口。
1. 你现在已返回到“Contoso Azure Active Directory”页面。  你可以 Azure AD 用户管理员身份创建用户和组、管理许可证等。   从左侧导航面板中，选择 **“用户”**。
1. 从用户列表中，选择 **“Bianca Pisani”**。
1. 在左侧导航面板中，选择 **“许可证”**。
1. 请注意 Bianca 尚未非分配到许可证。  从页面顶部选择 **“+ 分配”**。 
1. 从选择许可证列表中，选择 **“Office 365 E3”** 和 **“Windows 10 企业版 E3”**。
1. 从页面底部选择 **“保存”**。  页面右上角会出现一个简短的通知，指出已成功分配许可证。
1. 通过选择页面右上角的 **“X”**，关闭更新的许可证分配页面。
1. 通过选择屏幕右上角电子邮件地址旁边的用户图标并选择 **“注销”** 进行注销。然后关闭所有浏览器窗口。
1. 用户管理员角色的持续时间仅限于已配置的时间。

#### 回顾
在本实验室中，你探索了 PIM。  你以管理员身份在指定的时间内为 Diego 配置了用户管理员权限。  然后，你以 Diego 身份完成了激活用户管理员权限和配置用户设置的过程。  回想一下，PIM 需要 Azure AD Premium P2 许可。