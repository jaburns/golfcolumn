## Golf Column

Classic rotating column effect in a 317 byte HTML file.

### [View it live](https://jaburns.github.io/golfcolumn/)

### Final source
```
<b id=A></b><b id=B><style onload="q=t=99;setInterval(_=>{for(T=t+=.04*(C=Math.cos)(q/4);T>(P=1.57);
T-=P);[Z=A.style,B.style].map((x,i)=>{x.width=200*C(T-P*i);x.background=`#f${[7,8,7,6][(0|t/P+i)%4]}
3`});Z.marginLeft=350*C(q+=.02)},30)">*{margin:0;text-align:center;height:100%;background:#144}b{dis
play:inline-block
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
q = t = 99;

setInterval(_ => {
    for(
        T = t += .04 * (C=Math.cos)(q / 4);
        T > (P=1.57);
        T -= P
    );

    [Z=A.style,B.style].map((x,i) => {
        x.width = 200 * C(T-P*i);
        x.background = `#f${[7,8,7,6][ (0|t/P+i) % 4 ]}3`
    });

    Z.marginLeft = 350 * C(q+=.02)
}, 30)
```
