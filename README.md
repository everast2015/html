# html标签

## 文本格式化标签


标签 | 显示效果 | 
---------|----------|
 `<b></b><strong></strong>` | 文字以**粗体**方式展示（xhtml推荐使用strong） | 
 `<i></i><em></em>` | 文字以**斜体**方式展示（xhtml推荐使用em） | 
 `<s></s><del></del>` | 文字以加~~删除线~~的方式展示（xhtml推荐使用del） | 
 `<u></u>和<ins></ins>` | 文字以加下划线的方式展示（xhtml不赞成使用u）

 ## 锚点定位

```html
<a href="#id"></a>

<div id="id"></div>

```
锚点定位的特点就是利用`href="#链接的id名称"` 就是锚点链接所对应跳转的地址

## 特殊字符


特殊字符名称 | 实体标识符 |
---------|----------|
 空格 | `&nbsp;` |
 小于号 | `&lt;` |
 大于号 | `&gt;` |
版权 | `&copy;` | 
人民币 | `&yen;`

## 列表标签

- 无序列表
- 有序列表
- 自定义列表

1. 无序列表

> 无序列表的各个列表项之间没有顺序级别之分，是并列关系的

```html
<ul>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
</ul>

```

2. 有序列表

> 有序列表即为有排列顺序的列表，其每个列表按照一定的顺序排列，有序列表的基本语法格式

```html
<ol>
    <li>无序列表1</li>
    <li>无序列表2</li>
    <li>无效列表3</li>
</ol>

```


```html

<ul>
    <li>
        <h3>《红楼梦》</h3>
        <p>满纸荒唐言，一把辛酸泪，都云作者痴，谁解其中味。</p>
    </li>
    <li>
        <h3>泰坦尼克号</h3>
        <p>以你之名，冠我之姓</p>
    </li>
</ul>

```
3. 自定义列表
> 自定义列表用于对术语或名称进行解释
```html

<dl>
    <dt>名称1</dt>
    <dd>名称解释</dd>
    <dd>名称解释</dd>
</dl>

```

## lable 标签和input标签的使用

```html
<label>
    《平凡之路》
    <input type="text"/>
</label>

```

好处就是点击文字的时候，光标就聚焦在`<input/>` 文本框的里面

![点击文字聚焦input](https://github.com/yjn2015/html/blob/master/img/label.png)

## `html5`语义化标签


语义化标签 | 标签 | 使用的场景 |
---------|----------| ------- |
 `header` | 头部 | 网站标志，主导航，全站链接，搜索框
 `nav` | 导航条 | 主要导航部分
 `main` | 主要内容 | 网站页面的主要内容，一个页面只能使用一次
 `article` | 文章标记 | 表示的是一个文档，页面，主要的容器
 `section` | 区块 | 一组相似主题的内容，一般会有一个标题
 `aside` | 侧边栏 | 表示一部分内容与页面的主体没有较大的关系，并且可以独立存在
 `footer` | 页脚 | 表示的是附言，版权的相关信息

 ## `html5` 标签的兼容性问题

 > 对于`IE9`以上的浏览器部分都支持`html5`的标签，但是对于`IE8`以下的浏览器，是不支持`html5`的标签的

 对于不支持的情况，我们可以手动创建：

```html
 document.createElement("header");
 document.createElement("nav");
 document.createElement("main");
 document.createElement("article");
 document.createElement("aside");
 document.createElement("footer");
```
方法二、引入第三方插件

> html5shiv.min.js 在默认情况下，IE8及以下的IE版本不支持html5，引入这个文件就可以做到兼容性的处理

## `html5` 新增的表单

input 新增type属性 | 表单说明 | 解释
-------------------|----------|---------|
 `email` |  `<input type="email"/>` | 电子邮箱说明
 `tel` | `<input type="tel"/>` | 主要目的就是为了弹出一个数字键盘
 `url`| `<input type="url"/>` | 输入合法的网址
 `number` | `<input type="number"/>` | 只能输入数字，不能输入其他的字符
 `search` | `<input type="search"/>` | search 可以提供更人性化的体验
 `range`  | `<input type="range"/>` | `range` 范围