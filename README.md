## LESS mixins

### Usage

* `.clearfix()`
* `.hidden()`
* `.size()`
* `.border-radius()`
* `.box-sizing()`
* `.box-shadow()`
* `.transition()`
* `.filter()`
* `.rotate()`
* `.skew()`
* `.scale()`
* `.translate()`
* `.translate3d()`
* `.perspective()`
* `.placeholder()`
* `#gradient > .vertical(#333,#666)`
* `#gradient > .horizontal(#333,#666)`
* `flexbox()`
* `flex()`
* `order()`

### Example

#### .clearfix()

example

```less
.wj{
	.clearfix()
}
```

output

```css
.wj:before,
.wj:after {
  display: table;
  content: "";
}
.wj:after {
  clear: both;
}
```

#### #gradient > .horizontal(#000,#fff)

example

```less
.wj{
  #gradient > .horizontal(#000,#fff);
}

```

output

```css
.wj{
background-color: #ffffff;
  /* Konqueror */

  background-image: -khtml-gradient(linear, left top, right top, from(#000000), to(#ffffff));
  /* FF 3.6+ */

  background-image: -moz-linear-gradient(left, #000000, #ffffff);
  /* IE10 */

  background-image: -ms-linear-gradient(left, #000000, #ffffff);
  /* Safari 4+, Chrome 2+ */

  background-image: -webkit-gradient(linear, left top, right top, color-stop(0%, #000000), color-stop(100%, #ffffff));
  /* Safari 5.1+, Chrome 10+ */

  background-image: -webkit-linear-gradient(left, #000000, #ffffff);
  /* Opera 11.10 */

  background-image: -o-linear-gradient(left, #000000, #ffffff);
  /* IE10+ */

  background-image: -ms-linear-gradient(left, #000000 0%, #ffffff 100%);
  /* the standard */

}

```

#### .placeholder()

example

```less
.wj{
  .placeholder(#333);
}
```

output

```css
.wj :-moz-placeholder {
  color: #333333;
}
.wj ::-webkit-input-placeholder {
  color: #333333;
}
```