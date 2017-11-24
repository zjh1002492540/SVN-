---
title: 更新内容
tags: 更新说明,小书匠
---


# 小书匠收费

## 收费与不收费的区别

### 收费

#### 收费项目
1. pdf 定制化导出(pdf封面，水印，加密等)
2. 支持在线更新，优先使用新功能

#### 收费价格

1. 一年 20￥, 两年 40￥。 目前只支持两年，如果付费超过 40￥,只能算做两年的套餐。
 
### 不收费

1. 免费又实用的功能太多了，不知道重点写什么好，自己到 http://soft.xiaoshujiang.com/feature.html 这里看吧.....

## 其他

http://soft.xiaoshujiang.com/price.html

___

# 升级日志

## 注

新版调整了底层应用名称 `小书匠` 为 `storywriter`，对旧数据及配置有保留的用户，需要手动调整相应文件夹的名称

例如在 linux 环境下

```
在数据文件目录下 /home/suziwen/.config/小书匠/Default/IndexedDB 的内容

chrome-extension_cggoamjkdfofnimkkbdmnlhjacbfipgg_0.indexeddb.leveldb
chrome-extension_cggoamjkdfofnimkkbdmnlhjacbfipgg_0.indexeddb.blob
复制到
/home/suziwen/.config/storywriter/Default/IndexedDB 目录下，并且重命名为
chrome-extension_jalbgaejjmdihbhmdepjgcdikbeclnbe_0.indexeddb.leveldb
chrome-extension_jalbgaejjmdihbhmdepjgcdikbeclnbe_0.indexeddb.blob


在数据文件目录下 /home/suziwen/.config/小书匠/Default/Local Storage 的文件
chrome-extension_cggoamjkdfofnimkkbdmnlhjacbfipgg_0.localstorage
复制到
/home/suziwen/.config/storywriter/Default/Local Storage/ 目录下，并且重命名为 
/home/suziwen/.config/storywriter/Default/Local Storage/chrome-extension_jalbgaejjmdihbhmdepjgcdikbeclnbe_0.localstorage

```

数据库文件路径

```
Windows: %LOCALAPPDATA%/小书匠/
Mac: ~/Library/Application Support/小书匠/
Linux: ~/.config/小书匠
```

___


## 4.2.1

### 4.2.1 修改

1. 修复码云认证入口无法正常认证问题


## 4.2.0

### 4.2.0 新功能

1. 会员用户可以自定义 pdf 导出里目录样式 [查看教程](https://github.com/suziwen/blogxiaoshujiang/blob/master/2017-9-24%20%E5%B0%8F%E4%B9%A6%E5%8C%A0%20pdf%20%E5%AF%BC%E5%87%BA%E8%87%AA%E5%AE%9A%E4%B9%89%20css%20%E6%95%99%E7%A8%8B.md)
2. 添加 pdf 导出水印透明度设置

### 4.2.0 修改

1. 解决快捷键保存，退出水印预览模式不生效问题 #536 #476
2. ace 默认行高调整到 1.4
3. 解决 codemirror vim 模式下快捷键冲突问题 #534 #454
4. 客户端托盘图标消失问题 #537
5. 不再使用 cledit 编辑器
6. 调整预览区资源动态加载
7. 预览内的链接跳转会引起界面错位 #541
8. codemirror 编辑器（开启英文检查）总是提示 加载词典超时 #545
9. 升级 codemirror 编辑器到 5.30.0
10. pdf 封面换行算法修改为 `break-word`
11. codemirror 文本高亮颜色选择器在代码块显示的问题 #549

## 4.1.0

### 4.1.0 新功能

1. 添加 xsjimg 语法支持（[使用说明](https://github.com/suziwen/blogxiaoshujiang/blob/master/2017-9-15%20%E5%B0%8F%E4%B9%A6%E5%8C%A0%20xsjimg%20%E8%AF%AD%E6%B3%95%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.md)）

### 4.1.0 修改

1. 修正在较小窗口时，工具栏按钮提示名称被显示出来,太占用空间的问题
2. 修复 window 版本关联打开失败的问题 #526
3. 插入图片按钮支持 svg 格式图片 （svg 格式图片在印象笔记里会被当成附件处理）
4. 允许用户显示查看已经绑定印象(Evernote)笔记的 token

## 4.0.0

### 4.0.0 新功能

1. 小书匠也收费了......
2. 客户端加入了在线更新功能 (会员)
3. pdf 导出分成本地 pdf 导出和联网 pdf 导出
4. 联网 pdf 导出添加了 pdf 封面，水印，加密功能 (会员用户专用，非会员用户只能设置小书匠固定的内容，加密的密码随机)
5. 查找(`ctrl+f`)界面添加替换按钮，解决用户找不到 ==查找替换== 的功能(`ctrl+f,ctrl+f`)
6. 联网 pdf 导出支持 `@media print` 语法
7. 高亮语法支持指定颜色, ==红色 #ea0c2e==

___

### 4.0.0 修改

1. zip 导入失效 #466
2. 升级 jsyaml 到 3.9.1 ， 解决 emoji 符号不能做为标题的问题
3. 跟进为知新版同步方式的 api 的修改 #491
4. 印象笔记没有文档，会一直显示不出来 #489
5. 客户端搜索无法高亮显示不突出 #499
6. 解决 window 非中文版本安装客户端乱码问题 #473
7. 调整底层应用名称为 storywriter
8. 发布到 metaweblog 支持直接写 xmlrpc 地址 #504
9. 更详细的博客发布错误日志
10. 代码高亮部份 css 文件没正确加载引起高亮不完整 #467
11. 显示行号的代码块在 pdf 打印时字体变大
12. 修复 codemirror 显示不可见元素不生效问题
13. 抓取全部 evernote 文章 #517
14. 转为PDF格式时， 标题会缩进 #509
15. 代码块允许自动折行
