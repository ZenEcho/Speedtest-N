# Speedtest-N

**基于LibreSpeed和speedtest-x**

**本库是东凑西拼的屎山和bug堆起来的，能跑起来是个奇迹。**

**支持单线程，多线程**

**支持测速记录查询**

# 使用方法

**面板部署：**

下载本仓库并解压到网站目录。

1、访问 {域名}/index.html 进行测速

2、打开 {域名}/results.html 查看测速记录

3、results.html页面提示接口报错，是因为没有权限。请给予目录755权限

```bash
Tips：backend/config.php 中可定义一些自定义配置：
MAX_LOG_COUNT = 100：最大可保存多少条测速记录
IP_SERVICE = 'ip.sb'：使用的 IP 运营商解析服务(ip.sb 或 ipinfo.io)
SAME_IP_MULTI_LOGS = false：是否允许同一IP记录多条测速结果
```
**非面板部署：**
```bash
yum install httpd php git -y
git clone https://github.com/youheiss/Speedtest-N.git
cd Speedtest-N/
cp -R backend/ chartjs/ *.html *.js /var/www/html/
cd /var/www/html/
chown -R apache *
systemctl start httpd  #重启httpd服务
```
**其他**

正常部署是没有任何问题的，如果出错了就是你的问题

# 参考的库（我抄袭的库）

https://github.com/librespeed/speedtest

https://github.com/BadApple9/speedtest-x
