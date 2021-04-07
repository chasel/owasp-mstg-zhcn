# 前言

## 关于 OWASP 手机安全测试指南

OWASP 手机测试指南(MSTG)是一本全面的手机应用安全测试手册。它描述了验证[手机应用安全验证标准(MASVS)](https://github.com/OWASP/owasp-masvs )所需要的流程和技术，并提供了完整一致的安全测试基线。

OWASP 感谢众多作者、审批者和编辑为本指南的编写所付出的努力。如果您对《手机安全测试指南》有任何的意见或是建议，请在 [OWASP 手机安全项目的Slack频道](https://owasp.slack.com/?redir=%2Fmessages%2Fproject-mobile_omtg%2Fdetails%2F)中就 MASVS 和 MSTG 展开讨论。您可以使用[此链接](https://owasp.slack.com/join/shared_invite/zt-g398htpy-AZ40HOM1WUOZguJKbblqkw#//)注册Slack频道。(如果此链接过期，请在Github Repo打开一个PR)

## 免责声明

在使用MSTG的资料对手机应用程序进行测试之前，请查阅您所在国家的法律。

请避免使用MSTG中描述的任何内容违反法律。

## 版权和许可

Copyright © 2018 The OWASP Foundation. [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/)对任何再使用或者发行，您必须向他人明确此作品的许可条款。

## 国际标准书号

本书的国际标准书号是978-0-359-47489-9。

## 致谢

注意：此贡献者表是根据我们的[GitHub贡献统计](https://github.com/OWASP/owasp-mstg/graphs/contributors)生成的。关于这些统计的更多信息，请参阅 [GitHub Repository README](https://github.com/OWASP/owasp-mstg/blob/master/README.md)。我们会手动更新该表，所以如果你没有被立即列出，请耐心等待。

### 作者

#### Bernhard Mueller

Bernhard是一位网络安全专家，具有各种黑客系统的才能。 在该行业的十多年中，他发布了许多软件的0day漏洞，例如MS SQL Server，Adobe Flash Player，IBM Director，Cisco VOIP, 和ModSecurity。 如果你能说出它的名字，他可能至少破解过一次。 美国 BlackHat 杂志以Pwnie最佳研究奖来表彰他在手机安全领域所做的开拓性工作。

#### Sven Schleier

#### Jeroen Willemsen

#### Carlos Holguera

### 共同作者

#### Romuald Szkudlarek

#### Jeroen Beckers

#### Vikas Gupta

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

贡献者贡献了高质量的内容，并在GitHub版本库中至少记录了50个附加内容。

Jin Kung Ong, Sjoerd Langkemper, Gerhard Wagner, Michael Helwig, Pece Milosev, Ryan Teoh, Denis Pilipchuk, José Carlos Andreu, Dharshin De Silva, Anatoly Rosencrantz, Caitlin Andrews, Abhinav Sejpal, Anita Diamond, Raul Siles, Yogesh Sharma, Dominique RIGHETTO, Enrico Verzegnassi, Nick Epson, Anna Szkudlarek, Elie Saad, Prathan Phongthiproek, Tom Welch, Luander Ribeiro, Heaven L. Hodges, Shiv Sahni, Akanksha Bana, Dario Incalza, Murat Karaoz, Jason Doyle, Oguzhan Topgul, Ender IBL, Imani Sherman, magicansk, Sijo Abraham, Pishu Mahtani, Jay Mbolda, Anuruddha E., Oleg Surnin, Emil Tostrup

### 评审人

评审人一直通过GitHub问题和拉取请求评论提供有用的反馈。

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

#### Samaritan 赞助者

#### 捐赠者

以下个人和/或公司通过Leanpub或其他途径捐赠超过25美元：

- eShard

### 旧版本

《手机移动测试指南》由Milan Singh Thakur于2015年发起。原始文档最早托管在Google Drive，2016年10月迁移到GitHub上。

#### OWASP MSTG "Beta 2" (Google Doc)

| 作者                                                         | 评审人                                                       | 杰出贡献者                                                   |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| Milan Singh Thakur, Abhinav Sejpal, Blessen Thomas, Dennis Titze, Davide Cioccia, Pragati Singh, Mohammad Hamed Dadpour, David Fern, Ali Yazdani, Mirza Ali, Rahil Parikh, Anant Shrivastava, Stephen Corbiaux, Ryan Dewhurst, Anto Joseph, Bao Lee, Shiv Patel, Nutan Kumar Panda, Julian Schütte, Stephanie Vanroelen, Bernard Wagner, Gerhard Wagner, Javier Dominguez | Andrew Muller, Jonathan Carter, Stephanie Vanroelen, Milan Singh Thakur | Jim Manico, Paco Hope, Pragati Singh, Yair Amit, Amin Lalji, OWASP Mobile Team |

#### OWASP MSTG "Beta 1" (Google Doc)

| 作者                                                         | 评审人                         | 杰出贡献者                                                   |
| :----------------------------------------------------------- | :----------------------------- | :----------------------------------------------------------- |
| Milan Singh Thakur, Abhinav Sejpal, Pragati Singh, Mohammad Hamed Dadpour, David Fern, Mirza Ali, Rahil Parikh | Andrew Muller, Jonathan Carter | Jim Manico, Paco Hope, Yair Amit, Amin Lalji, OWASP Mobile Team |

