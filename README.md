# Rime 配置

新版 Rime 安装配置步骤

## Install

### Mac
```shell
# homebrew
brew cask install squirrel
```

### Win
- [下载](https://rime.im/download/)

## Plan

### Mac

```Shell
# 东风破 Plum
git clone --depth 1 https://github.com/rime/plum.git
cd plum
bash rime-install --select :all lotem/rime-forge/lotem-packages.conf
# 数字选择，小数点结束。
```

### Win

-   获取更多输入方案；

    ```Shell
    Enter package name, URL, user/repo or download ZIP to install:<rime-double-pinyin>
    # plum 页面方案名
    ```

-   [方案列表](https://github.com/rime/plum)
-   选择主题、指定用户目录；

## Patch

细节调整，自行补充；

-   共用：default.custom.yaml

-   Mac：squirrel.custom.yaml
-   Win：weasel.custom.yaml