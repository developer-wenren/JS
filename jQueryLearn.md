

# jQuery Form CodeSchool

### ***Write Less, Do More***

> `jQuery(dom)`
> 
> **Find Elements by tag, id, class**
> 
> - > jQuery(tag)`  == `$(tag)`
> 
> 
> - `$(“.promo”)`
> 
> 
> - `$(“#className”)`
> 
> **Change Attribute**
> 
> - `$(“h1”).text = “hi”`
> - `$(document).ready(function) {});`

------

> **Search Dom elements**
> 
> - find children `$(ul, li)`
> - find direct-children `$(ul>li)`
> - find first child or last child `$(ul, li:first)`  , `$(ul, li:last)`
> - find even or odd child `$(ul>li:even)` , `$(ul>li:odd)`

------

> **Traversing DOM**
> 
> - Find( )方法
>   - `$(slection). find(targetElement)`
> 
> 
> - first() , next(), prev()
>   - `$(targerElement).first() next() prev()`
> 
> 
> - 子标签 `children()`
> 
> 
> - 父标签`parent()`

------

> **Manipulating DOM**
> 
> - create Element  $(‘<tag>Text</tag>’)
> - append Element ` before(), prepend(), append(), insertAfter(), insertBefore()`
> - remove Element : ` element.remove()`

------

> **EventHandler**
> 
> - button `click( )`
> - document `ready()`
> - function target `this`
> - relativeTraverse`closest(element)`

------

> **Fetch Data From Dom**
> 
> - data-name `data(’name’)`

------

> **Deal Class**
> 
> - filter Dom `filter(id/class)`
>   
> - addClass `element.addClass(className)`
>   
> - toggleClass `element.toggleClass(className)`
>   
> - removeClass `element.remove(className)`
>   
>   ​

------

> **Listen Dom Event**
> 
> - show Element `.slideDown()`, `.slideTo()`, `.slideToggle`, `fadeIn()`, `fadeOut`
> - mouse Event ` mouseenter`, `mouseleave`
> - keyboard Event `keypress, keydown, keyup`
> - getVlaue/setValue `+$(element).val()`  , `.val(newValue)`
> - event  param  `.stopPropagation()` ,  `.preventDefault()`

------

> **Change Syle**
> 
> ` .css(attr, value)`
> 
> `.css({ object })`	
> 
> __Animation__
> 
> `.animate({‘attr’: ‘value’,'attr2': 'value2'}, duration )`