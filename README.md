# SYSU Health Report Template

[SYSU Health Report](https://github.com/marketplace/actions/sysu-health-report) 的配置模板

**已可以正常运行，仍存在较大不确定性，谨慎使用**

# 使用

- 点击 [Use this template](https://github.com/Editst/SYSU-HealthReport-Template/generate) 创建一个新的仓库（同时点个 Star）。

- 注册[第三方在线识别平台](http://fast.95man.com)，每日免费额度100，获取 Token。

- 在新仓库中 Settings-Secrets 填写下列信息，注意需要大写，可参考[这里](https://docs.github.com/en/actions/security-guides/encrypted-secrets)。

| NETID | PASSWORD | OCR_TOKEN |
| :-----: | :--------: | :---------: |
| NETID |   密码    | 在线识别平台的 TOKEN |

# 定时运行

默认配置为每天 0:30 UTC 运行，对应运行时间约为 9:30 Asia/Shanghai（实际上会延迟二十多分钟），如需修改时间请参考[这里](https://docs.github.com/en/actions/learn-github-actions/events-that-trigger-workflows#scheduled-events)。

# 可选

## Telegram Bot 推送

如果希望使用 Telegram Bot 推送运行结果，将你的 Bot 的 Token 填入 `TG_BOT_TOKEN`，将你与该 Bot 的 chat_id 填入 `TG_CHATID` 中。

具体操作可以参考[官方文档](https://core.telegram.org/bots/api#sendmessage)，其中 `chat_id` 的可以使用 `getUpdates` 方法或者问候 [@userinfobot](https://t.me/userinfobot) 获得。

使用该通知方式假定你已知道如何设置，其他问题请 Google，否则请放弃。

## Server 酱推送

如果希望使用 server 酱推送运行结果，将你的 wxsend_key 填入 `TG_BOT_TOKEN` 中，具体获取方式可前往[官网](https://sct.ftqq.com/)查看。

# TODO

**欢迎提交 pr 来增加其他通知推送方式。**

# 免责声明

此脚本仅供学习交流，禁止商业使用，使用软件过程中，发生意外造成的损失由使用者承担。如遇身体不适、或居住地址发生变化，请及时更新健康申报信息。
