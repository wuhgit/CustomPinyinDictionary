# 自建拼音输入法词库


---

鉴于 [Gboard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin) 孱弱的中文词库，在结合网上各方面的资源后，对其进行补充增强。

整个过程受到 [此处](https://github.com/studyzy/imewlconverter/issues/111) 的启发，深表感谢！

---

# ⚠️警告！

**导入此词库将会覆盖您输入法中已有的所有个人词库数据，请在操作前做好相关备份！**


---

## Q&A

### 既然 Gboard 这么弱，为什么不用XX输入法？

纯属个人喜好，我并不喜欢那些打着输入法的名义却塞进了太多乱七八糟功能的应用，如果您有合适的输入法，欢迎推荐。


### 为什么采用覆盖数据库的方式进行？

我曾经尝试过直接导入，由于数据量庞大，耗时很久且失败率相当之高，如果采用数据库替换的方式进行，基本上可以很快速的一次成功。


### 数据量为什么这么大？

当前数据库，包含了以下内容：

* 常见的成语、俗语、诗歌等
* 中华人民共和国四级行政区划名称（感谢[Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China)）
* 世界各个国家国名全称、简称（感谢[wgii](https://github.com/occultskyrong/wgii))
* 常见人名
* 网络提供的第三方输入法词库
* ……

已对以上所有数据进行去重、精简处理，最终词汇量为 1,085,476 (Releases/2020-11-01)。
  
因为暂不清楚 Gboard 自带的词汇范围，双方肯定存在大量重叠，如果后期找到相关数据，会进行进一步精简处理。


### 我要如何导入这个数据库

您所需要做的，就是把这个数据库复制到 `/data/data/com.google.android.inputmethod.latin/databases` 中替换原有文件。
  
这个过程中很可能需要root权限。
  
如果您有使用 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm)，可以使用我提供的这个 [tasker](https://raw.githubusercontent.com/wuhgit/CustomPinyinDictionary/main/tasker/Tasker_Gboard%E5%AF%BC%E5%85%A5%E8%AF%8D%E5%BA%93.tsk.xml) 配置文件，把它导入到 Tasker 中，再将下载解压后的 `PersonalDictionary.db` 置入您手机存储器的 `Download` 目录中，执行即可。


### 有其它需要注意的问题吗

由于是采用数据库替换的方式，您现有的个人词库将会被覆盖，请自行备份相关数据，主要是 `/data/data/com.google.android.inputmethod.latin/databases/PersonalDictionary.db` 。
  
在导入之前，请确保 Gboard 不是您手机上唯一的输入法，以免发送其它意外。
  
词库导入后，可能需要一点时间后才能在输入时感知到新词，期间 Gboard 可能会在通知栏以 **正在改善您的打字输入体验** 进行提示。
  
您可以在 `Gboard 设置 > 字典 > 个人字典 > 中文（简体）` 查看最终导入的数据。


### 后期会提供其它输入法的词库吗？

待定，不过您可以直接从现在的数据库文件中导出词汇，再使用 [深蓝词库转换](https://github.com/studyzy/imewlconverter) 转换为您所需要的格式。
