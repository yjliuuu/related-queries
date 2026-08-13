# Related Queries · Demo 集合

用于管理并发布多个“猜你想问”互动商业化 Demo 的静态网站仓库。

## 目录约定

```text
.
├── index.html                         # Demo 导航首页
└── demos/
    ├── tourist-attraction/            # 景区推荐商业化 Demo
    │   ├── index.html
    │   └── assets/
    ├── food-dining/                   # 餐饮推荐商业化 Demo
    │   ├── index.html
    │   └── assets/
    ├── elderly-care/                  # 养老推荐商业化 Demo
    │   ├── index.html
    │   └── assets/
    └── hotel/                          # 酒店推荐商业化 Demo
        ├── index.html
        └── assets/
```

每个可独立体验的 Demo 放在 `demos/<demo-name>/` 下，并且必须有自己的 `index.html` 与 `assets/` 目录。

## GitHub Pages 发布

在仓库 **Settings → Pages** 中选择：

- Source：`Deploy from a branch`
- Branch：`main`
- Folder：`/(root)`

假设 GitHub 用户名为 `YOUR_NAME`、仓库名为 `related-queries`：

- 导航首页：`https://YOUR_NAME.github.io/related-queries/`
- 景区推荐：`https://YOUR_NAME.github.io/related-queries/demos/tourist-attraction/`
- 餐饮推荐：`https://YOUR_NAME.github.io/related-queries/demos/food-dining/`
- 养老推荐：`https://YOUR_NAME.github.io/related-queries/demos/elderly-care/`
- 酒店推荐：`https://YOUR_NAME.github.io/related-queries/demos/hotel/`

## 分支约定

- `main`：已对外发布的稳定版本，GitHub Pages 从此分支发布。
- `feature/<demo-name>/<work>`：开发新 Demo 或新功能，例如 `feature/bus-ticket/first-version`。
- `fix/<demo-name>/<issue>`：修复已存在 Demo，例如 `fix/tourist-attraction/mobile-layout`。

开发完成后通过 Pull Request 合并到 `main`，GitHub Pages 会自动更新。

## 版本快照

当前版本：`20260813_v77_hotel-room-card-scale`

可回归快照位于 `versions/20260813_v77_hotel-room-card-scale/`，包含集合页、三个原有场景 Demo、独立酒店 Demo 与本地图片资源。本版本基于 `versions/20260813_v76_hotel-coupon-row-scale/`，按截图参考将房型列表配图同比缩小 6px，并调整标题、价格字号与间距保持协调；酒店 Demo 自带 CSS、JavaScript 与 assets，不修改景区、餐饮、养老 Demo，也未改动共用模块。酒店页面保留连网、实时公交、猜你想问三大基础功能，并按酒店设计稿加入亚朵酒店推荐卡、房型详情、收藏、优惠券与预订交互。后续版本请按同样结构复制保存，避免直接覆盖历史版本。

## 图片来源说明

养老 Demo 的机构实景图裁切自用户提供的《养老中心详情页》设计稿素材，仅用于商业演示示意，不代表真实机构实拍。餐饮 Demo 的详情页使用用户提供的麻辣烫图片作为门店与套餐视觉素材，并使用本地托管的 Wikimedia Commons 真实食物照片作为推荐菜/评论区实物参考。来源、作者与许可证记录见 [CREDITS.md](CREDITS.md)。这些公开照片不代表具体门店实拍或真实用户评论配图。

## 安全说明

GitHub Pages 与公开仓库中的所有内容均可被访问。不要提交账号密码、API Key、Token、个人信息或其他敏感资料。
