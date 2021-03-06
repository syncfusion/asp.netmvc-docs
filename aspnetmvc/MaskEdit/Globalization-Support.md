---
layout: post
title: Globalization Support | MaskEdit | ASP.NET MVC | Syncfusion
description: globalization support
platform: ejmvc
control: MaskEdit
documentation: ug
---

# Globalization Support in MaskEdit

We have provided the globalization support in **MaskEdit** control. Our **MaskEdit** control mainly rendered based on the **maskFormat** property, so we have provided the globalization support based on the maskFormat literals. We have given this globalization support option on below maskFormat literals in **MaskEdit** control. You can change the globalization by using the [locale](https://help.syncfusion.com/api/js/ejmaskedit#members:locale) property. The default value for **locale** property is 'en-US' in **MaskEdit** control.

<table class="props">
<thead>
<tr>
<th>Formats</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="formats">
$</td>
<td class="description">Currency symbol value will be changed based on the corresponding culture.</td>
</tr>
<tr>
<td class="formats">
.</td>
<td class="description">Decimal Separator value will be changed based on the corresponding culture.</td>
</tr>
<tr>
<td class="formats">
,</td>
<td class="description">Thousand Separator will be changed based on the corresponding culture.</td>
</tr>
</tbody>
</table>

To know more about EJ globalize support, please refer the below link

[https://help.syncfusion.com/aspnetmvc/globalization](https://help.syncfusion.com/aspnetmvc/globalization)


The following example describes the way to use localization in MaskEdit.


Refer the below German culture file in head section of HTML page after the reference of **ej.web.all.min.js** file.

 {% highlight javascript %}
   
           <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/i18n/ej.culture.de-DE.min.js"></script>
                
 {% endhighlight %}

{% highlight CSHTML %}

<label for="mask">Mask Edit</label>

@(Html.EJ().MaskEdit("maskedit").InputMode(InputMode.Text).MaskFormat("$999,999.99").Width("100%").Locale("de-DE"))

{% endhighlight %}





Output of MaskEdit with localization.



![](Globalization-Support_images/Globalization-Support_img1.jpg)

MaskEdit with de-DE locale
{:.caption}


![](Globalization-Support_images/Globalization-Support_img2.jpg)

MaskEdit with default (en-US) locale	
{:.caption}
