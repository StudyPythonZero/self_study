## github使用遇见的问题和解决方式
**就是把自己遇见的问题整理一下上传**
### 目录
1. [虽然添加了账号公钥，但还是上传失败(ED25519)](#1-warning-permanently-added-githubcom-ed25519-to-the-list-of-known-hosts-gitgithubcom)  
```Warning: Permanently added ‘github.com’ (ED25519) to the list of known hosts. git@github.com```
2. [连接github时出现22端口无法连接](#2-ssh-connect-to-host-githubcom-port-22-connection-timed-out)  
```ssh: connect to host github.com port 22: Connection timed out```  
3. [本地推送没有报错，且已经使用git add和git commit，但Github内容不更新](#3-本地推送没有报错但github内容不更新)  
```（第一次开始学习使用仓库，不确定是否为自身问题）```  

### 内容
#### 1. ```Warning: Permanently added ‘github.com’ (ED25519) to the list of known hosts. git@github.com```  
> 解决方式：添加windows -ssh  
> 网址参考，CSDN的NF_ye老师：https://blog.csdn.net/NF_ye/article/details/127475332  
#### 2. ```ssh: connect to host github.com port 22: Connection timed out```
> 解决方式：把自己的加速器关掉就好
> 参考方式（没试过）：切换连接端口
> 网址参考，CSDN的kuilaurence老师：https://blog.csdn.net/kuilaurence/article/details/135909974  
#### 3. ```本地推送没有报错，但Github内容不更新```
> 备注：该问题为第一次按照“GitHub”入门与实践"3.2章节设置时出现的问题，输入```git commit```后网站上的github仓库并未更新内容
> 问题描述：使用了```git init```且完成了仓库链接、```git add```和```git commit```操作，但是github网站没有更新内容  
> 解决方式：使用```git push -u origin master```命令处理
> 参考网址，CSDN的白蛇仙人老师：https://blog.csdn.net/mudooo/article/details/89684398


