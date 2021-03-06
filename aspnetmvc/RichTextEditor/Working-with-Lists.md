---
layout: post
title: Working with Lists related operation in RichTextEditor widget for Syncfusion Essential ASP.NET MVC
description: Working with Lists related changes in RichTextEditor widget
platform: ejmvc
control: RTE
documentation: ug
keywords: RichTextEditor, Create a Lists, Custom Lists, customOrderedList, customUnorderedList

---

# Working with Lists

The editor provides tools to makes your content as list such as an ordered and unordered list.

## Create a Lists

By default, [Insert Lists](http://help.syncfusion.com/js/api/ejrte#members:tools-lists) tool is enabled in the editor’s toolbar.The editor’s have ordered and unordered list types.

{% highlight html %}

    
@{
    List<String> toolsList = new List<string>() { "lists" };
    List<String> lists = new List<string>() { "unorderedList", "orderedList" };
}
@{Html.EJ().RTE("rteSample").Width("800px").ContentTemplate(@<div>
    The Rich Text Editor
    (RTE) control is an easy to render in client side. Customer easy to edit the contents
    and get the HTML content for the displayed content. A rich text editor control provides
    users with a toolbar that helps them to apply rich text formats to the text entered
    in the text area.
</div>)
.ToolsList(toolsList)
.Tools(tool => tool.Lists(lists))
.Render();}
<br />

{% endhighlight %}

## Custom Lists

You can use [custom lists](http://help.syncfusion.com/js/api/ejrte#members:tools-customOrderedList) tools to insert lists with custom behaviors.You can create a list with related attributes (such as listImage, listStyle, title, name, and text) using the custom list tool.Ordered and Unordered list having own customize ways to insert a list into the editor’s content.

* [Insert a customOrderedList](#insert-a-customOrderedList)
* [Insert a customUnorderedList](#insert-a-customUnorderedList)  


### Insert a customOrderedList

you need to enable [customOrderedList](http://help.syncfusion.com/js/api/ejrte#members:tools-customOrderedList) tool on the editor’s toolbar.

The customOrderedList having below options for an ordered list customization.

<table>
<tr>
<th>
Option<br/><br/></th><th>
Summary<br/><br/></th></tr>
<tr><td>name</td><td>Specifies the name for customOrderedList item.</td></tr>
<tr><td>tooltip</td><td>Specifies the title for customOrderedList item.</td></tr>
<tr><td>CSS</td><td>Specifies the styles for customOrderedList item.</td></tr>
<tr><td>text</td><td>Specifies the text for customOrderedList item.</td></tr>
<tr><td>listStyle</td><td>Specifies the list style for customOrderedList item.</td></tr>
<tr><td>listImage</td><td>Specifies the image for customOrderedList item.</td></tr>
</table>

{% highlight html %}

@{Html.EJ().RTE("rteSample").Width("800px").ContentTemplate(@<div>
    The Rich Text Editor
    (RTE) control is an easy to render in client side. Customer easy to edit the contents
    and get the HTML content for the displayed content. A rich text editor control provides
    users with a toolbar that helps them to apply rich text formats to the text entered
    in the text area.
</div>)
.Tools(tool => tool.CustomOrderList(customOrder => customOrder.Css("e-rte-toolbar-icon e-rte-listitems customOrder").ListStyle("lower-greek").Name("orderInsert").Tooltip("Custom OrderList").Text("Lower-Greek").Add()))
.Render();}
<br />

{% endhighlight %}

![](WorkingwithLists_images/ordered.png)

### Insert a customUnorderedList

you need to enable [customUnorderedList](http://help.syncfusion.com/js/api/ejrte#members:tools-customUnorderedList) tool on the editor’s toolbar.

The customUnorderedList having below options for an unordered list customization.

<table>
<tr>
<th>
Option<br/><br/></th><th>
Summary<br/><br/></th></tr>
<tr><td>name</td><td>Specifies the name for customUnorderedList item.</td></tr>
<tr><td>tooltip</td><td>Specifies the title for customUnorderedList item.</td></tr>
<tr><td>CSS</td><td>Specifies the styles for customUnorderedList item.</td></tr>
<tr><td>text</td><td>Specifies the text for customUnorderedList item.</td></tr>
<tr><td>listStyle</td><td>Specifies the list style for customUnorderedList item.</td></tr>
<tr><td>listImage</td><td>Specifies the image for customUnorderedList item.</td></tr>
</table>

{% highlight html %}

@{Html.EJ().RTE("rteSample").Width("800px").ContentTemplate(@<div>
    The Rich Text Editor
    (RTE) control is an easy to render in client side. Customer easy to edit the contents
    and get the HTML content for the displayed content. A rich text editor control provides
    users with a toolbar that helps them to apply rich text formats to the text entered
    in the text area.
</div>)
.Tools(tool => tool.CustomOrderList(customOrder => customOrder.Css("e-rte-toolbar-icon e-rte-listitems customOrder").ListStyle("lower-greek").Name("orderInsert").Tooltip("Custom OrderList").Text("Lower-Greek").Add()))
.Render();}
<br />

{% endhighlight %}

![](WorkingwithLists_images/unordered.png)

