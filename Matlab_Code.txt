clear all;
clc;
a = imread('rice.png');
p = size(a);
s = strel('square',3);
c1 = imdilate(a,s);
c2 = imerode(a,s);
figure(1),imshow(a);
title('Real Image')
figure(2),imshow(c1);
title('Dilation')
figure(3),imshow(c2);
title('Erosion')