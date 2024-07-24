## 简介  
以下内容为本人在vscode使用markdown预览格式并上传至GitHub后遇见的问题  
---
## 目录
1. [本地仓库跨文档链接引用正常，上传后点击github链接出现404](#1-仓库文档引用出现404)  
```404 - page not found```

## 内容
### 1. 仓库文档引用出现404
> 以本仓库举例  
> 本地引用：[使用GitHub遇见的问题](/self_study/issue/git_issue.md)  
> 链接内容为：```[使用GitHub遇见的问题](/self_study/issue/git_issue.md)```  
> 出现问题：本地点击会正常跳转文件，但github会显示404  
> 解决方式：[使用GitHub遇见的问题](/issue/git_issue.md) 删除掉`/issue`即可  
> 链接内容为：```[使用GitHub遇见的问题](/issue/git_issue.md)```  
> 查找原因：github会在跨文档链接前默认添加仓库名称导致文档跳转失败  