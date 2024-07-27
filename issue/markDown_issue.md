## 简介  
以下内容为本人在vscode使用markdown预览格式并上传至GitHub后遇见的问题  
<span id="title">这里是标题</span>  

## 目录
1. [本地仓库跨文档链接点击正常跳转，上传后点击github链接出现404](#1-仓库文档引用出现404)  
```404 - page not found```
2. [文档内普通文本跳转(试用)](#2-本地非标题文本跳转)

## 内容
### 1. 仓库文档跳转出现404
> 以本仓库举例  
> 本地引用：[使用GitHub遇见的问题](/self_study/issue/git_issue.md)  
> 链接内容为：```[使用GitHub遇见的问题](/self_study/issue/git_issue.md)```  
> 出现问题：本地点击会正常跳转文件，但github会显示404  
> 解决方式：[使用GitHub遇见的问题](/issue/git_issue.md) 删除掉`/issue`即可  
> 链接内容为：```[使用GitHub遇见的问题](/issue/git_issue.md)```  
> 查找原因：github会在跨文档链接前默认添加仓库名称导致文档跳转失败  

### 2. 本地非标题文本跳转  
> 以本文档举例  
> 本地引用: [标题](#title)  
> 链接内容为：```[标题](#title)```  
> 终点内容为：```<span id="title">这里是标题</span>```  
> 实现方式：html标签实现  
> 解决方案来源：https://www.cnblogs.com/JohnTsai/p/4027229.html  