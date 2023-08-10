---
title: "Small things that I've just wanted to discover before"
date: 2023-08-03T11:30:03+00:00
weight: 5
# aliases: ["/first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: true
hidemeta: false
comments: false
description: "A short description of things I've just wanted to discover before"
canonicalURL: "/blog/"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: false
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

How many times have you been in a situation where you just discover something super useful (a library, a shortcut, a very easy way to do something) and you think "I wish I knew this before"? Well, I've been in that situation a lot of times, so I decided to create this blog post to write down all those things that I've just wanted to discover before.

Maybe you already know some of these things, maybe you don't, maybe these things are useful only for me. But I hope you find something useful here.

## Einops
![meme_shape](/blog/images/meme_shape.jpg)

Well, this is a very useful and famous library, but I didn't know it until my second year of graduate school. If you are familiar with Deep Learning, you know for sure the pain to handle tensor shapes. Well, [Einops](https://einops.rocks/ ) is a library that allows you to handle tensor shapes in a very easy way. For example, if you want to transpose a tensor, you can do it with the following code:

```python
import einops
import torch

x = torch.randn(2, 3, 4, 5)
x = einops.rearrange(x, 'a b c d -> a c b d')
print(x.shape) # torch.Size([2, 4, 3, 5])
```
You can also use it to do reductions, for example, if you want to compute the mean of a tensor along a specific dimension, you can do it with the following code:

```python
import einops
import torch

x = torch.randn(2, 3, 4, 5)
x = einops.rearrange(x, 'a b c d -> a c b d')
x = einops.reduce(x, 'a c b d -> a c d', 'mean')
print(x.shape) # torch.Size([2, 4, 5])
```
or repeat a tensor along a specific dimension:

```python
import einops
import torch

x = torch.randn(2, 3, 4, 5)
x = einops.rearrange(x, 'a b c d -> a c b d')
x = einops.repeat(x, 'a c b d -> a c b d', 2)
print(x.shape) # torch.Size([2, 6, 3, 5])
```

Check out the [documentation](https://einops.rocks/ ) for more examples and details.