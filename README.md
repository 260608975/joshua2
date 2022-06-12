解决VPS时间无法同步的一般方法

 一般来说，可以通过在VPS中执行以下命令，来设置时区并且同步将时间与北京时间进行同步：
 
rm -rf /etc/localtime
ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
yum install -y ntp
ntpdate us.pool.ntp.org
date
