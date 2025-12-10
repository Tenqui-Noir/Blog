---
title: Play Integrity 完整性验证解决方案
description: 使用 Play Integrity Fix(Fork)，TrickyStore 和 TrickyStore Addon 来通过 Play Integrity 完整性验证
date: 2025-12-10
excerpt: 本文操作来源于 reddit 帖子：[Tutorial] Guide on fixing play integrity on rooted device ,我并不是来抢走他人的劳动成果，我只针对操作进行展开说明
permalink: /Play-Integrity-Pass/
---
# Play Integrity 完整性验证解决方案
本文操作来源于 reddit 帖子：[[Tutorial] Guide on fixing play integrity on rooted device.](https://www.reddit.com/r/Magisk/comments/1js8qm3/tutorial_guide_on_fixing_play_integrity_on_rooted/)
<br>
我并不是来抢走他人的劳动成果，我只针对操作进行展开说明

推荐您在操作时主动了解每一步所作的目的，这有助于您日后（或遇错）时排查错误。
<br>
此方案需要你拥有  [Root权限](https://zh.wikipedia.org/wiki/Root_(Android)) ,推荐使用 [MT管理器](https://mt2.cn/) 进行文件相关操作
## 简要操作流程：
首先请移除所有与完整性验证相关的模块
1. 下载 [Play Integrity Fork](https://github.com/osm0sis/PlayIntegrityFork/releases), [TrickyStore](https://github.com/5ec1cff/TrickyStore/releases/), [TrickyStore Addon](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases)
2. 安装 Play Integrity Fork 与 TrickyStore
3. 重启设备
4. 在模块列表中点击 Play Integrity Fork 的操作按钮
5. 将 ``/data/adb`` 下的 ``pif.json`` 复制到 ``/data/adb/modules/playintegrityfix`` 下
6. 安装 ``TrickyStore Addon``
7. 重启设备
8. 点击 ``TrickyStore`` 的操作按钮，若未安装 ``KsuWebUI`` 或 ``MMRL`` ，它将自动安装，推荐使用 ``KsuWebUI``
9. 点击 ``TrickyStore`` 的操作按钮以打开 ``KsuWebUI``
10. 选中 ``Google Play Services``, ``Google Play Store``, ``Google Services Framework``
11. 打开选项（右上角三个点），选择 密钥 ，点击"有效"
12. 再次打开选项，> 设置安全补丁 > 获取安全补丁日期，若操作成功，点击保存，若操作不成功请点击 自动
13. 重启设备

现在应该能够通过完整性验证，此外，若无必要，请尽量不要检查完整性验证，过多的请求会让 Google 怀疑你的设备

具体过程后详解面会补上（