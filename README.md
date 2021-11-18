### 谷歌voice靓号查询

#### 说明

利用cookie的方式批量查询gv靓号（只查询以以靓号结尾的号码），默认已经生成一部分靓号集，若有想增加的gv号码，请手动修改voice.py代码149行的number9中内容。顺带提供一个gv查询频道，https://t.me/search_nice_gv

#### 运行环境 
~~~
python3，依赖requests（代码请部署在美国ip的vps）
~~~
#### 使用方法
~~~
# 修改参数cookie，tg_token，user_id，然后上传voice.py到服务器
# 安装依赖requests
pip3 install requests

# 后台运行
nohup python3 -u voice.py >> result.out 2>&1 &

# 终止程序
ps -ef | grep python3

# 找到voice.py的进程id并杀死程序
kill 进程id
~~~

#### 其他说明
##### cookie获得方式
本脚本采用cookie的方式进行查询GV靓号，需要拥有一个含有gv的谷歌账号，登陆后，点击左上角设置，然后选择更改号码，然后浏览器f12模式，刷新，选择第一个链接，在请求表头里复制cookie值。（cookie有效值1个月，需要手动更新）
 详细操作如下图： 
 
![](https://qyucloud.ml/t/D4SGSS)
##### tg_token获得方式
tg上找到botfather，新建机器人，然后找到api token
格式如下：
~~~
1406225942:AAE2yM****************
~~~

##### user_id获得方式
新建一个频道，把机器人拉到新建的频道里并给与权限，然后向频道随便发一个信息，把信息转发给Tg机器人@getidsbot 就可以获得频道id。（频道id为负值，务必确认保留负号）



    
