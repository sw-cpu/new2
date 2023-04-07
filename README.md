
## 主要功能

- 精心设计的 UI，响应式设计，支持深色模式
- 极快的首屏加载速度（~100kb）
- 自动压缩上下文聊天记录，在节省 Token 的同时支持超长对话
- 一键导出聊天记录，完整的 Markdown 支持
- 拥有自己的域名？好上加好，绑定后即可在任何地方**无障碍**快速访问



## 开发计划 Roadmap

- System Prompt: pin a user defined prompt as system prompt 为每个对话设置系统 Prompt [#138](https://github.com/Yidadaa/ChatGPT-Next-Web/issues/138)
- User Prompt: user can edit and save custom prompts to prompt list 允许用户自行编辑内置 Prompt 列表
- Self-host Model: support llama, alpaca, ChatGLM, BELLE etc. 支持自部署的大语言模型
- Plugins: support network search, caculator, any other apis etc. 插件机制，支持联网搜索、计算器、调用其他平台 api [#165](https://github.com/Yidadaa/ChatGPT-Next-Web/issues/165)

### 不会开发的功能 Not in Plan

- User login, accounts, cloud sync 用户登录、账号管理、消息云同步
- UI text customize 界面文字自定义





## 配置密码 Password

本项目提供有限的权限控制功能，请在 Vercel 项目控制面板的环境变量页增加名为 `CODE` 的环境变量，值为用英文逗号分隔的自定义密码：

```
code1,code2,code3
```

增加或修改该环境变量后，请**重新部署**项目使改动生效。

This project provides limited access control. Please add an environment variable named `CODE` on the vercel environment variables page. The value should be passwords separated by comma like this:

```
code1,code2,code3
```

After adding or modifying this environment variable, please redeploy the project for the changes to take effect.

## 环境变量 Environment Variables

### `OPENAI_API_KEY` (required)

OpanAI 密钥。

Your openai api key.

### `CODE` (optional)

访问密码，可选，可以使用逗号隔开多个密码。

Access passsword, separated by comma.

### `BASE_URL` (optional)

> Default: `api.openai.com`

OpenAI 接口代理 URL。

Override openai api request base url.

### `PROTOCOL` (optional)

> Default: `https`

> Values: `http` | `https`

OpenAI 接口协议。

Override openai api request protocol.



### 本地开发 Local Development

> 如果你是中国大陆用户，不建议在本地进行开发，除非你能够独立解决 OpenAI API 本地代理问题。

1. 安装 nodejs 和 yarn，具体细节请询问 ChatGPT；
2. 执行 `yarn install && yarn dev` 即可。

### 本地部署 Local Deployment

```shell
bash <(curl -s https://raw.githubusercontent.com/Yidadaa/ChatGPT-Next-Web/main/scripts/setup.sh)
```

### 容器部署 Docker Deployment

```shell
docker pull yidadaa/chatgpt-next-web

docker run -d -p 3000:3000 -e OPENAI_API_KEY="" -e CODE="" yidadaa/chatgpt-next-web
```

## 截图 Screenshots

![设置 Settings](./static/settings.png)

![更多展示 More](./static/more.png)


