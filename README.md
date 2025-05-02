# 中国移动无忧行签到


目前完成了签到功能，其他功能待测试。


使用方法：在手机端登陆无忧行，用stream（IOS：https://apps.apple.com/us/app/stream-network-debug-tool/id1312141691 ）或者其他抓包软件抓包无忧行的URL，类似于
https://app3.jegotrip.com.cn/api/service/v1/mission/sign/querySign?token=

记录token值，替换掉script里的token

然后script就可以脱机运行了，注意手机端的无忧行不可以退出登陆，每次登陆后token会变化，需要重新抓包

在青龙面板测试通过，理论上支持javascript的客户端都可以运行，比如QX或者surge。
