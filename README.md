# Donut.jl

Andy Sloane's `donut` written in Julia.

> **Reference**: https://www.a1k0n.net/2011/07/20/donut-math.html

<!--
<p align="center">
  <img src="./img/donut.svg">
</p>
-->

<br>

__Copy this into the Julia REPL to watch the 🍩 spin!__
```julia
            function donut()
       A=B=1;b=Vector(undef,1760)
     z=Vector(undef,1760);println(
   "\33[2J");print("\e[?25l");while true
  A+=0.07;B+=0.03;cA=cos(A);sA=sin(A);cB=
cos(B);sB=sin(B);for k = 1:length(b);b[k]=
k%80==79 ? "\n" : " ";z[k] = 0;end;for j in
range(0, step=            0.07,stop = 6.28);
ct=cos(j);st=              sin(j); for i in
range(0,step=               0.02, stop=6.28);
sp=sin(i); cp=             cos(i);h=ct+2;D=1/
(sp*h*sA+st*cA+           5);t=sp*h*cA-st*sA
 x=0|trunc(Int,40+      30*D*(cp*h*cB-t*sB))
 y=0|trunc(Int,12+15*D*(cp*h*sB+t*cB));o=x+
  80*y;N=0|trunc(Int, 8*((st*sA-sp*ct*cA)*
    cB-sp*ct*sA-st*cA-cp*ct*sB));if y<22&&
     y>=0&&x>=0&&x<79&&D>z[o];z[o]=D;b[o]=
       ".,-~:;=!*#\$@"[N>1 ? N : 1];end
         end;end;println("\033[1;1H"*
            join(b));sleep(0.03)
              end;end;donut()
```

View the raw donut at [`donut.jl`](https://raw.githubusercontent.com/mossr/Donut.jl/master/donut.jl) and an unobfuscated version at [`donut-unobfuscated.jl`](https://github.com/mossr/Tetris.jl/blob/master/src/donut-unobfuscated.jl).


---
[Robert Moss](http://web.stanford.edu/~mossr)
