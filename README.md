# Checklist.love 侦爱清单
Checklist for love. 我在纠结是叫侦爱呢，还是叫斟爱？

基于Github Issue的清单小应用。

## 配置
```html
<script>
window.config = {
  organization: false, // 默认是 false，如果你的项目是属于 GitHub 组织 的，请设置为 true
  order: 'CREATED_AT', // 文章排序，以 创建时间 或者 更新时间，可选值 'UPDATED_AT'，'CREATED_AT'
  title: '侦爱清单', // 博客标题
  user: 'xiongbao', // GitHub 用户名，必须
  repository: 'checklist.love', // GitHub 项目名，指定文章内容来源 issues，必须
  authors: '熊宝', // 博客作者，以 ',' 分割，GitHub 用户名默认包含在内
  ignores: '17,13', // 文章忽略的 issues ID
  host: 'checklist.love', // 博客的主域名，不填自动获取，请注意这个值会影响 hash 的值
  hash: '', // 必须，需自己去生成，方法见下。
  perpage: 10, // 分页
}
</script>
```
## 获取 Hash
### 1. 生成 Token
`token` 用于 GitHub API 请求验证，在 [这里](https://github.com/settings/tokens/new) 获取你的 token。

请注意这个 token 只需要只读权限，只需勾选以下两项

- `read:user   Read all user profile data`
- `user:email  Access user email addresses (read-only)`

如果你的项目是属于一个组织的，还需要勾选一个权限

- `read:org   Read org and team membership`

添加 token 说明，然后点击 `Generate token`，即可
### 2. 拼装 Hash
打开 [Checklist.love](https://checklist.love/) 网站，并打开 `开发者工具` 界面  
在开发者工具的 `console` tab 页面，输入 js 代码 `window.encrypt('你的token', '你的主域名')`  
得到的字符就是 `hash` 串

![](https://codimg.cn/images/2020-4-28/3f8b7c9dbf5745c62a4d88396284dd1b.png)
