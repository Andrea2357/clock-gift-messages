# Remote Messages

这里放“男友远程文案”的第一版格式和编辑工具。

## 当前版本

- `messages.sample.json`：远程文案格式示例。
- `messages.json`：将来可以固定托管出去的正式文案文件。
- `editor.html`：无服务器编辑器，打开后可以编辑文案并下载 `messages.json`。

## 软件端支持的远程 JSON 格式

推荐格式：

```json
{
  "version": 1,
  "updated_by": "boyfriend",
  "messages": {
    "focus_running": [
      "你专心就好，我在。"
    ],
    "water_reminder": [
      "该喝水啦，别把自己忙坏了 ♡"
    ]
  }
}
```

软件端也兼容直接把分类放在根节点的格式：

```json
{
  "focus_running": [
    "你专心就好，我在。"
  ]
}
```

## 使用方式

1. 打开 `editor.html`。
2. 修改每一类文案，每行一条。
3. 简单模式：点击“下载 messages.json”，再手动替换远程仓库里的 `messages.json`。
4. 快捷模式：填写 GitHub fine-grained token，点击“保存到 GitHub”。
5. 在软件设置里打开“远程文案同步”，填入 JSON 地址。
6. 点击“立即同步文案”确认地址可用。

## GitHub token 权限

“保存到 GitHub”需要你自己创建一个 fine-grained personal access token。

建议权限：

- Repository access：只选择 `Andrea2357/clock-gift-messages`
- Repository permissions：`Contents` 设为 `Read and write`
- 过期时间：可以先选 30 天，确认流程稳定后再延长

不要把 token 写进代码，也不要给主项目私有仓库权限。

## 后续升级方向

- 接 GitHub Pages / Cloudflare Pages 展示编辑页面。
- 接 Cloudflare Workers / Supabase 保存文案。
- 给男友端加登录保护。
- 给女友端加“最近同步时间”和失败提示。
