# Smooth-Cubic-Bezier-curves-throught-points
An article to learn how to generate the control points of a bezier curve with the condition of be 2 times smooth and through a set of prescribed points.

What a bezier curve is : https://en.wikipedia.org/wiki/B%C3%A9zier_curve

The cubic bezier curve is given by: B(t)=(1-t)^3*P0 + 3*(1-t)^2*t*P1+3(1-t)*t^2*p2+t^3P3; 0<=t<=1;

P0 and P4 are points given and we have to calculate P1 and P2

notation: the i spline in the curve B[i](t),P[i,0]

The derivative of the cubic Bézier curve with respect to t is B'(t)=3(1-t)^2*(P1-P0)+6(1-t)*t*(P2-P1)+3t^2*(P3-P2);

and de second derivative B''(t)=6(1-t)(P2-2*P1+P0)+6t(p3-2*p2+p1);

In orther to make the union of the splines 2 times smooth B[i-1](1)=B[i](0); B'[i-1](1)=B'[i](0); B''[i-1](1)=B''[i](0); 
