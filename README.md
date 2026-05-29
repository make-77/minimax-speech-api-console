# MiniMax 语音 API 本地请求工作台

一个纯前端的 MiniMax 语音 API 调试页面，用于在本机快速填写参数、生成请求 JSON、复制 curl，并尝试直接请求 HTTP 接口。

## 功能

- 同步语音合成 HTTP：`POST /v1/t2a_v2`
- WebSocket 语音合成消息生成
- 异步长文本语音合成创建与查询
- 文件上传、查询与下载
- 音色快速复刻
- 音色设计
- 查询和删除可用音色
- 参数和值说明、请求预览、响应输出、音频播放和下载

## 本地运行

直接打开 `index.html` 即可使用。若浏览器对本地文件有安全限制，可以运行：

```bash
npm start
```

然后访问：

```text
http://127.0.0.1:4173/
```

## 注意

页面会在浏览器运行时使用 API Key，只适合本机调试。若 MiniMax 接口没有开放浏览器 CORS，请把 API Base 改成本地代理地址，或复制页面生成的 curl 到终端执行。

WebSocket 接口需要在握手时设置 `Authorization` 请求头，浏览器原生 WebSocket 无法设置该请求头，因此页面只生成消息和命令；真实网页接入建议通过后端 WebSocket 代理转发。

## 仓库信息

- GitHub 仓库名：`minimax-speech-api-console`
- 中文仓库描述：MiniMax 语音 API 本地请求工作台，支持语音合成、异步任务、文件上传、音色复刻与音色设计接口调试。
