#�ۑ�9�@���f�B�A���t�B���^�Ɛ�s��

���܂ł̉ۑ�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B

���f�B�A���t�B���^�[��K�p���C�m�C�Y������̌�����B


�摜�𔒍��̉摜�ɕϊ�����B

ORG=imread('sushi.png'); % ���摜�̓���

ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�

imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/SGnHxmR.png)

�}1�@�������摜

���̉摜�Ƀm�C�Y��Y�t����B

ORG = imnoise(ORG,'salt & pepper',0.02); % �m�C�Y�Y�t

imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/HiJC31m.png)

�}2�@�m�C�Y��Y�t�����摜

�������t�B���^�ŎG���������s���B

IMG = filter2(fspecial('average',3),ORG); % �������t�B���^�ŎG������

imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/2GVuc52.png)

�}3�@�������t�B���^�ŎG���������s�����摜

���f�B�A���t�B���^�ŎG���������s���B

IMG = medfilt2(ORG,[3 3]); % ���f�B�A���t�B���^�ŎG������

imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/iFb9wbU.png)

�}4�@���f�B�A���t�B���^�ŎG���������s�����摜


������Ńt�B���^��݌v���A�����K�p����

f=[0,-1,0;-1,5,-1;0,-1,0]; % �t�B���^�̐݌v

IMG = filter2(f,IMG,'same'); % �t�B���^�̓K�p

imagesc(IMG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/qs3FeS3.png)

�}5�@�t�B���^��K�p�����摜


�܂Ƃ�

�������t�B���^�ƃ��f�B�A���t�B���^�ɂ��m�C�Y�̏�����̌������B

�������t�B���^�͑����m�C�Y���������Ă͂��邪�F�ʂ͌��摜�ɍł��߂��B

���΂ɁA���f�B�A���t�B���^�͐F�ʂ͌��摜�������邢���A�m�C�Y�͂قƂ�ǌ��󂯂��Ȃ��B

�����̋��߂�摜���H�ɉ����ăt�B���^���g�������邱�Ƃ��厖�ł���ƌ�����B