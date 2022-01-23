# huddle landing page with alternating feature blocks

Date: 2022/01/20
Tags: css, html

项目名称：具有交替功能块的huddle登录页面

项目地址：[https://www.frontendmentor.io/challenges/huddle-landing-page-with-alternating-feature-blocks-5ca5f5981e82137ec91a5100](https://www.frontendmentor.io/challenges/huddle-landing-page-with-alternating-feature-blocks-5ca5f5981e82137ec91a5100)

项目步骤：

- 因为在GitHub上对上个项目的README文件进行了修改，那么我就想本地的并没有更新，肯定是需要把更新的部分拉回本地的。
    
    ![Untitled](huddle%20landing%20page%20with%20alternating%20feature%20block%201b8bece01c26401e98f373af8a30d0e1/Untitled.png)
    
    - [ ]  关于系统学习git版本控制：
        
        [Set up Git - GitHub Docs](https://docs.github.com/en/get-started/quickstart/set-up-git)
        
- CSS初始化代码
    
    > 需要知道的是：一些html标签中是自带margin属性的，比如一般浏览器都会给body标签自带了8px的margin属性。这会使边沿留出了8px的间隔。很多块级元素都有默认边距，清除它们才有利于我们的开发。
    > 
    
    初始化代码的作用：在HTML标签在浏览器里有默认的样式，例如 p 标签有上下边距，strong标签有字体加粗样式，em标签有字体倾斜样式。不同浏览器的默认样式之间也会有差别，例如ul默认带有缩进的样式，在IE下，它的缩进是通过margin实现的，而Firefox下，它的缩进是由padding实现的。在切换页面的时候，浏览器的默认样式往往会给我们带来麻烦，影响开发效率。所以解决的方法就是一开始就将浏览器的默认样式全部去掉，更准确说就是通过重新定义标签样式。“覆盖”浏览器的CSS默认属性。最最简单的说法就是把浏览器提供的默认样式覆盖掉！这就是CSS reset。
    
    [https://blog.csdn.net/pengpengpeng85/article/details/52070583](https://blog.csdn.net/pengpengpeng85/article/details/52070583)
    
    可以设置reset.css文件提高效率[https://blog.css8.cn/post/14959633.html](https://blog.css8.cn/post/14959633.html)
    
    **font-size:100%有什么作用?** [https://www.cnblogs.com/zhp404/articles/3791391.html](https://www.cnblogs.com/zhp404/articles/3791391.html)
    
    通常情况下这样就行：
    
    ```css
    * {
    	padding: 0;
    	margin: 0;
    	font-family:'Courier New', Courier, monospace;
    	box-sizing: border-box;
    }
    ```
    
- 了解网页的常见布局及实现
    
    from github [https://github.com/Sweet-KK/css-layout(内容随时更新)](https://github.com/Sweet-KK/css-layout)
    
- 确定本项目的layout
    
    ![Untitled](huddle%20landing%20page%20with%20alternating%20feature%20block%201b8bece01c26401e98f373af8a30d0e1/Untitled%201.png)
    
    可以分为上 中 下 三个部分，分别对应：top center bottom 三大部分采用flex纵向布局。
    
- coding the HTML section
    
    ![Untitled](huddle%20landing%20page%20with%20alternating%20feature%20block%201b8bece01c26401e98f373af8a30d0e1/Untitled%202.png)
    

项目要求：

desktop 桌面端 1440px宽—我按照我笔记本的宽度 1266.33px设计

mobile 移动端 375px宽—我按照iphoneSE的尺寸设计

为达到适配这两个屏幕的网页显示效果，使用了如下方法：

1. 弹性盒子+rem 布局
2. 媒体查询 
    
    以600px 为分割点
    

完成对比：左(原)  右(我)

移动端：

![mobile-design.jpg](huddle%20landing%20page%20with%20alternating%20feature%20block%201b8bece01c26401e98f373af8a30d0e1/mobile-design.jpg)

![https://s4.ax1x.com/2022/01/23/74T8Tf.png](https://s4.ax1x.com/2022/01/23/74T8Tf.png)

桌面端对比：

![desktop-design.jpg](huddle%20landing%20page%20with%20alternating%20feature%20block%201b8bece01c26401e98f373af8a30d0e1/desktop-design.jpg)

![https://s4.ax1x.com/2022/01/23/74TJk8.png](https://s4.ax1x.com/2022/01/23/74TJk8.png)

*可见还是有些不一样的：

1. 细节上 字体、按钮颜色、间距
2. 高度

造成不想动手改原因在于做到后面改到后面就烦躁了。

新增知识点：

1. CSS初始化代码
2. 媒体查询
3. flex布局
4. 颜色块布局法 熟练之后可以不用
5. 漂白图片
6. rem单位的使用

项目感悟：

1. 多看看别人怎么做的。
2. coding之前的预设很重要，想清楚html代码该怎么写，属性该怎么写，都有哪些是一样的，有哪些公共部分。
3. 可以选择不用less。
4. 提取公共部分作为公共变量，如背景色，字体字号等等。