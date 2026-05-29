# Markdown 常用语法速查表（GitHub 适配版）

> 本速查表展示了 GitHub 上常用的 Markdown 语法，每个示例下方都附有对应的源码代码块。

## 标题
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

```markdown
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

## 文本样式
- *斜体*  
- **粗体**  
- ~~删除线~~ （GitHub 专属）  
- `行内代码`  
- **粗体中的 _斜体_**

```markdown
*斜体* 或 _斜体_
**粗体** 或 __粗体__
~~删除线~~
`行内代码`
**粗体中的 _斜体_**
```

## 列表
### 无序列表
- 项目 1
- 项目 2
  - 子项目（缩进 2 空格）
  * 混合符号

```markdown
- 项目 1
- 项目 2
  - 子项目
  * 混合符号
```

### 有序列表
1. 第一项
2. 第二项
   1. 子项（缩进 3 空格）
   2. 子项

```markdown
1. 第一项
2. 第二项
   1. 子项
   2. 子项
```

### 任务列表（GitHub 专属）
- [x] 已完成任务
- [ ] 待办任务

```markdown
- [x] 已完成任务
- [ ] 待办任务
```

## 链接与图片
- 链接：[GitHub](https://github.com)  
- 自动链接：<https://example.com>  
- 图片：  
![示例图片](https://via.placeholder.com/150 "占位图")

```markdown
[GitHub](https://github.com)
<https://example.com>
![替代文字](https://via.placeholder.com/150 "标题")
```

## 引用
> 这是一段引用。
> 可以跨多行。
>
> > 嵌套引用。

```markdown
> 这是一段引用。
> 可以跨多行。
>
> > 嵌套引用。
```

## 代码块
使用三个反引号并指定语言：
```javascript
function greet() {
  console.log("Hello, GitHub!");
}
```

````markdown
```javascript
function greet() {
  console.log("Hello, GitHub!");
}
```
````

## 表格
| 左对齐 | 居中对齐 | 右对齐 |
| :--- | :---: | ---: |
| 单元格 | 单元格 | 单元格 |
| 数据 | 数据 | 数据 |

```markdown
| 左对齐 | 居中对齐 | 右对齐 |
| :--- | :---: | ---: |
| 单元格 | 单元格 | 单元格 |
| 数据 | 数据 | 数据 |
```

## 分隔线
---

```markdown
---
```

## 脚注（GitHub 专属）
这是一个带脚注的文本[^1]。

[^1]: 脚注内容在这里。

```markdown
这是一个带脚注的文本[^1]。

[^1]: 脚注内容在这里。
```

## 转义字符
\*这不是斜体\*  
\`这不是代码\`

```markdown
\*这不是斜体\*
\`这不是代码\`
```

## Emoji（GitHub 专属）
输入 `:smile:` 渲染为 😄，`:+1:` 渲染为 👍。

```markdown
:smile: :+1:
```

---
> 更多语法请参考 [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)。
