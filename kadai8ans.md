# �ۑ�8�@���x�����O

���܂ł̉ۑ�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B

��l�����ꂽ�摜�̘A�������Ƀ��x����t����B


���摜�𔒍��̉摜�ɕϊ�����D


ORG=imread('sushi.png'); % ���摜�̓���

ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�

imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/HcmEjtv.png)

�}1�@�������摜


臒l128�œ�l������D


IMG = ORG > 128; % 臒l128�œ�l��

imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��


![img](http://i.imgur.com/uUP5HOs.png)

�}2�@臒l128�œ�l�������摜

���x�����O���s��

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % �摜�̕\��

![img](http://i.imgur.com/pbuxDIo.png)

�}3�@���x�����O����


�܂Ƃ�

�ۑ�4�̃q�X�g�O������sushi.png���S�̓I�ɔ��ڂ̉摜�ł��邱�Ƃ͊��Ɋm�F�ł��Ă���B

����䂦�A��l���ŉ摜�̂قƂ�ǂ��������Ă��܂����߁A���x�����O���s���Ɠ�l���Ŕ����Ȃ��Ă��镔���ȊO�͐��Ȃ��Ă��܂��B

���낤���ĊC�V�̖ڂ�܂���̐g�̒��̔Z�ԐF�����̗֊s���m�F�ł�����x�ł���B