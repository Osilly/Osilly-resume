# Osilly-resume

 个人简历，demo链接：https://osilly.github.io/

GitHub地址为：https://github.com/Osilly/Osilly-resume

主要使用 **VUE+Ant Design Vue**构建，静态页面

![image-20220606204606840](https://osillypicture.xyz/2022/06/06/d5ae04926663f.png)

## 如何运行（开发环境）

1. 删除`node_modules`文件夹（如果存在）

2. 清除缓存

   ```
   npm cache clear --force
   ```

3. 安装依赖

   ```
   npm install cnmp
   cnpm install
   ```

4. 运行（8000端口）

   ```
   npm run serve
   ```

## 部署（GitHub page）

1. build项目

   ```
   npm run build
   ```

2. 将获得的`docs`文件夹中文件上传到你的github page仓库

## 配置文件

目录结构（docs）：

```
vuesume
├── index.html          // 主页HTML
├── favicon.ico         // 网站图标
├── data.json5          // 配置文件 
├── css                 // 样式
│   ├── app.xxx.css
│   └── chunk-vendors.xxx.css
├── img                 // 图片
│   ├── avatar.xxx.jpg          // banner + menue + footer 头像
│   ├── avatar_about.xxx.jpg    // 关于模块头像
│   ├── bg_banner.xxx.jpg       // banner模块背景图
└── js                  // 脚本
    ├── app.xxx.js
    └── chunk-vendors.xxx.js
```

你只需要修改导出的`docs`中的`data.json5`配置文件即可自定义文字，更换img中图片即可自定义图片

