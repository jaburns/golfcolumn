## Golf Column

Classic rotating column effect in a 293 byte HTML file.

### [View it live](https://jaburns.github.io/golfcolumn/)

### Final source
```
<b id=A></b><b id=B><style onload="q=t=9;setInterval(_=>[Z=A.style,B.style].map((x,i)=>x.width=200*C
((t+=!i*.008*C(q/4))%(P=1.57)-i*P,x.background=`#f${5+(0|t/P+i)%4}3`),Z.marginLeft=350*(C=Math.cos)(
q-=.004)),5)">*{margin:0;text-align:center;height:100%;background:#144}b{display:inline-block
```

### Source with whitespace

#### HTML
```html
<b id=A></b><b id=B>
```

#### CSS
```css
* {
    margin: 0;
    text-align: center;
    height: 100%;
    background: #144
}
b {
    display: inline-block
```

#### Javascript
```javascript
q = t = 9;

setInterval(_ =>
    [Z=A.style,B.style].map((x,i) =>
        x.width = 200 * C(
            (t += !i * .008 * C(q / 4)) % (P=1.57) - i*P
        ,
            x.background = `#f${ 5+(0|t/P+i)%4 }3`
        )
    ,
        Z.marginLeft = 350 * (C=Math.cos)(q-=.004)
    )
,
    5
)
```
