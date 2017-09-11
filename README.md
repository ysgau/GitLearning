Git Learning
======

作者: 狐狸 高


Git安裝
------
* [Git下載並安裝](https://git-scm.com/downloads); (建議安裝 [2.14.1](https://github.com/git-for-windows/git/releases/download/v2.14.1.windows.1/Git-2.14.1-64-bit.exe) 以上)
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

		//參考指令: git remote add <remote-name> <target>
		$ git remote add origin https://github.com/ysgau/projName.git
		
		//target 可以是...
		//   git server => git://host/projName.git
		//       github => https://github.com/ysgau/projName.git
		//remote folder => \\host\gitProjs\projName.git

* 確認是否有設定連結遠端儲存庫(視情況檢查)

		$ git remote -v
		origin  https://github.com/ysgau/projName.git (fetch)
		origin  https://github.com/ysgau/projName.git (push)

* 將本地儲存庫的資料, 上傳至遠端儲存庫(總是)

		//參考指令: git push [remote-name] [branch-name]
		$ git push -u origin master

複製遠端儲存庫的專案
------

* 複製遠端儲存庫的專案

		//參考指令: git clone <source> [localFolderName]
		$ git clone https://github.com/ysgau/projName.git myProj

更新來自於遠端儲存庫的文檔
------

* 更新來自於遠端儲存庫的文檔
		//參考指令: git pull [remote-name] [branch-name]
		$ git pull origin master
		
		//[資訊] git pull == git fetch + git merge

退回指定版本
------

* 退回前一版

		//參考指令: git reset HEAD~
		$ git reset HEAD~
		
		//退回時若要捨棄所有更改(與新增)文檔, 則多增加 --hard 參數
		$ git reset HEAD~ --hard

* 退回指定版本

		//利用git reflog指令, 調閱出所有進版檔頭資訊
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
		
		//指定欲回版本的檔頭 (以回到"v7"版為例)
		$ git reset 8dc8afd 

		//若沒有使用--hard, 且要"將未捨棄的文檔併入此版本"的話, 可用 "git add ."
		$ git add .