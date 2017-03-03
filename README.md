# Rime 自用配置

- 一直以来只是简单配置了 Rime 在使用，感谢 [scomper](https://medium.com/@scomper) 的文章: [「鼠鬚管」的调教笔记](https://medium.com/@scomper/%E9%BC%A0%E9%A0%88%E7%AE%A1-%E7%9A%84%E8%B0%83%E6%95%99%E7%AC%94%E8%AE%B0-3fdeb0e78814#.8d1na3s5q), 让我发现了更好的用法.
- 按个人需求只保留了拼音简体 & 双拼, 并稍作个人习惯的修改, 有其他输入需求请访问 scomper 的 medium 下载原始配置.
- 中英、全角、符号习惯快捷键切换，从输入法切换菜单中移除.
- 确信自己拼写标准, 移除了模糊音.
- Win 中字体习惯用方正隶变.

## 部署

- 根据系统二选一的文件:
    - Mac: Squirrel.custom
    - Win: weasel.custom
    - custom 配置样式 + 末尾配置默认英文的程序
- 其他文件通用覆盖

> Mac 留了两套主题(仿系统&绿色清新)

- simp.custom & flypy.custom 中自定义符号表:

    ```
    symbols:
    '/xx': [ 1, 2, 3 ]
    // 默认符号表: symbols 文件中
    ```

- custom_phrase, 文本替换:完全匹配,编码不能有空格.

## 遗憾

- 中英混合词组扩展导致某些分词异常,可在 pinyin.extended 中注释 cn_en;

    ```
    // 词库
    luna_pinyin.sgmain.dict.yaml，搜狗细胞词库
    luna_pinyin.cn_en.dict.yaml，英文、中英文混合短语和名词
    luna_pinyin.emoji.dict.yaml，表情符号
    luna_pinyin.hanyu.dict.yaml，汉语大词典
    luna_pinyin.kaomoji.dict.yaml，颜文字表情符号
    luna_pinyin.poetry.dict.yaml，唐诗宋词、千家集、楚辞、诗经
    ```

## 编译

- 新版本，新特性：新版候选高亮可以填充满背景色了。
- 感谢: [placeless](https://github.com/placeless)的文章: [我的鼠须管配置](http://placeless.net/2016/08/24/my-rime-squirrel-config.html)

- 自己编译新版本

    ```shell
    // 安装并启动 XCode，确认一下条款 (光有 Command Line Tool 是不行的)
    brew install cmake git boost
    git clone --recursive https://github.com/rime/squirrel.git
    cd squirrel
    make deps
    make
    sudo make install
    ```

- 把编译好的 APP 留到下一次重装系统之后安装使用

    ```shell
    // 把编译好的 Squirrel.app 复制到 /Library/Input Methods 目录下：
    cp -R YOUR_PATH/Squirrel.app "/Library/Input Methods"
    // 然后跑一下 postflight 脚本即可：
    sudo /Library/Input\ Methods/Squirrel.app/Contents/Resources/postflight
    ```


> 或者: 把保存的 Squirrel.app 复制到 `/Library/Input Methods` 下，注销重登入，将其加入输入法选单，「部署」即可。
> 差别在于: postflight 是把数据文件生成在 `/Library/Input Methods/Squirrel.app/Contents/SharedSupport/` 
> 后一种方法是把数据文件生成在 `~/Library/Rime/` 

## iRime

- 直接导入配置, 繁转简, 基本可用;
- GO!~
