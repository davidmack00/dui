# Direct UI - Effortless interaction without JS

<p>Direct UI is designed to provide a basic yet powerful interactive layer for web pages without writing a single line of JavaScript.</p>

<p>To use it, simply add dui attributes to elements. These attributes will invoke the addition or removal of the class name "dui-active" to a target element. In Direct UI, there are two types of elements, triggers (ones that start an action) and targets (ones that recieve an action). Both have serveral attribute options to chose from</p>


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
