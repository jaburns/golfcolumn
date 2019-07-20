## Golf Column

Classic rotating column effect in a 343 byte HTML file.

### [View it live](https://jaburns.github.io/golfcolumn/)

### Final source
```
<b id=A></b><b id=B><style onload="t=99;q=0;P=1.57;C=Math.cos;setInterval(_=>{for(T=t+=.04*C(q/4);T>
P;T-=P);[A.style,B.style].map((x,i)=>{x.width=200*C(T-P*i);x.background=`#f${[X=70,83,X,61][(0|t/P+i
)%4]}`});A.style.marginLeft=350*C(q+=.02)},30)">*{margin:0;text-align:center;height:100%;background:
#144;overflow:hidden}b{display:inline-block
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
    background: #144;
    overflow: hidden
}
b {
    display: inline-block
```

#### Javascript
```javascript
t = 99;
q = 0;
P = 1.57;
C = Math.cos;

setInterval(_=>{
    for(
        T = t += .04 * C(q / 4);
        T > P;
        T -= P
    );

    [A.style,B.style].map((x,i)=> {
        x.width = 200 * C(T-P*i);
        x.background = `#f${[X=70,83,X,61][ (0|t/P+i) % 4 ]}`
    });

    A.style.marginLeft = 350 * C(q+=.02)
},30)
```
