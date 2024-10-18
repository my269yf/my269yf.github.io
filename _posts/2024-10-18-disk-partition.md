---
layout:     post
title:      "如何给磁盘分区"
subtitle:   "DiskGenius的基本使用教程"
date:       2024-10-18 17:00:00
author:     "Mr.YF"
header-img: "img/default.jpg"
tags:
    - 计算机
    - 软件
---

# 一、引言
## 1. 什么是磁盘分区
打开电脑的资源管理器，我们可以看到我们所有的文件都在这里。但是这么多文件，如果不进行分类，很难进行管理。

因此，我们一般给磁盘进行分区，比如按照存储内容分为系统盘、应用盘、仓库盘等。每个磁盘的空间都可以根据自己的需求和喜好调整。

但要实现上述功能，我们要使用一些图形化的软件方便用户使用。例如Windows自带的磁盘管理工具、DiskGenius、分区助手等。Windows自带的工具就足以满足基本使用需求。

然而，如果你追求更便捷的操作、更多的功能，自带的工具就没那么好用了。
## 2. 什么是DiskGenius
DiskGenius（后面简称"DG"）是一款硬盘分区及数据恢复软件。

它是在最初的DOS版的基础上开发而成的。Windows版本的DiskGenius软件，除了继承并增强了DOS版的大部分功能外，还增加了许多新的功能。

如：已删除文件恢复、分区复制、分区备份、硬盘复制等功能。

另外还增加了对VMWare、Virtual PC、VirtualBox虚拟硬盘的支持。

# 二、使用DiskGenius进行磁盘分区的详细步骤

现在，我来讲解DG的具体使用步骤和注意事项。

## 1. 下载与安装
- 从官方网站下载DiskGenius软件并完成安装。[点击跳转官网](https://www.diskgenius.cn/)。选择自己系统版本对应的软件版本，进行下载（通常为64位）。
- 如果你已经进入了PE系统，通常PE系统会内置该软件，上期文章有详细教程关于如何制作和进入PE系统，[点击跳转](https://my269yf.github.io/2024/10/13/WinInstall/)。
>某些功能需要付费，而免费下载使用的版本可以满足普通用户绝大部分需求，因此我们选择DG官网下载即可免费使用。

## 2. 打开软件
- 使用解压软件解压下载过的压缩包，然后找到**DiskGenius.exe**文件，双击打开，即可启动程序。
>启动DiskGenius后，主界面将显示你的所有磁盘和分区，以及工作区面板。

## 3. 选择磁盘
- 找到你要进行分区的磁盘，确保选择正确（例如：硬盘、U盘等）。
>如果你的硬盘里面有文件，请务必注意备份（把重要的文件移动到其他磁盘即可，几乎不会对其他磁盘造成影响），因为分区过程有很大的概率丢失文件。备份文件后，即使分区出现问题，也不会造成损失。硬盘出现损坏的可能性相对比较小。

## 4. 查看当前分区情况
- 在下方的分区信息区域查看当前分区情况，包括分区大小、格式和未分配空间。可自行查看硬盘的详细数据以决定如何操作。


## 5. 调整、拆分和删除分区
- 如果磁盘上已有分区，可以进行分区调整：
     - 右键点击要调整的分区，选择“调整大小/移动分区”。
     - 拖动分区边缘或输入新大小，点击“确定”。
- 如果是想把现有的磁盘拆分为多个，可以选择拆分磁盘：
     - 右键点击要调整的分区，选择“拆分分区”。
     - 拖动分区边缘或输入新大小，点击“确定”。
- 如果想建立一个全新的分区，可以选择删除分区操作：
     - 右键点击要调整的分区，选择“删除当前分区”。
     - 点击“是”以确认。
>调整和拆分分区造成文件丢失的可能性较大，所以一般分区在系统安装前完成比较好，并且后期尽量不要进行修改。

## 6. 创建新分区
   - 右键点击未分配的空间，选择“创建分区”。
   - 在弹出的窗口中，填写以下信息：
     - **分区大小**：输入你希望新分区的大小。
     - **分区类型**：选择“主分区”或“逻辑分区”。
     - **文件系统**：选择文件系统类型（如NTFS、FAT32等）。
     - **分区标签**：可选择性输入分区名称。
>如果你想一次性创建多个分区，可以选择“快速分区”。

## 7. 确认设置
   - 检查所有设置无误后，点击“确定”。

## 8. 应用更改
   - 在主界面上，点击“保存更改”按钮，确认操作。
   - 软件可能会提示你确认操作，点击“是”继续。
>该步骤会对新建的分区进行格式化处理，分区里面的所有文件将会丢失，请务必确认操作。

## 9. 完成
   - 等待DiskGenius完成分区操作。完成后，可以在资源管理器中查看新分区。
>至此，分区操作完成。

## 注意事项
1. **备份数据**：在操作前务必备份重要数据，避免意外丢失。
2. **分区格式**：根据需要选择合适的文件系统：
   1. NTFS适合大文件和安全性要求高的场合，但是U盘不建议使用，这样做会损失U盘寿命；
   2. FAT32适合兼容性要求高的场合，但存储单个文件大小不得超过4GB，适合给U盘使用，并且没有传输大文件的需求；
   3. exFAT在老机器上的兼容性较差，但由于支持单个文件超过4GB的大小，并且比FAT32更具灵活性和效率，尤其是在不同操作系统之间的数据交换中，因此更适合有大文件存储需求的U盘使用。
>对于安装在电脑上的硬盘，选择NTFS即可；对于U盘，我个人更推荐FAT32。
3. **分区表**：分区表是存储在磁盘上的一部分，用于描述磁盘上各个分区的信息。它包含每个分区的起始位置、大小、类型和文件系统等信息。主要有两种分区表类型：MBR和GPT。确保了解你的磁盘类型，根据需要选择分区类型：
   1. **MBR**（主引导记录）：
   - 最大支持2TB的磁盘。
   - 最多支持四个主分区，或三个主分区加一个扩展分区。
   - 兼容性强，但不支持大于2TB的硬盘。
   - Legacy从MBR启动，一般为老机器使用，使用传统BIOS启动模式。
   - 适合老机器使用，新的机器更推荐GPT。
   2. **GPT**（GUID分区表）： 
   - 支持超过2TB的磁盘，理论上可以达到9.4ZB。
   - 可以有更多的分区（通常是128个）。
   - 提供冗余分区表，增加了数据安全性。
   - UEFI启动时读取GPT，启动更快更灵活，提供图形化界面BIOS。
   - 新的硬件通常支持GPT，适合64位操作系统。