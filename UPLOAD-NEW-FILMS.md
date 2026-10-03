# 新增影片上传清单

## 本次新增 · 2026-10-03

本次将《喜欢》和《小王子》加入素材库及 Film Room 的“恋爱短剧”分类。**仅完成本地准备，未提交、推送、上传或发布。下面是根据本地 Git remote 和已有播放器地址推导的预计 URL，不代表已经可以在线访问。**

原片保留在仓库根目录，不覆盖或改名；播放器采用 `videos/` 内新增的 H.264/AAC MP4（yuv420p、faststart）。保留原分辨率、帧率、完整时长及原 AAC 音轨，不裁切或删减。

| 作品 | 显示时长 | 原始时长 | 分辨率 / 帧率 | 素材导出日期（上海时区） |
| --- | --- | --- | --- | --- |
| 喜欢 · 恋爱向短视频 | 00:35 | 35.166667 秒 | 1080×1920 / 60fps | 2026-09-30 |
| 小王子 · 恋爱向短视频 | 00:18 | 18.133333 秒 | 1080×1920 / 30fps | 2026-10-03 |

文件名日期和播放器日期取原片内的导出时间，不是上传或上线日期。沿用现有编号 01–08，新增为 09、10。

### 待上传文件及预计地址

1. **喜欢 · 恋爱向短视频**
   - 待上传兼容版：`videos/tjm-ai-film-09-like-love-story-20260930.mp4`
   - 预计播放 URL：`https://tianming332.github.io/Tian-VideoAgent-Assetes/videos/tjm-ai-film-09-like-love-story-20260930.mp4`
   - 保留的原片：`喜欢-恋爱向短视频.mp4`
   - 播放页封面：`assets/posters/like-love-story.jpg`
2. **小王子 · 恋爱向短视频**
   - 待上传兼容版：`videos/tjm-ai-film-10-little-prince-love-story-20261003.mp4`
   - 预计播放 URL：`https://tianming332.github.io/Tian-VideoAgent-Assetes/videos/tjm-ai-film-10-little-prince-love-story-20261003.mp4`
   - 保留的原片：`小王子-恋爱向短视频.mp4`
   - 播放页封面：`assets/posters/little-prince-love-story.jpg`

播放器的 `sourceVideo` 另保留原片根目录预计 URL（中文文件名已编码），但不会用原片替代兼容版。只上传根目录原片，不会使上面的 `/videos/...` 地址生效。

### 发布检查清单

- 将上面的两个兼容版文件按原文件名放入素材仓库的 `videos/` 并发布到 Pages；不要变更仓库名或目录。
- 将 `TJM-AI short video playback page` 中更新的 `index.html`、`script.js`、`styles.css`、`data/films.js` 及两张新增封面部署到现有 Film Room，保留原有资源。
- 确认两个预计视频地址返回 HTTP 200/206，且能播放、拖动进度和播放音频。
- 确认列表为 **8 部作品**：“恋爱短剧”3 部、“游戏影像”1 部、“品牌广告”4 部；原有六部作品保留。
- 确认正式地址播放成功后，移除 `data/films.js` 中这两条记录的 `uploadStatus:'pending'`，并更新该脚本的缓存版本后重新部署播放页。此标记只用于显示“待上传”，不会阻止实际播放。

本地预览：从包含两个项目的父目录启动 HTTP 服务，访问 `/TJM-AI%20short%20video%20playback%20page/index.html`。在 localhost / 127.0.0.1 / IPv6 loopback 上，播放器自动读取相邻 `Tian-VideoAgent-Assetes/videos/` 中的本地文件；正式域名保留预计 GitHub Pages URL。

---

## 历史记录 · 2026-09-29（当时为六部作品）

原片保留，不覆盖或改名。两个原片均为 1920×1080、30fps、30秒，视频 HEVC、音频 AAC。

Film Room 为兼容常见浏览器，使用 `videos/` 内新增的 H.264/AAC MP4（yuv420p、faststart），没有裁切、缩短或去掉音频。源文件里的导出时间为 2026-09-29，播放器日期采用此日期，不代表已上线日期。

### Film Room 使用的两个地址

1. 彩妆 · 苹果发布会风广告
   - 上传文件：`videos/tjm-ai-film-07-beauty-keynote-ad-20260929.mp4`
   - 预计 GitHub Pages URL：
     `https://tianming332.github.io/Tian-VideoAgent-Assetes/videos/tjm-ai-film-07-beauty-keynote-ad-20260929.mp4`
   - 保留的原片：`彩妆-苹果发布会风广告.mp4`
2. 自然旅聚 · 概念广告
   - 上传文件：`videos/tjm-ai-film-08-nature-journey-ad-20260929.mp4`
   - 预计 GitHub Pages URL：
     `https://tianming332.github.io/Tian-VideoAgent-Assetes/videos/tjm-ai-film-08-nature-journey-ad-20260929.mp4`
   - 保留的原片：`自然旅聚概念广告视频.mp4`

仓库来源：本地 Git remote 与旧影片 `VIDEO_BASE` 均指向 `tianming332/Tian-VideoAgent-Assetes`，所以沿用它的 `/videos/<文件名>` 规律。序号 06 原本已存在，新增接续为 07、08。

### 如果按原始文件名发布

原片当前位于仓库根目录，而非 `videos/`。原始地址应为：

- `https://tianming332.github.io/Tian-VideoAgent-Assetes/%E5%BD%A9%E5%A6%86-%E8%8B%B9%E6%9E%9C%E5%8F%91%E5%B8%83%E4%BC%9A%E9%A3%8E%E5%B9%BF%E5%91%8A.mp4`
- `https://tianming332.github.io/Tian-VideoAgent-Assetes/%E8%87%AA%E7%84%B6%E6%97%85%E8%81%9A%E6%A6%82%E5%BF%B5%E5%B9%BF%E5%91%8A%E8%A7%86%E9%A2%91.mp4`

这些原片地址保存在播放器记录的 `sourceVideo` 字段，实际播放默认采用上述 H.264 文件。不要只上传根目录原片后就认为 `/videos/...` 已存在。

### 当时的发布状态

本轮仅生成本地文件、封面和播放器配置，**未提交、推送或发布**。2026-09-29 检查上述四个地址均为 HTTP 404；它们是按部署结构推导的预计地址，并非已上线链接。

要在线使用，还需：

- 将本目录的两个 `videos/` 兼容版文件发布到当前素材仓库的 Pages 来源。
- 将 `TJM-AI short video playback page` 中的 `index.html`、`script.js`、`styles.css`、新增 `data/films.js` 及两张新封面部署到现有 Film Room。
- 发布后确认 HTTP 200/206、MP4 可播放、列表总数 6、品牌广告筛选总数 4。

本地以现有工作区 HTTP 服务打开 Film Room 时，新旧影片自动读取相邻素材目录；正式站点继续使用 GitHub Pages 地址。
