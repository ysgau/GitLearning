GitLearning
======

作者: 狐狸 高


Git安裝
------
* [Git下載並安裝] (https://git-scm.com/downloads); (建議安裝 [2.14.1](https://github.com/git-for-windows/git/releases/download/v2.14.1.windows.1/Git-2.14.1-64-bit.exe) 以上)
* 設定你操作Git時的識別名稱

		$ git config --global user.name "your name"
		$ git config --global user.email "your email"

* 關閉Pull以FF (fast forward)功能

		$ git config --global pull.ff false

建立專案
------
* 建立工作目錄

		$ mkdir projName

* 切換到工作目錄

		$ cd projName

* 建立本地儲存庫(Local Repository)

		$ git init


建立文檔並送交至Git
------

* 建立文檔

		$ echo hello > hello.txt

* 將文檔提交到Staged DB

		$ git add hello.txt
		
		//或加入所有新增/異動之文檔
		$ git add .

* 確認提交至本地儲存庫, 並加入此次提交之註釋

		$ git commit -m "your comment"

送交至遠端儲存庫(Remote Repository)
------

* 設定連結遠端資料庫(一次性)
		$ git remote add origin <target>
		//target 可以是...
		//git server    => git://host/projName.git
		//github        => https://github.com/ysgau/projName.git
		//remote folder => \\host\gitProjs\projName.git

* 確認是否有設定連結遠端儲存庫(視情況檢查)
		$ git remote -v
		origin  https://github.com/ysgau/projName.git (fetch)
		origin  https://github.com/ysgau/projName.git (push)

* 將本地儲存庫的資料, 上傳至遠端儲存庫(總是)
		//指令 git push [remote-name] [branch-name]
		$ git push origin master
