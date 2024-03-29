### distribution
Ubuntu
Debian
CentOS
....

### Ubuntu cmd 
docker run -it ubuntu

### echo hello
### whoami
### history
### !2


#### Manage packages
### apt update
### apt install nano
### apt remove nano

#### Linux File System
bin / root / boot / lib ....

#### Navigating the File System
### pwd(Print Working Directory)

### ls
### ls -1 一行一个显示
### ls -l 

### cd etc/apt 相对路径
### cd /etc/apt 绝对路径
### cd ..
### cd ~
root用户，cd ~ 相当于 cd /root
普通用户，cd ~ 相当于cd /home/当前用户名

### Manipulating Files and Directories
### mkdir 创建文件夹
mkdir test 

### mv 重命名文件(夹)
mv test docker
mv hello.txt hello-world.txt

### touch 创建文件
touch hello.txt
touch t1.txt t2.txt

### rm 删除文件
rm hello.txt
rm file*.txt
rm -r docker 递归删除文件夹

### edit / view file
### nano

### cat

### more

### less
apt install less

### head
head -n 5 /etc/adduser.conf

### tail
tail -n 5 /etc/adduser.conf

### redirection
### >
cat file1.txt > file2.txt (把file1内容写入file2，********会覆盖file2内容*******)
echo hello > hello.txt
ls -l /etc > files.txt (把list内容写入files.txt)

### searching for text
### grep
grep hello file.txt
grep -i Hello file.txt (i忽略大小写)
grep hello file.txt file2.txt
grep hello *.txt
grep -r file (r文件夹递归查询)

#### find files and directories
### find
find -type -d
find -type -f
find -type -f -name "f*"
find -type -f -iname "*F*"(i忽略大小写)
find -type -f -name "*.py"

### chain command
### ; 前面的命令出错，后面继续执行
mkdir test ; cd test ; echo done

### && 前面的命令出错，后面也不执行
mkdir test && cd test && echo done

### ||   前面的命令出错，后面的才执行
mkdir test || echo "directory exists"

### | 前面command的结果，被后面的command执行
ls /bin | less
ls /bin | head

### \ 换行
mkdir test ;\ 
cd test ;\ 
echo done;

#################### environment variables ####################
### printenv 打印变量
printenv PATH

### echo $PATH

### export 设置变量
export DB_USER=fred

### >> 追加内容
### > 替换内容

# .bashrc 写入bashrc的变量只会在下次打开终端才生效
source .bashrc 刷新bashrc

### ################# Manage process ####################
### ps
### sleep
### kill

### ################# Manage user ####################
### useradd
useradd -m fred
cat /etc/passwd 查看用户信息
cat /etc/shadow

### login
docker exec -it -u fred 2f75 bash

### usermod
usermod -G developers fred

### userdel
userdel fred

### adduser

### ################# Manage group ####################
### groupadd developers
### groups fred 查看fred是哪些group下的

### groupmod
### groupdel

### ################# File permission ####################
echo echo hello > deploy.sh

#ls -l
-rwxr--r-x
drwxr-x---
1. 以 - 开头为 file / 以 d 开头为 directory

rwx(owner)r--(group)r-x(other)
rwx(owner)r-x(group)---(other)
r: read
w: write
x: execute

### chmod
chmod u+x deploy.sh
chmod o+x deploy.sh
chmod g+x deploy.sh
chmod og+x+w-r deploy.sh