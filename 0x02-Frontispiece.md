# 前言

## 关于 OWASP 手机安全测试指南

OWASP 手机测试指南(MSTG)是一本全面的手机应用安全测试手册。它描述了验证[手机应用安全验证标准(MASVS)](https://github.com/OWASP/owasp-masvs )所需要的流程和技术，并提供了完整一致的安全测试标准。

OWASP 感谢众多作者、审批者和编辑为本指南的编写所付出的努力。如果您对《手机安全测试指南》有任何的意见或是建议，请在 [OWASP 手机安全项目的 Slack 频道](https://owasp.slack.com/?redir=%2Fmessages%2Fproject-mobile_omtg%2Fdetails%2F)中就 MASVS 和 MSTG 展开讨论。您可以使用[此链接](https://owasp.slack.com/join/shared_invite/zt-g398htpy-AZ40HOM1WUOZguJKbblqkw#//)注册Slack频道。(如果此链接过期，请在Github Repo 创建一个 PR)

## 免责声明

在使用MSTG的资料对手机应用程序进行测试之前，请查阅您所在国家的法律。

请避免使用MSTG中描述的任何内容违反法律。

## 版权和许可

版权许可 © 2018 OWASP 基金会. [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/)对任何再使用或者发行的情况下，您必须向他人明确此作品的许可条款。

## 国际标准书号

本书的国际标准书号是978-0-359-47489-9。

## 致谢

注意：此贡献者表是根据我们的[GitHub贡献统计](https://github.com/OWASP/owasp-mstg/graphs/contributors)生成的。关于这些统计的更多信息，请参阅 [GitHub Repository README](https://github.com/OWASP/owasp-mstg/blob/master/README.md)。我们会手动更新该表，所以如果你没有被立即列出，请耐心等待。

### 作者

#### Bernhard Mueller

Bernhard是一位网络安全专家，具有各种黑客系统的技能。 在该行业的十多年中，他发布了许多软件的 0 day漏洞，例如 MS SQL Server，Adobe Flash Player，IBM Director，Cisco VOIP, 和ModSecurity。 如果你能说出它的名字，他可能至少破解过一次。 美国 BlackHat 杂志以Pwnie最佳研究奖来表彰他在手机安全领域所做的开拓性工作。

#### Sven Schleier

Sven 是一名经验丰富的web和手机渗透测试人员，他评估了从过去的 Flash 应用程序到当下的手机应用程序的所有内容。同时他也是一名安全工程师，并在 SDLC 期间为诸多端到端的项目提供“内置安全”的服务。他曾在本地和国际会议上发表演讲，并正在举办关于 web应用程序和手机应用程序安全性的实践研讨会。

#### Jeroen Willemsen

Jeroen 是 Xebia 的首席安全架构师，擅长移动安全和风险管理。他曾作为安全技术指导，安全工程师和全栈开发人员为公司提供支持，这也使他成为一个万能的人。他喜欢讲解的技术主题是从安全问题到编程挑战。

#### Carlos Holguera

Carlos 是一名安全工程师，在 ESRYPT 管理手机渗透测试团队。他在手机应用和嵌入式系统（如汽车控制单元和 IoT 设备）的安全测试领域拥有多年实践经验。他热衷于手机应用程序的逆向工程和动态检测，并不断学习和分享自己的知识。

### 共同作者

共同作者持续贡献了优质内容，并在 GitHub 版本库中至少有2000次提交记录。

#### Romuald Szkudlarek

Romuald 是一位充满活力的网络安全和隐私专家，在网络、移动、物联网和云领域拥有超过15年的经验。在他的职业生涯中，他一直在业余时间参与各种项目，以推动软件和安全领域的发展。他经常在各种机构授课。他拥有 CISSP、CCSP、CSSLP 和 CEH 证书。

#### Jeroen Beckers

Jeroen 是 NVISO 的移动安全负责人，负责移动安全项目的质量保证和所有移动设备的研发。他在高中和大学期间曾担任Flash开发人员，但毕业后转而从事网络安全工作，目前在移动安全领域有5年以上的工作经验。他乐于分享，并与同事、大学、客户和会议上的有过多次演讲和培训。

#### Vikas Gupta

Vikas 是一位经验丰富的网络安全研究人员，擅长移动安全。在他的职业生涯中，他曾为金融科技、银行和政府等不同行业的应用程序提供安全保障。他喜欢逆向工程，尤其是混淆本地代码和密码学。他拥有安全和移动计算方面的硕士学位，并获得 OSCP 认证。同时他也乐于分享知识及交流思想。

### 杰出贡献者

杰出贡献者持续贡献了优质内容，并在 GitHub 版本库中至少有500次添加记录。

- Pawel Rzepa
- Francesco Stillavato
- Henry Hoggard
- Andreas Happe
- Kyle Benac
- Paulino Calderon
- Alexander Anthuk
- Caleb Kinney
- Abderrahmane Aftahi
- Koki Takeyama
- Wen Bin Kong
- Abdessamad Temmar
- Cláudio André
- Slawomir Kosowski
- Bolot Kerimbaev
- Lukasz Wierzbicki

### 贡献者

贡献者贡献了高质量的内容，并在 GitHub 版本库中至少记录了50个附加内容。

Jin Kung Ong, Sjoerd Langkemper, Gerhard Wagner, Michael Helwig, Pece Milosev, Ryan Teoh, Denis Pilipchuk, José Carlos Andreu, Dharshin De Silva, Anatoly Rosencrantz, Caitlin Andrews, Abhinav Sejpal, Anita Diamond, Raul Siles, Yogesh Sharma, Dominique RIGHETTO, Enrico Verzegnassi, Nick Epson, Anna Szkudlarek, Elie Saad, Prathan Phongthiproek, Tom Welch, Luander Ribeiro, Heaven L. Hodges, Shiv Sahni, Akanksha Bana, Dario Incalza, Murat Karaoz, Jason Doyle, Oguzhan Topgul, Ender IBL, Imani Sherman, magicansk, Sijo Abraham, Pishu Mahtani, Jay Mbolda, Anuruddha E., Oleg Surnin, Emil Tostrup

### 评审人

评审人一直通过 GitHub 问题和拉取请求评论提供有用的反馈。

- Jeroen Beckers
- Sjoerd Langkemper
- Anant Shrivastava

### 编辑

- Heaven Hodges
- Caitlin Andrews
- Nick Epson
- Anita Diamond
- Anna Szkudlarek

### 其他

还有一些贡献者只提交了少量内容，例如单个单词或句子（添加的内容少于50个）。他们的完整的清单可在[GitHub](https://github.com/OWASP/owasp-mstg/graphs/contributors)中找到。

### 赞助者

#### 荣誉赞助者

[OWASP湾区分会](https://twitter.com/OWASPBayArea?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor)

#### Good Samaritan Benefactor

#### 捐赠者

以下个人和/或公司通过 Leanpub 或其他途径捐赠超过25美元：

- eShard

### 旧版本

《手机应用测试指南》由 Milan Singh Thakur 于2015年发起。原始文档最早托管在 Google Drive，2016年10月迁移到 GitHub 上。

#### OWASP MSTG "Beta 2" (Google Doc)

| 作者                                                         | 评审人                                                       | 杰出贡献者                                                   |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| Milan Singh Thakur, Abhinav Sejpal, Blessen Thomas, Dennis Titze, Davide Cioccia, Pragati Singh, Mohammad Hamed Dadpour, David Fern, Ali Yazdani, Mirza Ali, Rahil Parikh, Anant Shrivastava, Stephen Corbiaux, Ryan Dewhurst, Anto Joseph, Bao Lee, Shiv Patel, Nutan Kumar Panda, Julian Schütte, Stephanie Vanroelen, Bernard Wagner, Gerhard Wagner, Javier Dominguez | Andrew Muller, Jonathan Carter, Stephanie Vanroelen, Milan Singh Thakur | Jim Manico, Paco Hope, Pragati Singh, Yair Amit, Amin Lalji, OWASP Mobile Team |

#### OWASP MSTG "Beta 1" (Google Doc)

| 作者                                                         | 评审人                         | 杰出贡献者                                                   |
| :----------------------------------------------------------- | :----------------------------- | :----------------------------------------------------------- |
| Milan Singh Thakur, Abhinav Sejpal, Pragati Singh, Mohammad Hamed Dadpour, David Fern, Mirza Ali, Rahil Parikh | Andrew Muller, Jonathan Carter | Jim Manico, Paco Hope, Yair Amit, Amin Lalji, OWASP Mobile Team |

