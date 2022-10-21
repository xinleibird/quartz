---
title: Identifier
aliases: [标识符, 变量名, 函数名, 属性名, 键, Identifier, Key]
tags: [JS]
enableToc: true
lastmod: 2022-10-21
---

> [!summary]
>「标识符 [^1]」是代码中用来「识别」和「控制」[[JavaScript/Variable|变量]]、[[JavaScript/Function|函数]]、[[JavaScript/Type/Object/Property|属性]] 的「链」。我们可以简单的总结：「标识符」可以作为 [[JavaScript/Identifier|变量名]]、[[JavaScript/Identifier|函数名]] 和 [[JavaScript/Identifier|属性名]]。
> <br>
>「标识符」的 [[JavaScript/Type|类型]] 可以是 [[JavaScript/Type/Primitive/string|string]] 或者 [[JavaScript/Type/Primitive/symbol|symbol]]。

## 标识符命名规则

当使用 [[JavaScript/Type/Primitive/string|string]] 时：

- 只能包含：**字母**、**数字**、**下划线 `_`**、**美元符号 `$`**，且 **不能以数字开头**。
- 区分大小写。
- 可以使用大部分 Unicode[^2] 字符。

当使用 [[JavaScript/Type/Primitive/symbol|symbol]] 时：

- 由于 [[JavaScript/Type/Primitive/symbol|symbol]] 可以确保唯一性，因此无特殊要求。

## 标识符是「链」

前面提到了「链」，我们举个简单的例子：

```js
const hello = "fuck";

console.log(hello);	// "fuck"
```

上面的例子不应该期待输出结果是 `hello`。我们将一个 [[JavaScript/Type/Primitive/string|string]] 类型的 `"hello"` 作为「标识符」从而代表」了实际存储的字符串 `"fuck"`。

## 标识符是「键」

我们可以把数据存储简单的看做是一个 [[JavaScript/Identifier|键]] ⇢ [[JavaScript/Value|值]] 体系：由 [[JavaScript/Identifier|键]] 作为入口来访问 [[JavaScript/Value|值]]，这样我们就能摆脱直接通过内存地址进行数据访问的繁琐过程。在 JavaScript 中，「标识符」就是这个 [[JavaScript/Identifier|键]]。

假如有如下代码：

```js
const age = 12;
const gender = 1;
const info = {
	fatherName: "...",
};
const relations = [1, 3, 0 , 4];
```

我们把内存中的数据存储做一下抽象：

![[Attachments/Identifier.svg]]

可以看出，标识符是作为 [[JavaScript/Variable|变量]]、[[JavaScript/Function|函数]]、[[JavaScript/Type/Object/Property|属性]] 的 [[JavaScript/Identifier|键]] 而存在的：

![[Attachments/IdentifierKeyValue.svg]]

可以再抽象一下：

![[Attachments/IdentifierAbstract.svg]]

通过上面的例子可以明确，「标识符」就是作为 [[JavaScript/Identifier|键]] 来使用的。

[^1]: <https://developer.mozilla.org/zh-CN/docs/Glossary/Identifier>

[^2]: <https://home.unicode.org>
