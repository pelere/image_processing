�ۑ�1:�W�{���Ԋu�Ƌ�ԉ𑜓x


�W���摜�usushi.png�v�����摜�Ƃ���D

ORG=imread('sushi.png'); % ���摜�̓���

imagesc(ORG); axis image; % �摜�̕\��

�ɂ���ĕ\�����ꂽ���摜�͐}1�̂悤�ɂȂ����D

![img](http://i.imgur.com/AJkIVUy.png)

�}1�@���摜

���摜��1/2�ɃT���v�����O����ɂ́C�摜��1/2�ɏk��������C2�{�Ɋg�傷��D�g�傷��ۂɂ́C�P����Ԃ��邽�߂�box�I�v�V�����𗘗p����D

IMG = imresize(ORG,0.5); % �摜�̏k��

IMG2 = imresize(IMG,2,'box'); % �摜�̊g��

imagesc(IMG2); axis image; % �摜�̕\��

1/2�T���v�����O�̌��ʂ�}2�Ɏ����D

![img](http://i.imgur.com/NqoiUzR.png)

�}2 1/2�T���v�����O

���l�ɁC1/4�T���v�����O������ɂ́C1/2�T���v�����O�����摜��1/2�ɏk��������C2�{�Ɋg�傷�邱�Ƃŉ\�ł���D

IMG = imresize(IMG,0.5); % �摜�̏k��

IMG2 = imresize(IMG,4,'box'); % �摜�̊g��

imagesc(IMG2); axis image; % �摜�̕\��

1/4�T���v�����O�̌��ʂ�}3�Ɏ����D

![img](http://i.imgur.com/VNb15HU.png)

�}3 1/4�T���v�����O

![img](http://i.imgur.com/Bvetc41.png)

�}4 1/8�T���v�����O

![img](http://i.imgur.com/OaxA1nz.png)

�}5 1/16�T���v�����O


�܂Ƃ�

���̂悤�ɃT���v�����O�����傫���Ȃ�ƁC���U�C�N��̃T���v�����O�c�݂���������D