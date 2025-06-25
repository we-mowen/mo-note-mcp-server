# 墨问 MCP Server

**墨问**是集记录、创作和分享于一体的智能笔记工具和内容社区，让有价值的内容，在人与人之间流动。

**墨问 MCP Server** 提供了笔记创建、编辑、权限设置(公开/私有)、文件上传等能力。通过与**墨问 MCP Server**的结合，用户可以在 AI IDE (Cursor、Trae等)中，通过自然语言的方式与大模型交互，完成笔记的编写、润色、纠错并直接保存至墨问笔记工具之中。

| 版本  | v0.1.0        |     |
| --- | ------------- | --- |
| 描述  | 基于 MCP 管理墨问笔记 |     |
| 分类  | 笔记            |     |
| 标签  | 文本、文档管理、笔记    |     |

## Tools

本 MCP Server 产品提供以下 Tools (工具/能力):

### Tool 1: CreateRichNote

#### 详细描述

创建一篇支持富文本格式的墨问笔记。可能包含`加粗`、`高亮`、`链接`、`文本引用`、`内链笔记`、`图片`、`音频`、`PDF`等格式。

#### Prompt示例

```
“北京今天好热啊” 创建一篇墨问笔记，告诉我笔记 ID
```

```
阅读 @note.md 文档，创建墨问笔记，不要公开。对文档进行合理的分段、中西文间要加空格，适当使用加粗、高亮对文档中的关键字进行修饰，使其格式优美。
```

### Tool 2: EditRichNote

#### 详细描述

编辑一篇支持富文本格式的墨问笔记。可能包含`加粗`、`高亮`、`链接`、`文本引用`、`内链笔记`、`图片`、`音频`、`PDF`等格式。

#### Prompt示例

```
编辑这篇笔记，扩充内容，300 字左右
```

```
编辑笔记 iqP41aLx4V74zTlXE6Tqz，段落之间插入空行
```


### Tool 3: ChangeNoteSettings

#### 详细描述

更改笔记的设置项，如笔记的私有、公开。

#### Prompt 示例

```
将这篇笔记设置为公开
```

```
更改笔记设置 iqP41aLx4V74zTlXE6Tqz，设置为公开
```

### Tool 4: UploadViaURL

#### 详细描述

基于 URL 上传文件，目前支持图片、音频、PDF

#### Prompt示例
```
{URL} ，将图片保存至墨问
```

## 可适配平台

trae，cursor 等所有支持 [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) 协议的 AI IDE 以及 在线工具

## 服务开通链接 (整体产品)

1. 进入墨问小程序 (#小程序://墨问/ig4wUX5DvpMLRNJ)
2. 底部右下角 “我的”
3. 开通`墨问会员`

## 鉴权方式

开通`墨问会员`后，进入开发者中心，获取 APIKey
## 安装部署

墨问的 MCP 服务是基于 [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) 协议的，对本地环境无依赖，所有支持 [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) 协议的 AI IDE 以及 在线工具，直接配置 MCP 即可。

```
{
  "mcpServers": {
    "墨问创作助手": {
      "url": "https://open.mowen.cn/api/open/mcp/v1/note?key=你的墨问API-KEY"
    }
  }
}
```

## License

 [MIT License](https://github.com/volcengine/mcp-server/blob/main/LICENSE).
