# �ۑ�U�@�摜�̓�l��

���܂ł̉ۑ�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B

�摜�̓�l�����s���B


���̔����摜  
ORG=imread('sushi.png'); % ���摜�̓���  
ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�  

![img](http://i.imgur.com/eyaPHOH.png)  

�}1 �������摜

�P�x128�����ɓ�l��  
IMG = ORG>128; % 128�ɂ���l��

![img](http://i.imgur.com/oZrYj4E.png)  

�}2 �P�x128�ɂ���l���摜

�f�B�U�@  
IMG = dither(ORG); % �f�B�U�@�ɂ���l��

![img](http://i.imgur.com/Vhd47kc.png)  

�}3 �f�B�U�@�ɂ���l���摜


�܂Ƃ�

�P�x128�ɂ��摜�̓�l���ƃf�B�U�@�ɂ��摜�̓�l�����s�����B

�f�B�U�@�ɂ���l���̕����N���ɏ����ł��Ă��邱�Ƃ��m�F�ł���B