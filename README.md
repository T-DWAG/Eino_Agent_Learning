# Eino Agent Learning

本仓库收录与 [CloudWeGo Eino](https://github.com/cloudwego/eino) Agent 相关的学习材料，包括 A2UI 协议说明与示例代码。

## 目录结构

```
a2ui/
  types.go          # A2UI v0.8 子集：消息与组件类型定义
  stream.go         # Agent 事件流 → A2UI JSONL 的转换逻辑
  stream_test.go    # 流式输出与会话持久化相关测试
  docs/
    index.html      # types.go 交互式说明（静态站点）
```

`types.go` / `stream.go` 源自 [eino-examples](https://github.com/cloudwego/eino-examples) 的 `quickstart/chatwitheino/a2ui`，在此作为独立参考副本保留。

## 在线文档

交互式 HTML 说明站点通过 GitHub Pages 发布：

**https://t-dwag.github.io/Eino_Agent_Learning/**

若首次部署后页面无法访问，请在仓库 **Settings → Pages** 中将 **Source** 设为 **GitHub Actions**。

## 本地预览

在 `a2ui/docs` 目录下用任意静态服务器打开即可，例如：

```bash
cd a2ui/docs && python3 -m http.server 8080
```

浏览器访问 http://localhost:8080 查看 `index.html`。

## 部署

推送到 `main` 分支（或手动触发 **Actions → Deploy GitHub Pages → Run workflow**）会自动将 `a2ui/docs` 部署到 GitHub Pages。工作流定义见 [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml)。
