Code Prettify 
### 介绍

基于prismjs的代码语法高亮typecho插件，支持众多常见的代码语言高亮显示，提供11种代码高亮风格自由切换，支持显示代码语言类型、行号，以及支持复制代码到剪切板功能

最新更新时间：`2019-11-18`

### 起始

最初基于 Highlight 插件，开发一款名为ColorHighlight插件

但因为插件本身存在不少BUG，自己又不想重写结构，于是便重新基于CodeHighlighter开发了一款

依旧在原有的代码高亮样式上新增了Mac风格，修改了部分JS代码

### 激活

以Handsome主题为例：

第 1 步：下载本插件，解压，放到 usr/plugins/ 目录中；

第 2 步：文件夹名改为 CodePrettify；

第 3 步：登录管理后台，激活插件 （请勿与其它同类插件同时启用，以免互相影响）

第 4 步：设置：选择主题风格，是否显示行号等。

### 用法

```
\```php(语言类型选填)
<?php echo 'hello jrotty!'; ?>
\```
删除上边代码中的\
```

### Pjax

如果你的网站有开启Pjax

请把以下代码添加到回调函数的地方，在你使用的主题设置里看看

```javascript
if (typeof Prism !== 'undefined') {
var pres = document.getElementsByTagName('pre');
                for (var i = 0; i < pres.length; i++){
                    if (pres[i].getElementsByTagName('code').length > 0)
                        pres[i].className  = 'line-numbers';}
Prism.highlightAll(true,null);}
```

### 重要说明

#### 可设置项

1. 选择高亮主题风格 (官方提供的 8 种风格切换，本人自己新增了三种（Mac风格）)

- coy.css
- dark.css
- BlackMac.css（黑色Mac风格）
- GrayMac.css （默认选中：Mac风格（灰色））
- WhiteMac.css（白色Mac风格）
- twilight.css
- tomorrow-night.css
2. 是否在代码左侧显示行号 （默认开启）

### 后记

插件的兼容性应该不存在什么问题，博主在Handsome主题上使用一切正常

如果你在其他主题使用过程中出现了问题可以随时联系我

若有任何意见或发现任何BUG欢迎访问到我的博客www.xcnte.com留言
