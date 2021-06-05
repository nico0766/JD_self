# 简介
本程序仅限青龙面板 2.0 对接使用，添加自助扫码功能。
更多功能如下：

扫码添加 / 更新 cookie
删除 cookie
查看单用户日志

------------

# 说明
本程序已开源，不存在后门等恶意代码。

https://github.com/huayu8/JDC

请勿将本程序使用于商业化行为中，否则一切后果自行承担。
由于本人技术有限，不保证程序的可用性以及安全性，由使用本程序造成的一切损失请自行承担。

在使用中发现的 bug 可在此留言，有时间会修复。

------------

## 使用环境
请确保你的环境中已经安装了青龙面板 2.0。
首先 cd 到青龙面板容器的映射目录。(***一般为 /root***)
```
cd /root
ls -l
```
如果发现有 QL 文件夹，即说明目录正确。

------------

## 下载程序
请先安装 wget 和 unzip
    
    //ubuntu
    apt install wget unzip
    //centos
    yum install wget unzip -y
	
请按照你的 cpu 架构进行下载
    
    //如果你是amd64架构（服务器，PC等）
    //wget https://github.com/huayu8/JDC/releases/download/1.0.2/linux_amd64.zip && unzip linux_amd64.zip
    //由于原来作者已经跑路，自己拉了地址
    wget https://github.com/nico0766/JD_self/blob/main/QL%E9%9D%A2%E6%9D%BF/linux_amd64.zip && unzip linux_amd64.zip
	

------------

## 开始使用
    chmod 777 JDC
    ./JDC
	
第一次运行，自动生成配置文件并且程序会自动退出。如果你没有修改过青龙面板的端口，可直接执行下一步。

如果不为默认端口，请自行修改 config.toml 文件

然后执行下面步骤
    nohup ./JDC &
	

开始后台运行程序。程序默认端口为 5701。打开 http://ip:5701 即可看到面板
如果无法打开请检查端口是否放行。
需要进/root/config.toml 修改路径
path            = "QL/config/auth.json" #QL文件路径设置，一般无需更改
修改为：
path            = "ql/config/auth.json" #QL文件路径设置，一般无需更改

------------

> https://ihuayu8.cn/ql-get-cookie.html
