# uts_pengolahan_citra
konversi RGB

![image](https://user-images.githubusercontent.com/56398559/117011157-c079e880-ad17-11eb-8f73-5fd78072043a.png)

![image](https://user-images.githubusercontent.com/56398559/117011238-d5567c00-ad17-11eb-847a-4f5870a146fc.png)

kodingan :

[filename, pathname] = uigetfile({'*.png','*.png'});
gambar1 = imread([pathname, filename]);

axes(handles.axes1);
imshow(gambar1);

R = gambar1(:,:,1);
G = gambar1(:,:,2);
B = gambar1(:,:,3);

Red = cat(3,R,G*0,B*0);
Green = cat(3,R*0,G,B*0);
Blue = cat(3,R*0,G*0,B);

axes(handles.axes2);
imshow(Red);

axes(handles.axes3);
imshow(Green);

axes(handles.axes4);
imshow(Blue);

