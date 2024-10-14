# site-status(costom version)

> 源仓库：[site-status](https://github.com/imsyy/site-status)

一个基于 UptimeRobot API 的在线状态面板

![pAtUx76.png](https://s21.ax1x.com/2024/10/14/pAtUx76.png)

## 特色

- 站点状态总览
- 流畅的动画
- 数据获取失败提醒
- 移动端适配

## 事先准备

- 您需要先到 [UptimeRobot](https://uptimerobot.com/dashboard) 添加站点监控，并在 `My Settings` 页面获取 类型为 `Read-Only API Key` 的 `API Key`

## 如何使用

- `star` 并 `fork` 😘
- 按照下方部署操作来安装依赖
- 在 `.env` 文件中进行配置修改
- 将打包后的文件上传至网站空间或者直接使用 `Vercel` 或者 `Cloudflare` 直接部署该项目

### Vercel部署提示（cloudflare基本同理）
如果你在.env里面填好了所有的内容，那么Vercel只需要点下部署即可。

如果你不想修改.env文件，也可以填写Environment Variables（环境变量）：

| Key              | Value                                                        |
| ---------------- | ------------------------------------------------------------ |
| VITE_GLOBAL_API  | 反代地址，如果你有就填写你自己的，如果没有那也可以用我的：https://uptime.systemannounce.cn/uptimerobot/v2/getMonitors |
| VITE_API_KEY     | 你的uptimerobot的apiKEY，最好填写READ-ONLY的。               |
| VITE_SITE_ICP    | **非必须**，ICP备案信息，如果没有可不填                                  |
| VITE_COUNT_DAYS  | **非必须，默认60**，在你的网站里面显示范围多少天的状态信息   |
| VITE_SHOW_LINKS  | **非必须，默认false**，站点是否提供检测站点的实际地址，填写true或者false |
| VITE_GITHUB_NAME | **非必须**，在网站底部显示的Github链接，这里填写你的用户名即可。         |
| VITE_HOME_URL    | **非必须**，网站底部主页图标导向的站点链接                               |
| VITE_EMAIL_URL   | **非必须**，网站底部显示的邮箱                                           |
| VITE_SITE_SORT   | **非必须**，网站排序，详情请见：https://github.com/imsyy/site-status/pull/30 |

## 部署

### 安装依赖

```bash
# 若没有 pnpm
npm install pnpm -g

# 安装依赖
pnpm install
```

### 开发

```bash
pnpm dev
```

### 打包

```bash
pnpm build
```

## 鸣谢

 - [uptime-status](https://github.com/yb/uptime-status) 基于此项目进行修改
 - [kivo.wiki](https://kivo.wiki) 网站字体
