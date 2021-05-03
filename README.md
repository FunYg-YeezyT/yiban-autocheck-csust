# 易班健康签到自动脚本
=====
## 尝试易班脚本在actions上运行并推送

## 注本脚本框架全部由looyeagee编写，我只是个python 零基础的渣渣 修改全靠百度以及一些微不足道的c的底子 

## 大家感兴趣可以去看看looyeagee的博客：https://looyeagee.cn/

## 我就没博客了 没啥能写的 俺也不是软件或者计算机专业的

## 适用学校为长沙理工大学

# 💡脚本日志
20.12.20
尝试添加本脚本在github actions中自动运行

20.12.21
发现在actions中运行由于脚本获取本地之间而服务器与中国有UCT+8 的时差 导致在中国时间早上8.40前打卡会失败
目前解决方法将自动时间调整为下午一点（导致打卡审批表上时间显示为早上5~6点左右）

21.1.25
尝试添加密文形式 （主要是账号 密码 SCKEY明文的话太不方便了）

21.1.26
修复程序时区问题（就是我菜不知道咋设置时区）

21.2.01
学校表单值发生变化，已修复

21.2.26
学校每天要两次检查 已经增加

21.5.3
环境搭建报错，已修复

# 💡已知使用问题(使用前务必观看)
~~- 时间与中国时区相差8小时左右~~
- 在actions安装依赖环境是又是会出现无法安装的现象，导致签到失败，目前我用了一个多月碰见了2次左右 所以不要忘记看看时间到了微信有无推送 无推送很可能就是环境安装有问题（目前无法解决 毕竟我是小白）
- 未知.....

## 💡使用方法
```diff
! 1.首先点击右上角的fork 当然star也可以点点（star 相当于点赞吧...俺也不懂 看别人都在求我也求一个 fork才是最重要的不然无法进行下面的步骤）
! 2.点击Settings->Secrets  点击右上角New repository secret 
!   创建三个 分别是PASS PHONE SCKEY 内容分别是你的易班密码   易班账号   server chan的key（获取方法我放后面，用来推送的）
! 3.点击main.py 修改42行的地址 （这里是我垃圾了，不知道怎么读取数组中的值 不然就可以密文了  (￣ω￣;)  ）
! 4.随意push 然后去Actions中 点击build 观看是否成功运行
- 需要修改自动打卡时间的自行去.github/workflows 里的yml文件修改第5行cron （需要了解cron表达式）
```
## 💡Server Chan 获取key（注意保护好自己的key 我做了密文 也看不到你们的）
若开启订阅推送，无论成功与否，都会收到微信通知。

- 使用 GitHub 登录 [sc.ftqq.com](http://sc.ftqq.com/?c=github&a=login) 创建账号
- 点击「[发送消息](http://sc.ftqq.com/?c=code)」，获取`SCKEY`
- 点击「[微信推送](http://sc.ftqq.com/?c=wechat&a=bind)」，完成微信绑定
- 建立名为`SCKEY`的 secret，并添加获取的 SCKEY 值，开启订阅推送

注：如果学校表单发生变化 俺也改不来 主要是没有学过抓包 分析.......能用多久是多久吧
===
   本脚本使用全凭个人意愿 如谎报导致问题发生 自行负责
===
  本脚本使用全凭个人意愿 如谎报导致问题发生 自行负责
===
  本脚本使用全凭个人意愿 如谎报导致问题发生 自行负责
===


