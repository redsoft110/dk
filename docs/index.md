# Linux 命令 

https://www.toolhelper.cn/EncodeDecode/Base64

https://htmlcolorcodes.com/zh/yanse-biao/

https://www.bilibili.com/video/BV1BT4y1W7Aw/?spm_id_from=333.788.player.switch&vd_source=297b5a0462c10937129b257b1c5dc776&p=8

https://www.bilibili.com/video/BV1LAKgzXEiL/?vd_source=297b5a0462c10937129b257b1c5dc776


https://www.bilibili.com/video/BV1BYLCzCEbS/?spm_id_from=333.337.search-card.all.click&vd_source=297b5a0462c10937129b257b1c5dc776


https://www.bilibili.com/video/BV1gM411W7ex/?spm_id_from=333.337.search-card.all.click&vd_source=297b5a0462c10937129b257b1c5dc776

https://www.bilibili.com/video/BV1JYNZeNEy4/?spm_id_from=333.337.search-card.all.click&vd_source=297b5a0462c10937129b257b1c5dc776

https://mkdocs.org.cn/user-guide/cli/

https://learn.microsoft.com/zh-cn/azure/app-service/quickstart-nodejs?tabs=windows&pivots=development-environment-vscode

https://www.snapcnt.com/post/20.html

https://www.bilibili.com/video/BV1oz421q7BB/?spm_id_from=333.337.search-card.all.click&vd_source=297b5a0462c10937129b257b1c5dc776

https://www.bilibili.com/video/BV1a34y167AZ/?spm_id_from=333.788.videopod.episodes&vd_source=297b5a0462c10937129b257b1c5dc776&p=6

https://www.bilibili.com/video/BV1gM411W7ex/?spm_id_from=333.337.search-card.all.click&vd_source=297b5a0462c10937129b257b1c5dc776

https://search.bilibili.com/all?vt=85223851&keyword=%E5%88%B6%E4%BD%9C%E9%82%AE%E4%BB%B6%E6%9C%8D%E5%8A%A1%E5%99%A8&from_source=web_search&spm_id_from=333.1007&search_source=5

# youtube

https://www.youtube.com/watch?v=W9QX3fphyes

https://www.youtube.com/watch?v=NhhyCl1w-4c

# clode

https://www.tailwindcss.cn/docs/text-color

https://www.jb51.net/tools/html_jiami.htm

# 图标

https://fontawesome.com/v4/icon/windows

https://blog.oool.cc/archives/google-cloud-free-tier-200gb-traffic-ultimate-guide-2026

# mkdocs
https://wcowin.work/

# 音标
 
pronounce.renlab.ai



Linux 常用命令大全（分类整理，直接复制用）

一、基础信息（查看系统、主机）

pwd # 查看当前所在目录

ls # 列出目录文件

ls -l 详细列表（权限、大小、时间）

ls -a 显示隐藏文件（.开头）

ls -lh 人性化显示文件大小（KB/MB）

whoami # 当前登录用户名

hostname # 主机名

uname -a # 完整系统内核信息

cat /etc/os-release # 查看系统发行版（Ubuntu/CentOS）

二、目录操作（cd、mkdir、rmdir）

cd /home # 进入指定目录

cd ~ 回到用户家目录

cd ..返回上一级目录

CD - 回到上次所在目录

