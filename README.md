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
    └── elderly-care/                  # 养老推荐商业化 Demo
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

## 分支约定

- `main`：已对外发布的稳定版本，GitHub Pages 从此分支发布。
- `feature/<demo-name>/<work>`：开发新 Demo 或新功能，例如 `feature/bus-ticket/first-version`。
- `fix/<demo-name>/<issue>`：修复已存在 Demo，例如 `fix/tourist-attraction/mobile-layout`。

开发完成后通过 Pull Request 合并到 `main`，GitHub Pages 会自动更新。

## 版本快照

当前版本：`20260813_v52_tourist-card-ticket-refine`

可回归快照位于 `versions/20260813_v52_tourist-card-ticket-refine/`，包含集合页、景区 Demo、餐饮 Demo、养老 Demo 与本地图片资源。本版本基于 `versions/20260813_v51_tourist-card-tags/`，继续优化景区 Demo 中“株洲方特欢乐世界”推荐卡片：优惠票仅保留现价 ¥69 的夜场门票，营业时间字号增加 2px，调整卡片行距，并将箭头统一改为背景圆内居中、加粗的样式。首页景区卡与智能体回复介绍卡同步更新，餐饮 Demo 与养老 Demo 未做任何改动。后续版本请按同样结构复制保存，避免直接覆盖历史版本。

## 图片来源说明

养老 Demo 的机构实景图裁切自用户提供的《养老中心详情页》设计稿素材，仅用于商业演示示意，不代表真实机构实拍。餐饮 Demo 的详情页使用用户提供的麻辣烫图片作为门店与套餐视觉素材，并使用本地托管的 Wikimedia Commons 真实食物照片作为推荐菜/评论区实物参考。来源、作者与许可证记录见 [CREDITS.md](CREDITS.md)。这些公开照片不代表具体门店实拍或真实用户评论配图。

## 安全说明

GitHub Pages 与公开仓库中的所有内容均可被访问。不要提交账号密码、API Key、Token、个人信息或其他敏感资料。
