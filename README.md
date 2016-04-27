# Direct UI - Effortless interaction for designers (no JavaScript)

<p>Direct UI is designed to provide a basic yet open-ended interactive layer for web pages without writing a single line of JavaScript. By providing a seamless way to add and remove a class name, you can create intracate widgets and pages with only html and css.</p>

<h4>class="dui-active" is the name of the game</h4>

<p>To use it, simply add dui attributes to elements. These attributes will invoke the addition or removal of the class name "dui-active" to a target element. In Direct UI, there are two types of elements, triggers (ones that start an action) and targets (ones that recieve an action). Both have serveral attribute options to chose from. Clicking on the page will automatically remove the dui-active class from all elements except what you clicked (and its ancestors), the target of your click (and its ancestors), and any pinned elements.</p>

<p><pre>
TRIGGER DUI ATTRIBUTES:
dui-toggle:	    toggles a target(s) (parent element if no target is specified)
dui-enable:	    enables a target(s) (parent element if no target is specified)
dui-disable:    disasbles a target(s) (parent element if no target is specified)

TARGET DUI ATTRIBUTES:
dui-id:         names a target
dui-pin:        keeps a target active unlesss explicitly disabled
dui-quiet:      makes a target close on the next click (even if it is clicked on)
</pre></p>

<h4>BASIC EXAMPLE</h4>
<p>Clicking the button...</p>
```html
<div class="parent">
  <div class="button" dui-toggle>I'm a button</div>
</div>
```
<p>...has this result</p>
```html
<div class="parent dui-active">
  <div class="button" dui-toggle>I'm a button</div>
</div>
```

<h4>EXAMPLE 2</h4>
<p>Clicking the button...</p>
```html
<div class="button" dui-disable="foo" dui-enable="bar">I'm a button</div>

<div dui-id="foo bar" dui-pin></div>
<div dui-id="foo baz" dui-pin></div>
<div dui-id="foo qux" dui-pin class="dui-active"></div>

<div dui-id="fred" class="dui-active"></div>
<div dui-id="waldo" dui-pin class="dui-active"></div>
```
<p>...has this result</p>
```html
<div class="button" dui-disable="foo" dui-enable="bar baz">I'm a button</div>

<div dui-id="foo bar" dui-pin class="dui-active"></div>
<div dui-id="foo baz" dui-pin class="dui-active"></div>
<div dui-id="foo qux" dui-pin class=""></div>

<div dui-id="fred" class=""></div>
<div dui-id="waldo" dui-pin class="dui-active"></div>
```

<p>*Direct UI requires jQuery</p>
