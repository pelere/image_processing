# �ۑ�10 �摜�̃G�b�W���o

���܂ł̉ۑ�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B


�G�b�W���o��̌�����B


�܂��C�摜�𔒍��̉摜�ɕϊ�����D

ORG=imread('sushi.png'); % ���摜�̓���

ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�

imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��

![img](http://i.imgur.com/VcS8wWB.png)

�}1�@�������摜


�v���E�B�b�g�@�̃G�b�W���o���s���B

IMG = edge(ORG,'prewitt'); % �G�b�W���o�i�v���E�B�b�g�@�j

imagesc(IMG); colormap('gray'); colorbar;% �摜�\��


![img](http://i.imgur.com/23lvsVg.png)

�}2�@�v���E�B�b�g�@�ɂ��G�b�W���o�̌���

�\�x���@�ɂ��G�b�W���o���s���B

IMG = edge(ORG,'sobel'); % �G�b�W���o�i�\�x���@�j

imagesc(IMG); colormap('gray'); colorbar;% �摜�\��

![img](http://i.imgur.com/WmDRtoA.png)

�}3�@�\�x���@�ɂ��G�b�W���o�̌���

�L���j�[�@�ɂ��G�b�W���o���s��

IMG = edge(ORG,'canny'); % �G�b�W���o�i�L���j�[�@�j

imagesc(IMG); colormap('gray'); colorbar;% �摜�\��

![img](http://i.imgur.com/CFVPMPy.png)

�}4�@�L���j�[�@�ɂ��G�b�W���o�̌���


�܂Ƃ�

�v���E�B�b�g�@�A�\�x���@�A�L���j�[�@��3�̕��@�ɂ��G�b�W���o��̌������B

�����̌��ʂ��r����B

�v���E�B�b�g�@�ƃ\�x���@�̈Ⴂ�͍���̉摜����͂��܂茩�󂯂��Ȃ��B

����A�v���E�B�b�g�@�ƃ\�x���@����ɗ֊s�����𒊏o���Ă���̂ɑ΂��A�L���j�[�@�͗֊s�Ƃ��̓����Ɏ���܂Œ��o���s���Ă���ƌ��󂯂���B

����̌��摜�ł͎��i���ʂ̖ؖڂ𒊏o���悤�Ƃ��Ă��邽�߂ɍr�������Ă��邪�A���̉摜�A���ɔw�i�̗v�f�̔����摜�ł͂���3�̒��ŃL���j�[�@���ł��ǂ����o���s������@�ł���ƍl������B