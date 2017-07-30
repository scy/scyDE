# Creating the Keyboard Layout Chart

To visualize the layout, this project uses the excellent service at `keyboard-layout-editor.com`, which is the hosted version of Ian Prest’s [Keyboard Layout Editor project](https://github.com/ijprest/keyboard-layout-editor).

You can either use [this enormous permalink](http://www.keyboard-layout-editor.com/##@_css=.dead%20%7B%20background-color/:%20#fcc/;%20border-radius/:%202px/;%20padding/:%200%200.2em/;%20%7D;&@=%C2%B0%0A%3Cspan%20class/=%22dead%22%3E%5E%3C//span%3E%0A%0A%5E&=!%0A1%0A%E2%82%81%0A%C2%B9&=%22%0A2%0A%E2%82%82%0A%C2%B2&=%C2%A7%0A3%0A%E2%82%83%0A%C2%B3&=$%0A4&=%25%0A5%0A%0A%E2%80%B0&=/&%0A6%0A%E2%80%A1%0A%E2%80%A0&=//%0A7%0A%0A%7B&=(%0A8%0A%0A%5B&=)%0A9%0A%0A%5D&=/=%0A0%0A%E2%89%A0%0A%7D&=?%0A%C3%9F%0A%E1%BA%9E%0A%5C&=%3Cspan%20class/=%22dead%22%3E%60%3C//span%3E%0A%3Cspan%20class/=%22dead%22%3E%C2%B4%3C//span%3E%0A%C2%B4%0A%60&_w:2;&=Backspace;&@_w:1.5;&=Tab&=Q%0A%0A%0A/@&=W%0A%0A%0A//&=E%0A%0A%0A%E2%82%AC&=R%0A%0A%0A(&=T%0A%0A%0A)&=Z%0A%0A%E2%80%94%0A%E2%80%93&=U%0A%0A%E2%8C%80%0A%CE%A3&=I%0A%0A%E2%90%A3%0A%C5%BF&=O&=P&=%C3%9C%0A%0A%E2%89%A5%0A%E2%89%A4&=*%0A+%0A%3Cspan%20class/=%22dead%22%3E~%3C//span%3E%0A~&_x:0.25&w:1.25&h:2&w2:1.5&h2:1&x2:-0.25;&=Enter;&@_w:1.75;&=Caps%20Lock&=A%0A%0A%0A%5B&=S%0A%0A%0A%5D&=D%0A%0A%0A%7B&_n:true;&=F%0A%0A%0A%7D&=G%0A%0A%E2%80%9A%0A%E2%80%9E&=H%0A%0A%E2%80%98%0A%E2%80%9C&_n:true;&=J%0A%0A%E2%80%99%0A%E2%80%9D&=K&=L%0A%0A%E2%87%90%0A%E2%86%90&=%C3%96%0A%0A%E2%87%94%0A%E2%86%94&=%C3%84%0A%0A%E2%87%92%0A%E2%86%92&='%0A#%0A%0A%E2%80%99;&@_w:1.25;&=Shift&=%3E%0A%3C%0A%C2%A6%0A%7C&=Y%0A%0A%E2%80%BA%0A%C2%BB&=X%0A%0A%E2%80%B9%0A%C2%AB&=C&=V&=B%0A%0A%E2%99%AF%0A%E2%99%AD&=N%0A%0A%C3%B7%0A%C3%97&=M%0A%0A%E2%88%92%0A%C2%B5&=/;%0A,%0A%C2%B1%0A%E2%80%A2&_fa@:0&:0&:1;;&=/:%0A.%0AZWNJ%0A%E2%80%A6&_fa@:0&:0&:1&:1;;&=/_%0A-%0ANBHY%0ASHY&_w:2.75;&=Shift;&@_w:1.25;&=Ctrl&_w:1.25;&=Win&_w:1.25;&=Alt&_f:3&w:6.25;&=%0A%0ANNBSP%0ANBSP&_w:1.25;&=AltGr&_w:1.25;&=Win&_w:1.25;&=Menu&_w:1.25;&=Ctrl) to load the scyDE layout, or use the following JSONish string and CSS.

Except for simply specifying the keys and what they do, the only thing that’s special is the use of the `.dead` CSS class to highlight dead keys in red.

## “JSON”

Load this into the “Raw data” tab:

```javascript
["°\n<span class=\"dead\">^</span>\n\n^","!\n1\n₁\n¹","\"\n2\n₂\n²","§\n3\n₃\n³","$\n4","%\n5\n\n‰","&\n6\n‡\n†","/\n7\n\n{","(\n8\n\n[",")\n9\n\n]","=\n0\n≠\n}","?\nß\nẞ\n\\","<span class=\"dead\">`</span>\n<span class=\"dead\">´</span>\n´\n`",{w:2},"Backspace"],
[{w:1.5},"Tab","Q\n\n\n@","W\n\n\n/","E\n\n\n€","R\n\n\n(","T\n\n\n)","Z\n\n—\n–","U\n\n⌀\nΣ","I\n\n␣\nſ","O","P","Ü\n\n≥\n≤","*\n+\n<span class=\"dead\">~</span>\n~",{x:0.25,w:1.25,h:2,w2:1.5,h2:1,x2:-0.25},"Enter"],
[{w:1.75},"Caps Lock","A\n\n\n[","S\n\n\n]","D\n\n\n{",{n:true},"F\n\n\n}","G\n\n‚\n„","H\n\n‘\n“",{n:true},"J\n\n’\n”","K","L\n\n⇐\n←","Ö\n\n⇔\n↔","Ä\n\n⇒\n→","'\n#\n\n’"],
[{w:1.25},"Shift",">\n<\n¦\n|","Y\n\n›\n»","X\n\n‹\n«","C","V","B\n\n♯\n♭","N\n\n÷\n×","M\n\n−\nµ",";\n,\n±\n•",{fa:[0,0,1]},":\n.\nZWNJ\n…",{fa:[0,0,1,1]},"_\n-\nNBHY\nSHY",{w:2.75},"Shift"],
[{w:1.25},"Ctrl",{w:1.25},"Win",{w:1.25},"Alt",{f:3,w:6.25},"\n\nNNBSP\nNBSP",{w:1.25},"AltGr",{w:1.25},"Win",{w:1.25},"Menu",{w:1.25},"Ctrl"]
```

(It’s not quite JSON, but this is how the tool outputs the data.)

## CSS

Load this into the “Custom Styles” tab:

```css
.dead { background-color: #fcc; border-radius: 2px; padding: 0 0.2em; }
```
