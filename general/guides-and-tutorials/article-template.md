---
description: This article shows formatting examples for a TSG wiki entry.
---

# Article template

This is a template article example to help contributors format their articles easier and to show what kinds of formatting possibilities there are.

## Section title

### Section sub-title

All titles made with the # leading like the example titles above will be shown in the "On this page" content table on the top right of the wiki article page to help quickly navigate the article.

* Here is information about this topic explained in a easily understandable manner. Here is an example of <a href="/main/halo-infinite/forge/lighting/fog" target="_Blank">a hyperlink</a> that can be used to redirect the user to a different place.
    * Here is an indentation section.

<figure><img src="/.gitbook/assets/template-image.jpg" alt="Image of a peculiar question mark (this text will show if the image can't load)"><figcaption><p>A white question mark on a grey background (a description of what is in the picture)</p></figcaption></figure>

<hr>

## Lists

### Unorderd list

With markdown

* List item
* List item
* List item

Or HTML

<ul>
  <li>List item</li>
  <li>List item</li>
  <li>List item</li>
</ul>

### Ordered list

With markdown

1. Item 1
2. Item 2
3. Item 3
    1. Item 3a
    2. Item 3b

Or HTML

<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
    <ol>
      <li>Item 3a</li>
      <li>Item 3b</li>
    </ol>
</ol>

### Table

With markdown

|Column 1|Column 2|Column 3|Column 4|
|-|-|-|-|
|First One|First Two|First Three|First Four|
|Second One|Second Two|Second Three|Second Four|
|Third One|Third Two|Third Three|Third Four|

Or HTML

 <table>
  <tr>
    <th>Column 1</th>
    <th>Column 2</th>
    <th>Column 3</th>
  </tr>
  <tr>
    <td>First One</td>
    <td>First Two</td>
    <td>First Three</td>
  </tr>
  <tr>
    <td>Second One</td>
    <td>Second Two</td>
    <td>Second Three</td>
  </tr>
</table> 


## Interactive things

### Video embed

{% embed url="https://youtu.be/A4cyNZ35xEY" %}
This is a tutorial video on getting started using the Blender2Forge Printer for Halo Infinite. (this text will show under the video embed)
{% endembed %}

### Info hint

{% hint style="info" %}
This is a transparent info box that can be used to convey highlight information like a clarification to the reader about a topic. The formatting of this info box won't preview properly in VS Code.
{% endhint %}

## Dropdown details

<details>
<summary>Wave Options</summary>

* Custom Wave A
* Custom Wave B
* Custom Wave C
* Custom Wave D
* Custom Wave E
* Custom Wave F
* Custom Wave G

</details>

## Text formatting

### Emphasis

*This text will be italic*  
_This will also be italic_

**This text will be bold**  
__This will also be bold__

_You **can** combine them_

### Quotes and code demonstration

> This is a blockquote. Markdown is a lightweight markup language with plain-text-formatting syntax, created in 2004 by John Gruber with Aaron Swartz.
>
>> Markdown is often used to format readme files, for writing messages in online discussion forums, and to create rich text using a plain text editor.



```
This is a block of code
let message = 'Hello world';
alert(message);
```



This is an example of `an inline code section`.



<hr>

**Contributors**\
Okom\
Another contributor name
