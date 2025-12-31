![](https://raw.githubusercontent.com/wuhgit/CustomPinyinDictionary/main/documents/title.png)

<br/>

<div><img src="https://img.shields.io/badge/dynamic/json?style=social&label=%E6%9B%B4%E6%96%B0%E6%97%A5%E6%9C%9F&query=updateDate&url=https%3A%2F%2Fgithub.com%2Fwuhgit%2FCustomPinyinDictionary%2Fraw%2Fmain%2Fstatus.json" align="right">&emsp;&emsp;&emsp;&emsp;<img src="https://img.shields.io/badge/dynamic/json?style=social&label=%E6%95%B0%E6%8D%AE%E6%9B%B4%E6%96%B0%E8%AE%A1%E6%95%B0&query=versionNumber&url=https%3A%2F%2Fgithub.com%2Fwuhgit%2FCustomPinyinDictionary%2Fraw%2Fmain%2Fstatus.json" align="right">&emsp;&emsp;&emsp;&emsp;<img src="https://img.shields.io/badge/dynamic/json?style=social&label=%E8%AF%8D%E6%9D%A1%E6%80%BB%E8%AE%A1&query=totalWords&url=https%3A%2F%2Fgithub.com%2Fwuhgit%2FCustomPinyinDictionary%2Fraw%2Fmain%2Fstatus.json" align="right"></div>

<br/>

---

针对日常输入习惯，当前词库包含了以下内容：

* 人文类
	* 成语
	* 俗语
	* 诗歌
	* 汉语相关词典（感谢[FREEMDICT](https://forum.freemdict.com)）
	* ……
* 地理类
	* 中华人民共和国行政区划，收录`省份、城市、区县、乡镇`四级数据（感谢[Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China)）
	* 世界主要国家或地区，收录`国名全称、简称、首都`（感谢[wgii](https://github.com/occultskyrong/wgii)）
	* 世界各国和地区名称及一级行政区划（数据来源：[中华人民共和国海关总署](http://online.customs.gov.cn/)）
	* ……
* 生活类
	* 统计用产品分类目录（数据来源：[国家统计局](http://www.stats.gov.cn/)）
	* 商品目录（数据来源：京东、淘宝 等购物网站）
	* 常见人名
	* ……
* 其它
    * 第三方输入法词库
	* ……


> 已对以上所有数据进行去重、精简处理。


---


<div><img src="https://fcitx-im.org/fcitx.png" alt="Fcitx5 logo" width="100" align="right"></div>


# Fcitx 5 Linux

- 手动安装
	1. 下载词库文件 `CustomPinyinDictionary_Fcitx.dict`。
    2. > - 当前用户 `~/.local/share/fcitx5/pinyin/dictionaries/`
       > - 全局（可能需要root权限） `/usr/share/fcitx5/pinyin/dictionaries/`
	   
	   按照您的喜好选择一个目录，将词库文件复制到该目录，如之前已安装过同名词库，可以直接覆盖。
	4. 重启 <u>Fcitx</u> 后即可生效。

- 通过用户软件仓库安装
	- [![AUR](https://img.shields.io/aur/version/fcitx5-pinyin-custom-pinyin-dictionary?style=for-the-badge&logo=archlinux)](https://aur.archlinux.org/packages/fcitx5-pinyin-custom-pinyin-dictionary)


# Fcitx 5 Android 

> Q：如何打开`管理词库`？
> 
> A：Fcitx 输入法，切换至拼音输入模式（双拼或全拼皆可），在输入法键盘上选择 `输入法设置` > `管理词库`

- 手动安装
	1. 下载词库文件 `CustomPinyinDictionary_Fcitx.dict`。
	2. 使用`文件`（com.android.documentsui）打开词库文件，由于 Fcitx5 Android 输入法已经在系统中注册了 `.dict` 的打开方式，直接确定导入即可。如果此方式在您手机上无效，则可以打开`管理词库`，添加词库文件完成安装，注意，若之前已安装过本词库，需要先删除旧版本词库。

- 通过模块安装
    > 首次安装如果报错 `词库文件夹不存在` ，请打开`管理词库`，以让应用生成相关目录。
	1. 下载模块文件 `CustomPinyinDictionary_Fcitx_Magisk_<版本号>.zip` 。
	2. 使用 Magisk 或 KernelSU 应用进行安装更新。详见 [模块的使用](#模块的使用)


---


<div><img src="https://play-lh.googleusercontent.com/X64En0aW6jkvDnd5kr16u-YuUsoJ1W2cBzJab3CQ5lObLeQ3T61DpB7AwIoZ7uqgCn4=s180" alt="Gboard logo" width="100" align="right"></div>


# Gboard

![提示](https://img.shields.io/badge/-%E6%8F%90%E7%A4%BA-orange?style=for-the-badge)

> - 本词库仅对 ___中文（简体） 拼音___ 的键盘语言和布局生效。This thesaurus is only valid for ___Chinese (Simplified) Pinyin___ keyboard language and layout.
> - 词库数据通过模块进行安装，支持 Magisk 及 KernelSU
> - 当前词库在使用上会有一些限制和问题，详情请查看 [相关issue](https://github.com/wuhgit/CustomPinyinDictionary/issues/21)。
> - 如果是旧版数据用户 (即 2022-04-22 前通过直接替换文件方式进行安装的用户) ，先恢复词库至您之前备份的数据，若没有相应备份，当迁移至 Magisk 模式时，请先在模块安装时选择卸载，此时模块会将原有词库替换为空白数据，随后再进行安装。
> - 词库导入后，可能需要一段时间后才能在输入时感知到新词。您可以在 `Gboard 设置` > `字典` > `个人字典` > `中文（简体）` 查看到本词库导入后的数据。

下载模块文件 `CustomPinyinDictionary_Gboard_Magisk_<版本号>.zip` ，使用 Magisk 或 KernelSU 应用进行安装更新。详见 [模块的使用](#模块的使用)

---

<div><img src="https://upload.wikimedia.org/wikipedia/commons/b/b8/Magisk_Logo.png" alt="Magisk logo" width="100" align="right"></div>
<div><img src="https://kernelsu.org/logo.png" alt="kernelsu logo" width="100" align="right"></div>

# 模块的使用

![提示](https://img.shields.io/badge/-%E6%8F%90%E7%A4%BA-orange?style=for-the-badge)

> 由于我现有的几台设备均已无法升级到最新的系统、 Magisk 或 KernelSU，符合个人使用需求且能解锁BL的新机几乎不存在，换机计划一再推迟，我不能保证模块在后续使用中如果出现问题能够如以前一样及时排障，加之考虑到诸位可能面临相似困境，且在这种现状下，模块面临的碎片化问题会更加严重，本着尽责的态度，做出了停止更新模块的决定，v20260101将成为最终的模块版本。
> 
> 针对 Fcitx 用户，建议完全迁移到手动安装方式，通过模块安装只是为了方便管理更新，后续应该会有更优雅的解决方式。
> 
> 针对 Gboard 用户，若您的设备已经解锁BL并Root，可以考虑通过命令行进行手动安装。
> 
> 由衷感谢各位模块用户在过去五年（2020.11-2026.01）的使用和支持！！！

---

> 安装、升级、卸载此模块均 **不需要重启** ，即时生效。

打开 Magisk 或 KernelSU 的应用，进入 `模块` 页面

- 首次安装
   1.  `从本地安装` ，选择下载的模块文件。
   2. 使用音量键选择`安装`。

- 升级
   - 直接检查更新并安装。

- 卸载
   1.  `从本地安装` ，选择下载的模块文件。
   2. 使用音量键选择`卸载`。
   3. 对本模块进行 `移除`。
    > ![注意](https://img.shields.io/badge/-%E6%B3%A8%E6%84%8F-red?style=for-the-badge)
    > - 若未按流程进行卸载而直接对模块执行移除，会导致词库数据仍然存在，此时可以再按照上面的`卸载`流程重新执行一遍，随后移除模块即可。
    > - “多用户”[^multi-user] 需要在确保其它已安装此模块的用户均已卸载的情况下才能进行移除。


---


[^multi-user]:  这里的“多用户”指 [Android 系统自带的“多用户”功能](https://source.android.com/docs/devices/admin/multi-user)。<br/>
  模块信息存放在系统目录，所有用户共用，而本模块写入的词库数据位于各用户独立的数据文件目录中，无法互相访问。<br/>
  如果某一用户需要使用本模块提供的词库数据，请使用该用户安装模块。<br/>
  在某一用户下进行的安装或升级操作，其它已安装本模块的用户数据会同步更新。<br/>
  如果某一用户不想再使用，单独以该用户执行卸载（只需执行 `卸载` 中的 1～2 即可），若其它用户也安装有此模块，请确保其它用户均完成卸载后再执行`移除`。<br/>
  使用 `Island`、`Shelter` 等应用创建的“多用户”需要进行一些[手动操作](https://github.com/wuhgit/CustomPinyinDictionary/issues/20)。
