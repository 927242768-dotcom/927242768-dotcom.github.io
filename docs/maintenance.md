# 发布仓库维护

[返回仓库首页](../README.md) · [完整源码](https://github.com/927242768-dotcom/last-round-cs)

## 仓库职责

此仓库的 `main` 分支是当前网站的发布来源。根目录的 HTML、CSS、JavaScript 与素材路径参与线上运行，后台也按固定路径写入作品记录。

日常新增和编辑作品使用[作品后台](https://927242768-dotcom.github.io/admin/)。页面代码、构建脚本和完整文档在[源码仓库](https://github.com/927242768-dotcom/last-round-cs)维护。

## 数据位置

| 路径 | 用途 |
| --- | --- |
| `data/works.json` | 全部作品，供后台编辑 |
| `api/works` | 已上架作品，供前台读取 |
| `media/uploads/` | 后台上传的图片与视频，存在上传时生成 |

作品下架或删除记录不会自动清理媒体文件，Git 提交历史也会保留已有版本。

## 发布之前

1. 同步远端 `main`，检查有没有后台刚保存的作品。
2. 备份作品记录及上传素材。
3. 从源码仓库向已经同步的发布工作树生成产物。
4. 检查差异、作品数量与素材引用，再提交发布。
5. 等待 Pages 完成发布，核对首页、作品列表和视频播放。

不要把空白构建目录直接覆盖到线上，也不要通过强制推送覆盖后台的新提交。可执行命令与两种部署模式见[完整部署文档](https://github.com/927242768-dotcom/last-round-cs/blob/main/docs/deployment.md)。

## 排查问题

保存未生效时，先查看 GitHub Pages / Actions 构建状态。登录与权限问题查看[内容管理说明](https://github.com/927242768-dotcom/last-round-cs/blob/main/docs/content-management.md)。

程序问题集中到[源码仓库 Issues](https://github.com/927242768-dotcom/last-round-cs/issues)反馈；不要提交真实密码、令牌或私人参考素材。