mkdir test # 创建文件夹
mkdir -p a/b/c 递归创建多级目录
rmdir test # 删除空文件夹
三、文件操作（增删改查）
1.创建文件
bash
运行
touch touch 1.txt
echo “内容” > test.txt
2.查看文件
bash
运行
cat test.txt # 一次性读取全部内容
less test.txt # 分页查看（空格翻页 q退出）
head -10 test.txt # 查看前10行
tail -20 test.txt # 查看最后20行
tail -f test.txt # 实时监控日志（常用）
3.复制、移动、重命名
bash
运行
CP a.txt /tmp/ # 复制文件
cp -r 文件夹 /tmp/ # 复制文件夹（-r递归）
mv a.txt b.txt # 重命名
mv a.txt /tmp/ # 移动文件
4.删除（谨慎！）
bash
运行
rm 1.txt # 删除文件
rm -rf folder # 强制删除文件夹（无回收站）
# 禁止直接 rm -rf / 会清空系统！
四、权限管理 chmod /chown
1.修改文件权限
bash
运行
chmod 755 test.sh # 数字权限
chmod +x test.sh # 添加执行权限
权限数字说明：4 读 2 写 1 执行
755：所有者读写执行，组 / 其他读执行
644：所有者读写，其他人只读（普通文件）
2.修改文件归属用户 / 组
bash
运行
chown root：root test.txt
chown -R www：www /www # 递归修改文件夹所有者
五、查找文件 / 内容 find、grep
1.Find 查找文件
bash
运行
find / -name “*.log” # 全盘查找后缀log文件
find ./ -type f -size +100M # 查找当前目录大于100M文件
2.grep 过滤文本（最常用）
bash
运行
grep “关键词” test.txt
grep -i “error” log.txt # -i忽略大小写
grep -n “warn” log.txt # -n显示行号
grep -r “关键词” /var/log # 递归搜索目录下所有文件
六、压缩解压 tar/zip/unzip
tar（Linux 通用打包）
bash
运行
# 压缩 tar.gz
tar -zcvf 打包名.tar.gz 文件夹/文件
# 解压 tar.gz
tar -zxvf 打包名.tar.gz

# tar.bz2
tar -jcvf xxx.tar.bz2 源文件
tar -jxvf xxx.tar.bz2
参数：z （gz） j （bz2） c 压缩 x 解压 v 显示过程 f 指定包名
zip/unzip
bash
运行
zip -r test.zip ./test/ # 压缩文件夹
unzip test.zip -d /tmp # 解压到/tmp目录
七、进程、端口、系统资源
1.查看进程
bash
运行
ps aux # 全部进程
top # 实时系统资源（q退出）
htop # 更美观的top（需安装）
pstree # 进程树
2.杀死进程
bash
运行
kill 进程 PID
kill -9 PID # 强制杀死
3.查看端口占用
bash
运行
netstat -tulnp
ss -tulnp
lsof -i：80 # 查看80端口被哪个程序占用
八、网络命令
bash
运行
ip addr / ifconfig # 查看网卡IP
ping baidu.com # 测试网络连通
curl 网址 # 访问网页接口
wget 下载地址 # 下载文件
systemctl restart network # 重启网络服务（centos）
systemctl restart NetworkManager # ubuntu重启网络
九、软件服务管理 systemctl（主流）
bash
运行
systemctl start nginx # 启动服务
systemctl 停止 nginx # 停止
systemctl restart nginx # 重启
systemctl enable nginx # 开机自启
systemctl disable nginx # 取消开机自启
systemctl status nginx # 查看服务运行状态
十、磁盘、内存查看
bash
运行
df -h # 查看磁盘分区使用情况
du -sh * # 查看当前目录各文件夹大小
free -h # 查看内存、swap交换分区
十一、用户管理
bash
运行
useradd testuser # 创建用户
passwd testuser # 设置密码
userdel -r testuser # 删除用户并删除家目录
groupadd testgroup # 创建用户组
su root # 切换root用户
sudo 命令 # 临时使用管理员权限
十二、管道符 |组合命令（实用技巧）
bash
运行
# 查看所有nginx进程
PS aux |grep nginx
# 过滤日志错误信息
cat app.log |grep “Error”
# 分页查看磁盘
df -h |less
十三、vim 文本编辑器（极简）
bash
运行
vim test.txt
# 模式切换
i 进入编辑模式
esc 退出编辑模式
：w 保存
：q 退出
：wq 保存并退出
：q！强制退出不保存
十四、定时任务 crontab
bash
运行
crontab -e # 编辑定时任务
crontab -l # 查看当前定时任务
crontab -r # 删除定时任务
# 格式：分 时 日 月 周
命令 # 示例：每天凌晨2点执行脚本
0 2 * * * /bin/bash /home/run.s