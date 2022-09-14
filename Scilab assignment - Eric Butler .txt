
function []=gussianElemination(a11, a12, a13, b1, a21, a22, a23, b2, a31, a32, a33, b3)  

x = [a11, a12, a13, b1 ; a21, a22, a23, b2 ; a31, a32, a33, b3]

x(1,:) = x(1,:) / a11

disp (x);



x(2,:) = x(2,:) - x(1,:) * a21
disp(x);


x(3,:) = x(3,:) - x(1,:) * a31
disp(x);

x(2,:) = x(2,:)  / x(2,2)
disp(x);


x(3,:) = x(3,:) - x(2,:) * x(3,2)
disp (x);

x(3,:) = x(3,:) / x(3,3)
disp(x);


disp("Z = ", x(3,4));
z=x(3,4)
disp("Y = ", x(2,4) - x(2,3) * x(3,4));
y=x(2,4) - x(2,3) * x(3,4);


disp("X = ", - x(1,2)*y - x(1,3) *z + x(1,4));


endfunction 


