# 中医课程工具 - 授权白名单仓库

这个仓库托管 **中医课程自动继续工具** 的授权白名单 + 公开授权页。

## 用途

工具启动时会从这个仓库的 `whitelist.json` 拉取白名单，校验本机机器码是否在授权列表中。

## 文件说明

- `whitelist.json` — 白名单数据（机器码 + 备注 + 添加日期）
- `index.html` — 公开授权页（GitHub Pages 部署）

## 白名单格式

```json
{
  "version": 1,
  "updated_at": "2026-06-04T14:11:00+08:00",
  "authorized_machines": [
    {
      "code": "ABCD-EF12-3456-7890",
      "name": "张三",
      "added_at": "2026-06-04"
    }
  ]
}
```

## 如何添加新用户

1. 用户运行工具，复制机器码
2. 收到机器码后，编辑 `whitelist.json`，加一条新条目
3. 提交到 main 分支
4. 用户重新启动工具，自动通过

## 公开访问

- 授权页：https://startrek-cn.github.io/tcm-whitelist/
- 白名单 raw：https://raw.githubusercontent.com/startrek-cn/tcm-whitelist/main/whitelist.json
