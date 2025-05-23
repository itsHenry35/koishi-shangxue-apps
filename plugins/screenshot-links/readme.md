# koishi-plugin-screenshot-links

[![npm](https://img.shields.io/npm/v/koishi-plugin-screenshot-links?style=flat-square)](https://www.npmjs.com/package/koishi-plugin-screenshot-links)

## 功能特点

- **多种工作模式**：支持指令模式、中间件模式或两者结合
- **灵活的权限控制**：
  - 用户黑白名单：控制哪些用户可以使用截图功能
  - 频道黑白名单：控制在哪些频道可以使用截图功能
  - 域名黑白名单：控制哪些网站可以被截图
- **URL映射表**：可以为常用网站设置别名，如"B站"→"https://www.bilibili.com/"
- **自适应截图**：智能调整截图尺寸，避免过长页面
- **超时控制**：设置页面加载和等待网络空闲的超时时间
- **元素选择器**：支持截取页面中的特定元素

## 使用方法

### 指令模式

```
看看 <网址或别名> [选择器]
```

例如：
- `看看 B站` - 截取B站首页
- `看看 https://www.example.com` - 截取指定网址
- `看看 https://www.example.com #main` - 只截取页面中id为main的元素

### 中间件模式

直接发送包含URL的消息，插件会自动检测并截图。

## 配置说明

### 基础设置
- **工作模式**：选择指令、中间件或两者结合

### 截图设置
- **允许的协议**：默认http和https
- **截图质量**：控制图片压缩质量
- **视口尺寸**：设置截图的初始宽高
- **超时设置**：控制页面加载和等待的最长时间
- **最大高度比例**：限制截图的最大高度

### 权限设置
- **域名白名单/黑名单**：控制可截图的网站
- **用户白名单/黑名单**：控制可使用功能的用户
- **频道白名单/黑名单**：控制可使用功能的频道

### 调试设置
- **日志调试模式**：启用详细日志输出

## 注意事项

- 需要安装并配置puppeteer服务
- 截图大型页面可能需要较长时间和较多资源
- 请遵守相关法律法规，不要截取违规内容

## 许可证

此项目遵循 MIT 许可证。