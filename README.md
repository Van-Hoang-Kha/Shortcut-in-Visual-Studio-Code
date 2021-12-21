# Shortcut-in-Visual-Studio-Code
## Syntax
### Child: >
```
nav>ul>li
```
Result: 

```
<nav>
    <ul>
        <li></li>
    </ul>
</nav>

```
### Sibling: +
```
div+p+bq
```
Result: 
```
<div></div>
<p></p>
<blockquote></blockquote>

```
### Climb-up: ^
### 1.
```
div+div>p>span+em^bq
```
Result: 
```
<div></div>
<div>
    <p><span></span><em></em></p>
    <blockquote></blockquote>
</div>
```
### 2.
```
div+div>p>span+em^^bq
```
Result:
```
<div></div>
<div>
    <p><span></span><em></em></p>
</div>
<blockquote></blockquote>
```
### Grouping: ()
### 1.
``` 
div>(header>ul>li*2>a)+footer>p
```
**Result: 
```
<div>
    <header>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
</div>
```
### 2. 
```
(div>dl>(dt+dd)*3)+footer>p
```
**Result:
```
<div>
    <dl>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
        <dt></dt>
        <dd></dd>
    </dl>
</div>
<footer>
    <p></p>
</footer>
```

### Multiplication: *
```
ul>li*5
```
Result:
```
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

### Item numbering: $
### 1.
```
ul>li.item$*5
```
Result:
```
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```
### 2.
```
h$[title=item$]{Header $}*3
```
Result:
```
<h1 title="item1">Header 1</h1>
<h2 title="item2">Header 2</h2>
<h3 title="item3">Header 3</h3>
```
### 3.
```
ul>li.item$$$*5
```
Result:
```
<ul>
    <li class="item001"></li>
    <li class="item002"></li>
    <li class="item003"></li>
    <li class="item004"></li>
    <li class="item005"></li>
</ul>
```
### 4.
```
ul>li.item$@-*5
```
Result:
```
<ul>
    <li class="item5"></li>
    <li class="item4"></li>
    <li class="item3"></li>
    <li class="item2"></li>
    <li class="item1"></li>
</ul>
```
### 5. 
```
ul>li.item$@3*5
```
Result:
```
<ul>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
    <li class="item6"></li>
    <li class="item7"></li>
</ul>
```

### ID and CLASS attributes
### 1.
```
#header
```
Result:
```
<div id="header"></div>
```
### 2.
```
.title
```
Result:
```
<div class="title"></div>
```
### 3. 
```
form#search.wide
```
Result:
```
<form id="search" class="wide"></form>
```
### 4.
```
p.class1.class2.class3
```
Result:

```
<p class="class1 class2 class3"></p>
```

### Custom attributes
### 1.
```
p[title="Hello world"]
```
Result:

```
<p title="Hello world"></p>
```
### 2. 
```
td[rowspan=2 colspan=3 title]
```
Result:

```
<td rowspan="2" colspan="3" title=""></td>
```
### 3. 
```
[a='value1' b="value2"]
```
Result:

```
<div a="value1" b="value2"></div>
```

### Text: {}
### 1.
```
a{Click me}
```
Result:
```
<a href="">Click me</a>
```
### 2.
```
p>{Click }+a{here}+{ to continue}
```
Result:
```
<p>Click <a href="">here</a> to continue</p>
```

### Implicit tag names
### 1.
```
.class
```
Result:
```
<div class="class"></div>
```
### 2.
```
em>.class
```
Result:
```
<em><span class="class"></span></em>
```
### 3.
```
ul>.class
```
Result:
```
<ul>
    <li class="class"></li>
</ul>
```
### 4.
```
table>.row>.col
```
Result:
```
<table>
    <tr class="row">
        <td class="col"></td>
    </tr>
</table>
```







