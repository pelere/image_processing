# �ۑ�3�@臒l����


���܂ł̉ۑ�Ɠ������W���摜�usushi.png�v�����摜�Ƃ���B

臒l��4�p�^�[���ݒ肵�A臒l���������摜�������B

�܂��A�摜�𔒍��̉摜�ɕϊ�����B


ORG=imread('sushi.png'); % ���摜�̓���

ORG= rgb2gray(ORG); % �J���[�摜�𔒍��Z�W�摜�֕ϊ�

imagesc(ORG); colormap(gray); colorbar; % �摜�̕\��



![img](http://i.imgur.com/PTeOGya.png)

�}1�@�������摜

�P�x�l��64�ȏ�̉�f��1�A���̑���0�ɕϊ�����B


IMG = ORG > 64; 

imagesc(IMG); colormap(gray); colorbar;


���ʂ͐}2�̂悤�ɂȂ����B

![img](http://i.imgur.com/p4ZrN1A.png)

�}2�@�P�x�l��64�ɐݒ肵���摜

�P�x�l��96�ȏ�̉�f��1�A���̑���0�ɕϊ�����B


IMG = ORG > 96;

imagesc(IMG); colormap(gray); colorbar;


���ʂ͐}3�̂悤�ɂȂ����B

![img](http://i.imgur.com/GW5u1YV.png)

�}3�@�P�x�l��96�ɐݒ肵���摜


�P�x�l��128�ȏ�̉�f��1�A���̑���0�ɕϊ�����B



IMG = ORG > 128;

imagesc(IMG); colormap(gray); colorbar;


���ʂ͐}4�̂悤�ɂȂ����B

![img](http://i.imgur.com/aZmSBWw.png)

�}4�@�P�x�l��128�ɐݒ肵���摜

�P�x�l��192�ȏ�̉�f��1�A���̑���0�ɕϊ�����B


IMG = ORG > 192;

imagesc(IMG); colormap(gray); colorbar;


���ʂ͐}5�̂悤�ɂȂ����B

![Imgur](http://i.imgur.com/sdYJ69b.png)

�}5�@�P�x�l��192�ɐݒ肵���摜

�܂Ƃ�

���E�l�ȉ��̋P�x��0�ƂȂ邽�߁A�P�x�̋��E�l���グ�Ă����ƋP�x0�̉�f�������A���X�ɉ摜�S�̂������ω����Ă������Ƃ��m�F�ł���B