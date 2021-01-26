# 自建拼音输入法词库

---

目前提供 `Fcitx5 (Linux)` 以及 `Gboard (Android)` 两种词库数据格式。

当前词库，包含了以下内容：

* 常见的成语、俗语、诗歌等
* 中华人民共和国四级行政区划名称（感谢[Administrative-divisions-of-China](https://github.com/modood/Administrative-divisions-of-China)）
* 世界各个国家国名全称、简称（感谢[wgii](https://github.com/occultskyrong/wgii))
* 常见人名
* 网络提供的第三方输入法词库
* ……

已对以上所有数据进行去重、精简处理，最终词汇量为 `747,892` (Releases/2021-01-26)。

---

# 使用方法

---

## Fcitx5

下载 `PersonalDictionary_fcitx.dict`，将其复制粘贴到目录 `~/.local/share/fcitx5/pinyin/dictionaries/` 中（如果没有这个目录，您可以自行创建），重启 `Fcitx` 后即可生效。

---

## Gboard

⚠️警告！

**因为词库词条数量过多，目前不能在 Gboard 中直接导入，使用此词库需要 root 权限对原有词库数据库进行替换，这将会覆盖您输入法中已有的所有个人词库数据，请在操作前做好相关备份！**

您需要执行以下操作：

- 下载 `PersonalDictionary.db`
- 切换到其它输入法 或者 在 Android 的 管理屏幕键盘 中关闭 Gboard
- 在应用设置中清除 Gboard 的缓存
- 将 `PersonalDictionary.db` 复制到 `/data/data/com.google.android.inputmethod.latin/databases` 中替换原有文件
- 切换回 Gboard 或者 在 Android 的 管理屏幕键盘 中打开 Gboard

您可能需要注意：

由于是采用数据库替换的方式，您现有的个人词库将会被覆盖，请自行备份相关数据，主要是 `/data/data/com.google.android.inputmethod.latin/databases/PersonalDictionary.db` 。
  
在导入之前，请确保 Gboard 不是您手机上唯一的输入法，以免发送其它意外。
  
词库导入后，可能需要一点时间后才能在输入时感知到新词，期间 Gboard 可能会在通知栏以 **正在改善您的打字输入体验** 进行提示。
  
您可以在 `Gboard 设置 > 字典 > 个人字典 > 中文（简体）` 查看最终导入的数据。

为获得更好的使用体验，建议对 Gboard 中以下设置进行修改：

`Gboard 设置 > 高级 > 学习`

- 关闭 **个性化设置**
- 关闭 **改进语音和输入功能，让所有用户受益**
