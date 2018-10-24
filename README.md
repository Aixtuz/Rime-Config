# Rime 自用配置

- 一直以来只是简单配置了 Rime 在使用，感谢 [scomper](https://github.com/scomper) 的文章: [「鼠鬚管」的调教笔记](https://scomper.me/gtd/-shu-xu-guan-de-diao-jiao-bi-ji), 让我发现了更好的用法。
- 按个人需求只保留了拼音简体 & 小鹤双拼, 并根据个人习惯稍作修改, 如有需求建议 参考 scomper 的[原始配置](https://github.com/scomper/Rime)。

## 安装

``` zsh
brew cask install squirrel
# brew install squirrel # 不是 Rime
```

## 部署

- 覆盖用户设置进行部署；
- Win 平台的 `weasel.custom.yaml` 参考 `squirrel.custom.yaml` 配置；

## 编译

- 新版本，新特性：候选高亮可以充满背景色。

- 自己编译新版本

    ``` zsh
    # dev tools:
    brew install git
    brew install cmake
    # libraries:
    brew install boost
    # Repositories
    git clone --recursive https://github.com/rime/squirrel.git
    # cd squirrel
    make deps
    make
    # build 中找到生成文件
    ```


- 替换新版 App
    1. 移除 Rime 输入法，并注销；
    2. 替换 /Library/Input Methods/ 中的 App；
    3. 运行 & 部署；


## iOS

- 早期在塞班和安卓上一直使用点讯/百度，优点是可以自定义布局和方案，安卓早期版本也很轻量，只是后来的体积和隐私都让人心生抵触。 
- iOS 端使用过 iRime 和落格等，优点方面：iRime 配置和 Rime 通用，落格是细节亮眼，最终放弃的原因都在于纠错能力，移动端的小键盘实在是太容易点错了。
- iOS 原生推出双拼以后，也曾尝试使用，只是由于习惯了小鹤方案并且原生双拼键盘布局比较奇怪，所以也放弃了。
- 最终使用至今的是 Google 的 Gboard，感受中的纠错能力最好，日常聊天不在意选错字的话，甚至可以闭眼打字。
- iOS 中所有第三方都存在同样的缺点：系统某些情境使用受限，所以还是非常期望原生可以调整下布局 & 支持小鹤方案，当然能自定义方案就更好了。

