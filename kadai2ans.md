# �ۑ�Q�@�K�����Ƌ^���֊s
�Q�K���C�S�K���C�W�K���̉摜�𐶐�����D

�ۑ�1�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B

�܂��A�摜���甒���摜�𐶐�����B

clear; % �ϐ��̃I�[���N���A  
ORG=imread('view.png'); % ���摜�̓���  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % �摜�̕\��  

![img](http://i.imgur.com/S9n36Rv.png)  
�}1 �����摜


2�K���摜�̐������s���B
% �Q�K���摜�̐���  
IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

![img](http://i.imgur.com/ueC87F2.png)  
�}2 2�K��

4�K���摜�̐������s���B
% �S�K���摜�̐���  
IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
![img](http://i.imgur.com/0lhmmxz.png)  
�}3 4�K��

8�K���摜�̐������s���B
8�K���摜�𐶐�����v���O�����́A2�K���A4�K���摜�����̃T���v���v���O��������ȉ��̃v���O�����ł���ƍl�����B
% �W�K���摜�̐���  
IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>96;  
IMG3 = ORG>128;  
IMG4 = ORG>160;  
IMG5 = ORG>192;  
IMG6 = ORG>224;  
IMG = IMG0 + IMG1 + IMG2 + IMG3 + OMG4 + IMG5 + IMG6;  
![img](http://i.imgur.com/SRrvm3Q.png)  
�}4 8�K��

�܂Ƃ�
�Q�K���C�S�K���C�W�K���̉摜�𐶐������B
�K�����ɉ�����8�K���A4�K���A2�K���̏��ɉ摜���N���ɂȂ��Ă��邱�Ƃ��m�F�ł���B  
