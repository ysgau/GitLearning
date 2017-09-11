Git Learning
======

�@��: ���W ��


Git�w��
------
* [Git�U���æw��](https://git-scm.com/downloads); (��ĳ�w�� [2.14.1](https://github.com/git-for-windows/git/releases/download/v2.14.1.windows.1/Git-2.14.1-64-bit.exe) �H�W)
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

		//�Ѧҫ��O: git remote add <remote-name> <target>
		$ git remote add origin https://github.com/ysgau/projName.git
		
		//target �i�H�O...
		//   git server => git://host/projName.git
		//       github => https://github.com/ysgau/projName.git
		//remote folder => \\host\gitProjs\projName.git

* �T�{�O�_���]�w�s�������x�s�w(�����p�ˬd)

		$ git remote -v
		origin  https://github.com/ysgau/projName.git (fetch)
		origin  https://github.com/ysgau/projName.git (push)

* �N���a�x�s�w�����, �W�Ǧܻ����x�s�w(�`�O)

		//�Ѧҫ��O: git push [remote-name] [branch-name]
		$ git push -u origin master

�ƻs�����x�s�w���M��
------

* �ƻs�����x�s�w���M��

		//�Ѧҫ��O: git clone <source> [localFolderName]
		$ git clone https://github.com/ysgau/projName.git myProj

��s�Ӧ۩󻷺��x�s�w������
------

* ��s�Ӧ۩󻷺��x�s�w������
		//�Ѧҫ��O: git pull [remote-name] [branch-name]
		$ git pull origin master
		
		//[��T] git pull == git fetch + git merge

�h�^���w����
------

* �h�^�e�@��

		//�Ѧҫ��O: git reset HEAD~
		$ git reset HEAD~
		
		//�h�^�ɭY�n�˱�Ҧ����(�P�s�W)����, �h�h�W�[ --hard �Ѽ�
		$ git reset HEAD~ --hard

* �h�^���w����

		//�Q��git reflog���O, �վ\�X�Ҧ��i�����Y��T
		$ git reflog
		5b390d9 (HEAD -> master, origin/master) HEAD@{0}: commit: markdown v10
		2b911b6 HEAD@{1}: commit: markdown v9
		03eda0f HEAD@{2}: commit: markdown v8
		8dc8afd HEAD@{3}: commit: markdown v7
		5e7415e HEAD@{4}: commit: markdown v6
		3931199 HEAD@{5}: commit: markdown v5
		7fb610b HEAD@{6}: commit: markdown v4
		c8b1515 HEAD@{7}: commit: markdown v3
		60281de HEAD@{8}: commit: markdown t2
		47d1206 HEAD@{9}: commit: markdown test
		8523185 HEAD@{10}: commit (initial): frist commit
		
		//���w���^���������Y (�H�^��"v7"������)
		$ git reset 8dc8afd 

		//�Y�S���ϥ�--hard, �B�n"�N���˱󪺤��ɨ֤J������"����, �i�� "git add ."
		$ git add .