![](https://raw.githubusercontent.com/wuhgit/CustomPinyinDictionary/main/documents/title.png)

> 目前提供 <u>Fcitx 5</u> (Linux / Android) 以及 <u>Gboard</u> (Android + Magisk) 两种词库数据格式。

当前词库，包含了以下内容：

   * 常见的成语、俗语、诗歌等
   * 中华人民共和国四级行政区划名称（感谢[Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China)）
   * 世界各个国家国名全称、简称（感谢[wgii](https://github.com/occultskyrong/wgii))
   * 世界各国和地区名称及一级行政区划（数据来源：中华人民共和国海关总署)
   * 常见人名
   * 网络提供的第三方输入法词库
   * ……

已对以上所有数据进行去重、精简处理，最终词汇量等信息详见 [![Releases](https://img.shields.io/github/last-commit/wuhgit/CustomPinyinDictionary?label=Releases&style=for-the-badge)](https://github.com/wuhgit/CustomPinyinDictionary/releases) 。


---


<div><img src="https://fcitx-im.org/fcitx.png" alt="Fcitx5 logo" width="100" align="right"></div>


# Fcitx 5


下载 `CustomPinyinDictionary_Fcitx_<版本号>.tar.gz` 并解压，得到词库文件 `CustomPinyinDictionary_Fcitx.dict`

- Linux

	将词库文件复制到目录 `/usr/share/fcitx5/pinyin/dictionaries/` 中（如果没有这个目录，您可以自行创建），重启 <u>Fcitx</u> 后即可生效。
	
   > **ArchLinux** 可以通过 [![AUR](https://img.shields.io/aur/version/fcitx5-pinyin-custom-pinyin-dictionary)](https://aur.archlinux.org/packages/fcitx5-pinyin-custom-pinyin-dictionary) 进行安装，便于后期升级更新。


- Android

	拼音输入模式下，在输入法键盘上选择 `输入法设置` > `词典`，添加词库文件即可。


---


<div><img src="https://play-lh.googleusercontent.com/X64En0aW6jkvDnd5kr16u-YuUsoJ1W2cBzJab3CQ5lObLeQ3T61DpB7AwIoZ7uqgCn4=s180" alt="Gboard logo" width="100" align="right"></div>


# Gboard (Magisk 模块)

> ![提示](https://img.shields.io/badge/-%E6%8F%90%E7%A4%BA-orange)
> - 本词库仅对 ___中文（简体） 拼音___ 的键盘语言和布局生效。
> - 如果是旧版数据用户 (即 2022-04-22 前通过直接替换文件方式进行安装的用户) ，先恢复词库至您之前备份的数据，若没有相应备份，当迁移至 Magisk 模式时，请先在模块安装时选择卸载，此时模块会将原有词库替换为空白数据，随后再进行安装。
> - 安装、升级、卸载此模块均 **不需要重启**，即时生效。
> - 词库导入后，可能需要一点时间后才能在输入时感知到新词。您可以在 `Gboard 设置` > `字典` > `个人字典` > `中文（简体）` 查看到导入后本词库的数据。

下载 `CustomPinyinDictionary_Gboard_Magisk_<版本号>.zip` ，打开 Magisk 应用，进入 `模块` 页面

- 首次安装
   1.  `从本地安装` ，选择下载的文件。
   2. 使用音量键选择`安装`。

- 升级
   - 直接检查更新并安装。

- 卸载
   1.  `从本地安装` ，选择下载的文件。
   2. 使用音量键选择`卸载`。
   3. 对本模块进行 `移除`。
    > ![注意](https://img.shields.io/badge/-%E6%B3%A8%E6%84%8F-red)
    > - 若未按流程进行卸载而直接对模块执行移除，会导致词库数据仍然存在于`个人字典`中，此时可以再按照上面的`卸载`流程重新执行一遍，随后移除模块即可。
    > - “多用户”[^multi-user] 需要在确保其它已安装此模块的用户均已卸载的情况下才能进行移除。


[^multi-user]:  这里的“多用户”指 [Android 系统自带的“多用户”功能](https://source.android.com/docs/devices/admin/multi-user)。<br/>
  Magisk 模块信息存放在系统目录，所有用户共用，而本模块写入的词库数据位于各用户独立的数据文件目录中，无法互相访问。<br/>
  如果某一用户需要使用本模块提供的词库数据，请使用该用户安装模块。<br/>
  在某一用户下进行的安装或升级操作，其它已安装本模块的用户数据会同步更新。<br/>
  如果某一用户不想再使用，单独以该用户执行卸载（只需执行 `卸载` 中的 1～2 即可），若其它用户也安装有此模块，请确保其它用户均完成卸载后再执行`移除`。<br/>
  使用 `Island`、`Shelter` 等应用创建的“多用户”需要进行一些[手动操作](https://github.com/wuhgit/CustomPinyinDictionary/issues/15#issuecomment-1272198671)。
