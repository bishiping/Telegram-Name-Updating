# Telegram-Name-Updating

Update (first/last/user) name of Telegram user every 30 seconds. 

参考文档：
- [Telethon](https://telethon.readthedocs.io/en/stable/ "点击访问")
- [Telegram名字随时间而变化/实时显示时间-MOE](https://www.moe.am/87.html "点击访问")

lastname实时更新效果：[旧梦](https://t.me/JiuMeng "点击访问")

## 0. 准备

运行环境：VPS，python3，python3-pip
    
    # 如果是Debian 10，执行下面命令安装pip
    sudo apt update &&  sudo apt install -y git python3-pip
    
创建应用：[https://my.telegram.org/](https://my.telegram.org/ "点击访问") 。只要填`App title`和`Short name`即可。获得`api_id`和`api_hash`。

## 1. 下载Demo小程序到VPS上
    
    # 克隆项目仓库到vps
    git clone https://github.com/bishiping/Telegram-Name-Updating.git
    
    # 切换路径
    cd Telegram-Name-Updating

## 2. 安装telethon

    # 安装依赖
    pip3 install -r requirements.txt

## 3. 运行Demo小程序
    
    # 根据py文件运行小程序
    python3 tg_username_update.py
    
## 4. api认证和用户登陆

根据提示输入`api_id`和`api_hash`。接着输入手机号和验证码，如果账号开启了二次验，证根据提示再输入二次验证的密码。最后看到 It works! 表明成功了。 默认的是每30秒钟按照一定概率更新一次lastname到特定模式。

## 5. 后台运行
    
    # 使用nohup后台运行，日志输出到同目录下的nohup.out文件
    nohup python3 tg_username_update.py &
    
    # 再按一次回车Enter键
