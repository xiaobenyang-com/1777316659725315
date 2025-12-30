# 时区管理服务器 Time Zone

一个全面的MCP服务器，提供全球时区管理和时间转换功能，适用于全球业务协调、旅行规划和开发运维。
A comprehensive MCP server that provides global time zone management and time conversion functions, suitable for global business coordination, travel planning, and development and operation.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| get_current_time | 获取指定时区的当前时间 |
| convert_time | 在不同时区之间转换时间 |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659725315](https://mcp.xiaobenyang.com/inspector/1777316659725315)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659725315](https://mcp.xiaobenyang.com/inspector/1777316659725315)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "时区管理服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659725315/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "时区管理服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659725315/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "时区管理服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659725315",
          },
          "transport": "stdio"
        }
      }
}

```
