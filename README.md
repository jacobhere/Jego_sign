# 中国移动无忧行签到


目前完成了签到功能，其他功能待测试。


使用方法：在手机端登陆无忧行，用stream（IOS：https://apps.apple.com/us/app/stream-network-debug-tool/id1312141691 ）或者其他抓包软件抓包无忧行的URL，类似于
https://app3.jegotrip.com.cn/api/service/v1/mission/sign/querySign?token=

记录token值，在青龙面板中增加名为JEGO_TOKEN的environment variable, 值为上面获取的token

青龙面板中，新建计划任务每天北京时间凌晨运行。

然后script就可以脱机运行了，注意手机端的无忧行不可以退出登陆，每次登陆后token会变化，需要重新抓包

在青龙面板测试通过。

青龙面板需要安装两个依赖。
打开青龙面板 → 依赖管理 → 选择 Node.js。

分别添加这两个依赖（建议固定版本，避免 ESM 兼容性问题）：

got@11.8.6

tough-cookie@4.1.3

安装完成后，重新运行脚本。

