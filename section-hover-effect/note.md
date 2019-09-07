## z-index

1. `z-index` doesn't work unless that element is set to `position:relative`

2. [how is the z-index determined]([http://plnkr.co/edit/CCO4W0NS3XTPsVL9Bqgs?p=preview](http://plnkr.co/edit/CCO4W0NS3XTPsVL9Bqgs?p=preview))

   [z-index relative or absolute?](https://stackoverflow.com/questions/7490146/z-index-relative-or-absolute)

## background:linear-gradient

背景渐变，可以设置多种颜色，并为他们设置位置，位置使用相对背景宽度的百分比

```css
background:linear-gradient(red 0%, orange 25%, yellow 50%, green 75%, blue 100%);
```

比如我有一个宽度1000px的div，上面的设置是

> 0 - 250px: 红橙渐变
>
> 250px - 500px: 橙黄渐变
>
> 500px - 750px: 黄绿渐变
>
> 750px - 1000px: 绿蓝渐变

可以利用这个性质设置多色（块）背景

~~~css
background: linear-gradient(#0f4675, #0f4675 50%, #fff 50%, #fff);
~~~

还是宽度1000px的div

> 0 - 500px: `#0f4675`到`#0f4675`的渐变，所以全都是`#0f4675`
>
> 500px - 500px: 从`#0f4675` 瞬间转为白色
>
> 500px - 1000px; 全白

