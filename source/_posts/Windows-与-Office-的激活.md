---
title: Windows 与 Office 的激活
date: 2026-01-01 07:19:19
tags:
  - 科技
---
{% note warning %} 本文章仅供交流与学习，不对任何版权问题负责！ {% endnote %}
{% note warning %} 如果本文涉及工具被杀毒软件如360报告有“病毒”，请无视，这种破解微软肯定要防啊，总之爱用不用。 {% endnote %}

# 各种激活方式的区别

## KMS

KMS，Key Management Service。这是一种微软官方认可的系统激活方式，主要用于企业计算机 Windows 和 Office 的批量激活。其原理是在企业中选取一台授权计算机作为服务器分发许可证，类似于一张门卡，谁拿来刷一下都能开一次门。

- 优点：有手就行；历史悠久，兼容至 Win7。
- 缺点：一次激活有时长限制（一般180天），麻烦。

## HWID

HWID，Hardware ID。是数字许可证的一种，这种激活方式可以将激活码与硬件信息绑定，即将目标设备永久激活（虽然我也不知道为什么重装系统会失效而理论上不会）。

- 优点：永久，省心。
- 缺点：容易出岔子（有时需要系统更新），老系统（Win7）不适用。

## Ohook

Office 仅检测一次许可证，通过后不会再检查，利用此漏洞制成。

- 优点：全是。
- 缺点：无。

## TSforge

简而言之，攻破了微软的许可证存储，直接把许可证塞进去了。

- 优点：没太多缺点。
- 缺点：Windows 重大更新后需要重新激活，无法在 Win7 下激活 Office。

## 账户许可证

数字许可证的另一种，与微软账号相关联，不多说。

# 首选方案：[MAS](https://massgrave.dev/)

这是一款开源的 Windows 和 Office 激活器，功能强大。TSforge 也是制作团队的原创。

## 对于 Windows 10 和 11

按下 Win + X 组合键，在弹出列表中选择 Powershell 或 终端，输入指令：

```Powershell
irm https://get.activated.win | iex
```

然后等待进度条完成，会弹出脚本页面。

## 对于 Windows 7

[官方脚本下载地址](https://dev.azure.com/massgrave/Microsoft-Activation-Scripts/_apis/git/repositories/Microsoft-Activation-Scripts/items?path=/MAS/All-In-One-Version-KL/MAS_AIO.cmd&download=true)，其实 Win10 和  Win11也能用，不过用指令会更快更方便。

虽然是纯英文，但应该不难理解。贴上张网图（KMS38 已移除）。

<img src="https://developer.qcloudimg.com/http-save/yehe-10236472/d25b3930f2be5e9facde50ea13b5cee8.png" alt="" referrerpolicy="no-referrer">

个人建议：优先使用绿色（指字的颜色）的激活方式。对于 Windows，HWID优先（Win7 当然除外），TSforge 其次，最后是 KMS。对于 Office，Ohook 足矣。

注意，KMS 和 TSforge 中的 KMS 不一样，后者可以卡 Bug 激活 4000+ 年，约等于永久激活。

找了张汉化图（KMS38 已移除）。

<img src="https://developer.qcloudimg.com/http-save/2102001/936ffd8773eb8097b9f5a39b20d1055f.png" alt="" referrerpolicy="no-referrer">

# 其他方案：网上各种神秘激活器

HEU_KMS_Activator

KMSPico

不想贴素材了，MAS 脚本搞不定的话可以评论区留言。

# 附：

借助 MAS，还可以实现许多操作，如家庭版（多数笔记本默认）转为专业版等，可前往官网根据文档自己摸索。