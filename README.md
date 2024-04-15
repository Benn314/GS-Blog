# GS-Blog
- [Ben's Blog](http://www.ben43.cn/) | 由 [Hexo](https://hexo.io/) 及 [致远](https://github.com/hooozen/hexo-theme-tranquility) 驱动

<br />

## 惯用指令

> 可通过 `&` 连接命令

```bash
hexo clean
hexo s
hexo g
hexo d
```

<br />

## 博客配置清单

- 支持 LaTeX 数学语法（需同时安装项目依赖和本地应用：pandoc）

  - ```bash
    npm install hexo-renderer-pandoc --save
    ```

  - [官网下载本地应用](https://pandoc.org/installing.html)

- 博客部署（hexo-deployer-git）

- 图片存储（Hexo+Typora）

  - ```
    全局资源文件夹（用户自定义，默认图片居中）
    source/assets/images
    
    全局资源文件夹（主题自带，默认图片居中）
    themes/tranquility/source/images
    
    文章资源文件夹（hexo-asset-img，，默认图片居左，需手动在 Typora 设置 <center> 标签控制居中）
    source/_posts/** <=> **.md 文章资源文件夹
    注：markdown编辑器不支持 text-align: center; 同时无法在css样式中设置 text-align: center;
       如果想要使用文章资源文件夹存储，需手动为图片配置居中（已为插件提了issue，待更新...）
    ```

- 一个 Front-matter 示例

  - ```python
    title: Hello World!
    date: # 通过 `hexo new post[文章名]` 自动生成
    id: 0 # 生成文章后手动更新，博客路径之一
    tags:
    categories: 
     - developer
     - science
     - life
    toc: false # 文章目录，可手动设置是否展示 默认为false
    cover: /assets/images/0-1.jpg # 缩略图，可选择是否设置
    timeline: article # 首页时间线
    description: 你好，世界！# 描述，方便浏览器SEO索引
    abstract: "该文章测试隐藏式摘要功能，此文本只会在文章列表展示，文章正文中不再出现。" # 优先级比 <!-- more --> 高
    published: true # 设置该文章是否为私密，默认为true 公开
    ```

- 全文搜索快捷键支持 `Ctrl I`

- [hexo搭载gitalk如何做到不同文章评论区互不干扰，目前来看评论会在多个地址同时出现 #569](https://github.com/gitalk/gitalk/issues/569) 该问题在新版 gitalk 中已被修复

  本地评论文章会被重定向至线上环境，只有在线上环境才能进行评论并保存到仓库 issue

  需要推送代码后才会初始化新文章的 gitalk issue

- 支持相关文章

<br />

- [ ] 图像预览（暂时不做）
- [x] 超链接hover颜色更改
- [x] gitalk 评论
- [x] 部署到 vercel 并绑定域名
- [ ] 图片懒加载
- [x] feat: 图片向上渐显飞入的入场动画？
