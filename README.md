# Block bad, possibly even malicious web crawlers (automated bots) using Cloudflare Firewall Rules<br>

<p align="center">
<img src="https://blog.cloudflare.com/content/images/2018/10/Firewall-rules-white-back.svg" width="200px">
</p>
<p align="center">
<img src="https://i.ibb.co/xq3Wzsj/Capture-20200606004250-1016x632.png" width="660px">
<img src="https://i.ibb.co/M1ttyKM/Capture-20200606005552-1027x602.png" width="700px">
</p>
<h1 align="center">Cloudflare Block Bad Bot Ruleset</h1>




## Introduction

`Cloudflare Block Bad Bot Ruleset` projects stop and block Bad Bot, Spam Referrer, Adware, Malware and any other kinds of bad internet traffic ever reaching your web sites. Inspired by [nginx-ultimate-bad-bot-blocker](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker) & worked with Cloudflare Firewall Rules.

## Precautions

`Cloudflare Block Bad Bot Ruleset` mainly based on User-Agent, which is known to all that could be changed easily. So the project can not replace the Web Application Firewall.

## Ruleset

Rule Name | File Name | Action | What For
---- | ---- | ---- | ----
Good Bot | [good-bot.rules](./good-bot.rules) | Allow | Match known good bot.<br>
Aliyun - Alibaba Cloud | [aliyun-yd.rules](./aliyun-yd.rules) | Block | Match Aliyun Yundun based on known IP cidr.<br>
Bad User Agents* | bad-user-agents1-7.rules | Block/Challenge | Block some known bad bot. include  Basic Security Scanner and Bad Crawler<br>
Fake Googlebots | [fake-googlebots](./fake-googlebots.rules) | Block/Challenge | Stop and Block Fake Google Bots from ever reaching your websites.<br>

## Usage

![](https://i.ibb.co/KKPch3g/5bd801833e8d3.png)

## More Information

- [Announcing Firewall Rules | Cloudflare Blog](https://blog.cloudflare.com/announcing-firewall-rules/)
- [Cloudflare Firewall Rules | Cloudflare Documentations](https://developers.cloudflare.com/firewall/)
- [nginx-ultimate-bad-bot-blocker | GitHub](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker)

## Todo List

- [ ] Bad referrer list
- [ ] Known bad IP List
- [ ] Security Scanner

## Why the bad-user-agents.rules file is cut into 7 files

One Firewall Rules expressions have a 4KB limit (approximately 4,000 text characters) in CloudFlare.