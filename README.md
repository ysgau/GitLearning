GitLearning
======

�@��: ���W ��


Git�w��
------
* [Git�U���æw��] (https://git-scm.com/downloads); (��ĳ�w�� [2.14.1](https://github.com/git-for-windows/git/releases/download/v2.14.1.windows.1/Git-2.14.1-64-bit.exe) �H�W)
* �]�w�A�ާ@Git�ɪ��ѧO�W��

		$ git config --global user.name "your name"
		$ git config --global user.email "your email"

* ����Pull�HFF (fast forward)�\��

		$ git config --global pull.ff false

�إ߱M��
------
* �إߤu�@�ؿ�

		$ mkdir projName

* ������u�@�ؿ�

		$ cd projName

* �إߥ��a�x�s�w(Local Repository)

		$ git init


�إߤ��ɨðe���Git
------

* �إߤ���

		$ echo hello > hello.txt

* �N���ɴ����Staged DB

		$ git add hello.txt
		
		//�Υ[�J�Ҧ��s�W/���ʤ�����
		$ git add .

* �T�{����ܥ��a�x�s�w, �å[�J�������椧����

		$ git commit -m "your comment"

�e��ܻ����x�s�w(Remote Repository)
------

* �]�w�s�����ݸ�Ʈw(�@����)
		$ git remote add origin <target>
		//target �i�H�O...
		//git server    => git://host/projName.git
		//github        => https://github.com/ysgau/projName.git
		//remote folder => \\host\gitProjs\projName.git

* �T�{�O�_���]�w�s�������x�s�w(�����p�ˬd)
		$ git remote -v
		origin  https://github.com/ysgau/projName.git (fetch)
		origin  https://github.com/ysgau/projName.git (push)

* �N���a�x�s�w�����, �W�Ǧܻ����x�s�w(�`�O)
		//���O git push [remote-name] [branch-name]
		$ git push origin master
