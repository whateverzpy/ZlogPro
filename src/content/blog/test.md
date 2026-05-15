---
title: "Markdown 功能测试"
description: "用于测试 Astro 中 Markdown / GFM / frontmatter 的渲染效果"
pubDate: 2026-05-12
updatedDate: 2026-05-12
author: "Leo Zhu"
tags:
  - Astro
  - Markdown
  - Test
draft: false
heroImage: "./hero-test.png"
---

# H1 标题

这是一个用于测试 Astro Markdown 渲染的文章。

## H2 标题

### H3 标题

#### H4 标题

##### H5 标题

###### H6 标题

---

## 段落与换行

这是第一段。Markdown 中普通换行通常不会产生新的段落。

这是第二段。

行尾两个空格可以产生软换行。 
这是同一段里的下一行。

---

## 强调

普通文本。

*斜体*

**粗体**

***粗斜体***

~~删除线~~

`行内代码`

---

## 链接

[Astro 官网](https://astro.build)

自动链接：https://astro.build

---

## 图片

![测试图片](./hero-test.png)

---

## 无序列表

- 第一项
- 第二项
  - 嵌套项 A
  - 嵌套项 B
- 第三项

## 有序列表

1. 第一步
2. 第二步
   1. 子步骤
   2. 子步骤
3. 第三步

## 任务列表

- [x] 已完成
- [ ] 未完成
- [ ] 继续测试

---

## 引用

> 这是一级引用。
>
> > 这是嵌套引用。
>
> 引用中也可以使用 **粗体** 和 `代码`。

---

## 表格

| 功能 | Markdown | Astro |
|:---|:---:|---:|
| 标题 | 支持 | 支持 |
| 表格 | GFM 支持 | 支持 |
| 任务列表 | GFM 支持 | 支持 |
| 组件 | 不支持 | 请用 MDX |

---

## 代码块

```js
const site = "Astro";

function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet(site));
```

```ts
type Post = {
  title: string;
  pubDate: Date;
  draft?: boolean;
};

const post: Post = {
  title: "Markdown 功能测试",
  pubDate: new Date("2026-05-12"),
};
```

```bash
pnpm create astro@latest
pnpm astro add mdx
pnpm dev
```

```ansi
[1;31mERROR[0m
[1;32mSUCCESS[0m
[1;33mWARNING[0m
```

---

## HTML

<div class="custom-html-block">
  <p>Markdown 中可以直接写 HTML。</p>
</div>

<details>
  <summary>点击展开</summary>

这里是 details 内部内容。

</details>

---

## 脚注

这是一个带脚注的句子。[^note]

[^note]: 这是脚注内容。

---

## 转义字符

\*这不会变成斜体\*

\# 这不会变成标题

---

## 特殊字符

中文标点：，。！？；：

英文符号：& < > " '

Emoji：🚀 🧪 📚

---

## 数学公式测试

如果你安装并配置了 remark-math / rehype-katex，可以测试：

行内公式：$E = mc^2$

块级公式：

$$
f(x) = x^2 + 2x + 1
$$

未配置数学插件时，这些内容通常只会作为普通文本处理。

---

## 结束

如果你能看到以上内容正常渲染，说明基础 Markdown 测试通过。
