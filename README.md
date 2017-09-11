GitLearning
======

作者: 狐狸 高


Git安裝
------
* [Git下載並安裝] (https://git-scm.com/downloads); (建議安裝 [2.14.1](https://github.com/git-for-windows/git/releases/download/v2.14.1.windows.1/Git-2.14.1-64-bit.exe) 以上)
* 設定你操作Git時的識別名稱

		git config --global user.name "your name"
		git config --global user.email "your email"

* 關閉Pull以FF (fast forward)功能

		git config --global pull.ff false

建立專案
------
* 建立工作目錄

		mkdir projName

* 切換到工作目錄

		cd projName

* 建立Local Repository

		git init


建立文檔並送交至Git
------

* 建立文檔

		echo hello > hello.txt

* 將文檔提交更新到儲存庫

		git add hello.txt
		//加入所有新增/異動之文檔
		git add .

