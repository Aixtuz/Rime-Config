# Rime 自用配置

- 一直以来只是简单配置了 Rime 在使用，感谢 [scomper](https://medium.com/@scomper) 的文章, 让我发现了更好的用法.
- 按个人需求只保留了拼音简体 & 双拼, 并稍作个人习惯的修改, 有其他输入需求请访问 scomper 的 medium 下载原始配置.
- 中英、全角、符号习惯快捷键切换，从输入法切换菜单中移除.
- 符号是否直接上屏(Markdown /bq).
- 确信自己拼写标准, 移除了模糊音.
- Win 中字体习惯用方正隶变.

## 部署

- 根据系统二选一的文件:
  - Mac: Squirrel.custom
  - Win: weasel.custom
  - custom 配置样式 + 末尾配置默认英文的程序.
- 其他文件通用覆盖.

> Mac 留了两套主题(仿系统&绿色清新).

- simp.custom & flypy.custom 中自定义符号表:

  ```
  symbols:
    '/xx': [ 1, 2, 3 ]
  // 默认符号表: symbols 文件中.
  ```
  
- custom_phrase, 文本替换:完全匹配,编码不能有空格.

## 遗憾

- 中英混合词组扩展导致某些分词异常(如 win 中: sf、qingk),可在 pinyin.extended 中注释 cn_en.

  ```
  // 词库
  luna_pinyin.sgmain.dict.yaml，搜狗细胞词库
  luna_pinyin.cn_en.dict.yaml，英文、中英文混合短语和名词
  luna_pinyin.emoji.dict.yaml，表情符号
  luna_pinyin.hanyu.dict.yaml，汉语大词典
  luna_pinyin.kaomoji.dict.yaml，颜文字表情符号
  luna_pinyin.poetry.dict.yaml，唐诗宋词、千家集、楚辞、诗经
  ```
  
## iRime

- 直接导入 Rime 配置、繁转简.
- GO!~
