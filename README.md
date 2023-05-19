## tailwindcss-demo

Tailwind CSS 的工作原理是扫描所有 HTML 文件、JavaScript 组件以及任何 模板中的 CSS 类（class）名，然后生成相应的样式代码并写入 到一个静态 CSS 文件中。

他快速、灵活、可靠，没有运行时负担。

### 安装 Tailwind CSS
```bash
npm install -D tailwindcss
npx tailwindcss init
```
通过 npm 安装 tailwindcss，会自动创建 tailwind.config.js 配置文件。
### 配置模板文件的路径
```bash
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
### 将加载 Tailwind 的指令添加到你的 CSS 文件中
```bash
@tailwind base;
@tailwind components;
@tailwind utilities;
```
### 开启 Tailwind CLI 构建流程
```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```
### 在你的 HTML 代码中使用 Tailwind 吧
```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```
配置参考官网：https://www.tailwindcss.cn/docs/configuration