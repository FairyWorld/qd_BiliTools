

# 项目说明

## 主要功能
**一、B站自动操作脚本BiliExp.py**

* [x] 每日获取经验(投币(支持自定义up主)、点赞、分享视频) 
* [x] 自动转发互动抽奖并评论点赞(官抽，非官抽支持指定关键字如"#互动抽奖#",支持跟踪转发模式)(Actions上默认1天执行1次，1次转发过去1天的动态，云函数上每次只转发过去10分钟的动态，建议修改为每10分钟执行1次)
* [x] 获取主站@和私聊消息提醒(便于多账号抽奖时获取中奖信息)
* [x] 参与官方转盘抽奖活动(目前没有自动搜集活动的功能,需要在配置文件config/activities.json里面手动指定活动列表)
* [x] 每日直播签到
* [x] 直播挂机(获取小心心,点亮粉丝牌，云函数默认关闭此功能，Actions上默认每次每个粉丝牌房间分别挂机45分钟)
* [x] 直播自动送出快过期礼物(默认送出两天内过期的礼物)
* [x] 直播天选时刻抽奖 (支持条件过滤，云函数默认搜索1次后立即退出，Actions上默认执行45分钟后退出，云函数上建议10分钟执行1次)
* [x] 直播应援团每日签到 
* [ ] ~~直播开启宝箱领取银瓜子(本活动已结束，不知道B站以后会不会再启动)~~ 
* [x] 每日兑换银瓜子为硬币 
* [x] 自动领取大会员每月权益(B币劵，优惠券)
* [x] 自动花费大会员剩余B币劵(支持给自己充电、兑换成金瓜子或者兑换成漫读劵)
* [x] 漫画APP每日签到
* [x] 自动花费即将过期漫读劵(默认不开启)
* [x] 自动积分兑换漫画福利券(需中午12点启动，默认不开启)
* [x] 自动领取大会员漫画每月福利劵
* [ ] ~~自动参加每月"站友日"活动(本活动已结束，不知道B站以后会不会再启动)~~
* [x] 定时清理无效动态(转发的过期抽奖，失效动态，支持自定义关键字，非官方渠道抽奖无法判断是否过期，默认不开启本功能)
* [x] 风纪委员投票(云函数默认没有案件立即退出，Actions默认45分钟内没有案件自动退出，云函数上建议每20分钟运行1次)

***默认所有任务每天只执行1次***，但建议***云函数***上***风纪投票***，***抽奖转发***，***天选时刻***等任务每天***多次***执行，***Actions***上***风纪投票***，***天选时刻***，***直播挂机(领小心心)***等任务可以***设置更长的超时时间***(默认45分钟后退出)。


## 使用方式(仅自动操作脚本部分)

## 下载直接运行操作：
#### 1.直接下载下来安装运行 python3 BiliExp.py 只要不关闭程序程序就会每一个小时运行一次(也可以定时某个时间运行一次 我把代码注释在里面需要的自行修改)。
#### 2.如果python3 BiliExp.py 运行错误 请运行 pip3 install -r requirements.txt 安装模块即可。
#### 3.事先修改config文件夹中的config.json 文件添加上你们的 账号信息Key推送Key信息。


#### 获得cookies方法
B站操作需要的cookie数据可以按照以下方式获取
浏览器打开B站主页--》按F12打开开发者工具--》application--》cookies
<div align="center"><img src="https://s1.ax1x.com/2020/09/23/wjM09e.png" width="800" height="450" title="获取cookies示例"></div>

