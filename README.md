# 自建拼音输入法词库

> 目前提供 <u>Fcitx 5</u> (Linux / Android) 以及 <u>Gboard</u> (Android + Magisk) 两种词库数据格式。

当前词库，包含了以下内容：

   * 常见的成语、俗语、诗歌等
   * 中华人民共和国四级行政区划名称（感谢[Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China)）
   * 世界各个国家国名全称、简称（感谢[wgii](https://github.com/occultskyrong/wgii))
   * 世界各国和地区名称及一级行政区划（数据来源：中华人民共和国海关总署)
   * 常见人名
   * 网络提供的第三方输入法词库
   * ……

已对以上所有数据进行去重、精简处理，最终词汇量等信息详见 [Releases](https://github.com/wuhgit/CustomPinyinDictionary/releases)。


---

<div>
	<img src="https://fcitx-im.org/fcitx.png" alt="Fcitx5 logo" width="100">
</div>

# Fcitx 5

下载 `CustomPinyinDictionary_Fcitx.dict`

- Linux

	将下载的词库复制粘贴到目录 `~/.local/share/fcitx5/pinyin/dictionaries/` 中（如果没有这个目录，您可以自行创建），重启 <u>Fcitx</u> 后即可生效。

- Android

	> https://github.com/fcitx5-android/fcitx5-android

	“小企鹅输入法5” 处于拼音输入模式时，在输入法键盘上选择 `输入法设置 > 词典`，添加刚刚下载的词库即可。


---


<div>
	<img src="https://play-lh.googleusercontent.com/X64En0aW6jkvDnd5kr16u-YuUsoJ1W2cBzJab3CQ5lObLeQ3T61DpB7AwIoZ7uqgCn4=s180" alt="Gboard logo" width="100">
</div>

# Gboard (Magisk module)

下载 `CustomPinyinDictionary_Gboard_Magisk.zip` 通过 Magisk 应用进行模块安装。

> 旧版数据用户注意： 请先恢复词库至您之前备份的数据，若没有相应备份，当迁移至 Magisk 模式时，请先在安装时选择卸载，此时模块会将原有词库替换为空白数据，随后再进行安装。
> 
> 考虑到之前的操作模式过于麻烦，且目前绝大多数 Android 用户都通过 [Magisk](https://github.com/topjohnwu/Magisk) 进行 root，今后本词库的相关数据将通过 Magisk module 模式进行更新。借助于 Magisk 的模块更新机制，您可以第一时间在模块管理页面得到词库升级提示，使用体验会更好。

安装、升级、卸载此模块均 **不需要重启**，即时生效。

安装流程中需要使用音量键进行选择操作。

若要 `完整卸载`，请先在模块中执行卸载后，再至 Magisk 模块管理页面进行 `移除` 即可。若忘记执行卸载直接移除，可以再重新执行一遍`从本地安装`，过程中选择卸载，随后移除模块即可。


## **注意**

词库导入后，可能需要一点时间后才能在输入时感知到新词，期间 <u>Gboard</u> **可能**会在通知栏以 **正在改善您的打字输入体验** 进行提示。
  
> 您可以在 `Gboard 设置 > 字典 > 个人字典 > 中文（简体）` 查看到导入后本词库的数据。

为获得更好的使用体验，建议对 <u>Gboard</u> 中以下设置进行修改：

`Gboard 设置 > 高级 > 学习`

  - 关闭 **个性化设置**
  - 关闭 **改进语音和输入功能，让所有用户受益**
