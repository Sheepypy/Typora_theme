# Typora_theme
My self-use Typora theme

# 使用方法
解压docsify-yyy.rar，将docsify-yyy文件夹和docsify-yyy.css一起复制到C:\Users\xxx\AppData\Roaming\Typora\themes，重启Typora软件选择该主题即可。

![image](https://github.com/Sheepypy/Typora_theme/assets/84173072/579652d8-587f-42ba-b8b2-4aa1a3fedbb3)

# 效果展示
在官方给的主题上做了一些改动，符合我自己的审美，修改了内容宽度、代码颜色、标题样式、引用块颜色等等，在代码中也有一定的注释说明，希望能给找一个好看的主题的同学提供帮助。

先放一下整体效果：

![在这里插入图片描述](https://img-blog.csdnimg.cn/7636b3f2fc0a4602816f5213914b84f8.png)

代码效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/6196a48abaf5415cb3a1aaa3de7516dc.png)

表格效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/c6b477d795d140918a2e78c0ceca5bdb.png)

# 自定义修改
一些涉及个人审美的地方可以自己修改，例如：

- 引用：

  ```css
  #write blockquote,
  .markdown-section blockquote {
    padding: 0.75rem 0.75rem; /*边框粗细*/
    border-left: 4px solid #CCC; /*左竖条颜色*/
    background: rgba(245, 245, 245, 0.5);
    color: rgba(34, 34, 34, 0.75);
    border-radius: 0 0.5em 0.5em 0;/*边框转角半径大小*/
    transition: 1s;
  }
  ```

- 一级标题居中：

  ```css
  #write h1 *,
  .markdown-section h1 *{
    text-align: center;
  }
  ```

- 文本宽度：自适应缩放至屏幕80%，左右边距2em

  ```css
  #write,
  .markdown-section {
    max-width: 80%;
    padding-left: 2em;
    padding-right: 2em;
  ```

- 标题下方分割线：solid实线，dotted点线

  ```css
  #write h3 *,
  .markdown-section h3 * {
    border-bottom: 1px solid rgb(129, 143, 206);
    font-size: 1.5rem;
  }
  ```

- 代码颜色：在typora-docsify\codeblock.css中修改

  ```css
  :root {
      --code-background: #282a36;
      --code-current-line: #44475a;
      --code-section: #44475a;
      --code-foreground: #f8f8f2;
      --code-comment: #cfbc0c;
      --code-cyan: #8be9fd;
      --code-green: #50fa7b;
      --code-orange: #ffb86c;
      --code-pink: #ff79c6;
      --code-purple: #bd93f9;
      --code-red: #ff5555;
      --code-yellow: #f1fa8c;
      --code-math: #151320;
  }
  
  /** code highlight */
  
  .cm-s-inner .cm-variable {/* 入参定义，亮绿色 */
      color: var(--code-green)
  }
  
  .cm-s-inner .cm-operator {/* +=等操作符，粉色*/
      color: var(--code-pink)
  }
  
  .cm-s-inner .cm-property {
      color: var(--code-foreground);
  }
  
  .cm-s-inner .cm-keyword {/* if、return等关键字粉色*/
      color: var(--code-pink);
  }
  
  .cm-s-inner .cm-tag {
      color: var(--code-pink);
  }
  
  .cm-s-inner .cm-attribute {
      color: var(--code-green);
  }
  
  .CodeMirror div.CodeMirror-cursor {
      border-left: 1px solid var(--code-foreground);
      z-index: 3;
  }
  
  .cm-s-inner .cm-string,
  .cm-s-inner .cm-string-2 {
      color: var(--code-yellow);
  }
  
  .cm-s-inner .cm-comment,
  .cm-s-inner.cm-comment { /*注释绿色*/
      color: var(--code-comment);
  }
  
  .cm-s-inner .cm-header,
  .cm-s-inner.cm-header,
  .cm-s-inner .cm-def,
  .cm-s-inner.cm-def {  /* 函数定义，黄色 */
      color: var(--code-yellow);
  }
  
  .cm-s-inner .cm-quote,
  .cm-s-inner.cm-quote {
      color: #57ac57;
  }
  
  .cm-s-inner .cm-hr {
      color: #d8d5d5;
  }
  
  .cm-s-inner .cm-link {
      color: #d3d3ef;
  }
  
  .cm-s-inner .cm-negative {
      color: #d95050;
  }
  
  .cm-s-inner .cm-positive {
      color: #50e650;
  }
  
  .cm-s-inner .cm-meta{/* 头文件、宏定义一整行 绿色*/
      color: var(--code-green);
  }
  .cm-s-inner .cm-qualifier { 
      color: var(--code-green);
  }
  
  .cm-s-inner .cm-builtin {
      color: var(--code-green);
  }
  
.cm-s-inner .cm-bracket {/* 花括号 */
    color: #00BFFF;
}
  
  .cm-s-inner .cm-atom,
  .cm-s-inner.cm-atom {
      color: var(--code-cyan);/* 原子 true、false 蓝绿色*/
  }
  
  .cm-s-inner .cm-number { 
      color: var(--code-purple);/*数字，紫色*/
  }
  
  .cm-s-inner .cm-variable {
      color: var(--code-foreground);
  }
  
  .cm-s-inner .cm-variable-2 {
      color: var(--code-foreground);
  }
  
  .cm-s-inner .cm-variable-3 {/*返回值、变量类型，int、void等，蓝绿色*/
      color: var(--code-cyan);
      font-style: italic;
  }
  
  .CodeMirror-selectedtext,
  .CodeMirror-selected {
      background: var(--code-current-line);
      color: #fff !important;
      text-shadow: none;
  }
  
  ```


--------------
待更新
