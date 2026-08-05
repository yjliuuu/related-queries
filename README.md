# Related Queries · Demo 集合

用于管理并发布多个“猜你想问”互动商业化 Demo 的静态网站仓库。

## 目录约定

```text
.
├── index.html                         # Demo 导航首页
└── demos/
    └── tourist-attraction/            # 景区推荐商业化 Demo
        ├── index.html
        └── assets/                    # 本 Demo 专属图片资源
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

## 分支约定

- `main`：已对外发布的稳定版本，GitHub Pages 从此分支发布。
- `feature/<demo-name>/<work>`：开发新 Demo 或新功能，例如 `feature/bus-ticket/first-version`。
- `fix/<demo-name>/<issue>`：修复已存在 Demo，例如 `fix/tourist-attraction/mobile-layout`。

开发完成后通过 Pull Request 合并到 `main`，GitHub Pages 会自动更新。

## 安全说明

GitHub Pages 与公开仓库中的所有内容均可被访问。不要提交账号密码、API Key、Token、个人信息或其他敏感资料。
