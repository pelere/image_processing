# �ۑ�7�@�_�C�i�~�b�N�����W�̊g��

���܂ł̉ۑ�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B

��f�̃_�C�i�~�b�N�����W���O����Q�T�T�ɂ���B


���̔����摜  
ORG=imread('sushi.png'); % �摜�̓ǂݍ��� 
ORG= rgb2gray(ORG); % �����Z�W�摜�ɕϊ�
  
![img](http://i.imgur.com/BfYpzQJ.png)  

�}1 �������摜

imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��

![img](http://i.imgur.com/HW1iJ3F.png)  

�}2 ���摜�̃q�X�g�O����

ORG = double(ORG);  
mn = min(ORG(:)); % �Z�x�l�̍ŏ��l���Z�o
mx = max(ORG(:)); % �Z�x�l�̍ő�l���Z�o  
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��


![img](http://i.imgur.com/ijBjPhB.png)  

�}3 �_�C�i�~�b�N�����W�ύX�̌���

ORG = uint8(ORG);  
imhist(ORG); % �Z�x�q�X�g�O�����𐶐��A�\��

![img](http://i.imgur.com/sPcgXMK.png)  

�}4 �ύX��̃q�X�g�O����


�܂Ƃ�

uint8��8bit�����Ȃ������ւ̕ϊ����s���֐��ł���B  

8bit�ł͒l��0�`255�܂ł͈̔͂���邽�߁A�K�����̒l�����B

�܂�ORG�̐����𐳂̏�Ԃɂ��Ă���B

