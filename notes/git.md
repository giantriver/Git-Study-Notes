# Git 學習筆記
---
## 一、基本指令
> Notice :
> 1. 以下code都執行在command line
> 2. 在資料夾中點選右鍵開始Git-bash

| 指令 | 用途 |
| :--: | :---|
| git init | 建立git repository (.git子資料夾)/初始化git repo |
| git status | 查看目前狀態|
| git add <文件名>| 追蹤網gi站/將文件加入reposirory |
| git commit -m "文字"| 保存進度/存檔 |
| git log | 查看commit紀錄 |
| git remote add <自訂名稱><網址> | 增加remote |
| git remote | 列出所有remote |
| git push -u <remote名稱><branch名稱> | 上傳到GiuHub |
| git clone <網址> | 下載遠端的git repo |

## 二、搭配Vscode使用Git
> Notice : 可在資料夾的command line中使用code .(用Vscode開啟資料夾)

| 常用指令 | 用途 |
| :--: | :---|
| git reset -- <檔案名稱> | 將add完成的檔案unstage回去 |
| git checkout -- <檔案名稱>**(點選Discard Changes)**　| 將檔案回到上次commit時的狀態 |
| git reset -- soft Head~1 **(點選Undo Last Commit)** | 往前退一個commit並保留修改的部分 |

> Notice : git checkout -- <檔案名稱> 與 git reset -- soft Head~1 之比較
![compare.jpg](..\images\git\compare.jpg)

## 三、 Conflict介紹
假設有A、B兩台電腦並有相同的檔案，若A已修改檔案並且push到GitHub，則B電腦上的repo則會與GitHub上的repo有所衝突。B電腦需要先執行"git pull"並解決衝突的部分。
| 常用指令 | 用途 |
| :--: | :---|
| git pull | 將remote上的新commit抓取下來 |

> Notice :
> 1.出現conflict的檔案會出現在 "merge changes"中
> ![merge.jpg](..\images\git\merge.jpg)
> 2.解決衝突後會產生一個merge的commit
## 四、 Branch介紹
"Commit"可比喻為遊戲的存檔，而一個專案會出現多次的"Commit"。多次"Commit"形成一條線時，"Branch"可使這條線產生分支並且進行開發，使其暫時不用擔心遇到"Conflift"。當專案開發到最後，可將Branch整併為主要的線上(Master branch)，如下圖所示。
![branch.jpg](..\images\git\branch.jpg)
| 常用指令 | 用途 |
| :--: | :---|
| git checkout -b <branch名稱> | 建立新的branch並切換過去 **(點選Create New Branch)** |
| git branch | 查看電腦上的branch |
| git branch -a | 查看所有的branch(包含remote) |
| git push -u <remote名稱> HEAD | 推送當前分支至遠端repo |
## 五、 將Branch整併回Master Branch
### 方法1. 在GitHub上使用"pull request"
![pull-request.jpg](..\images\git\pull-request.jpg)
| 常用指令 | 用途 |
| :--: | :---|
### 方法2. 在自己電腦上merge之後再push

## 參考資料

<iframe width="560" height="315" src="https://www.youtube.com/embed/Zd5jSDRjWfA?si=1P4nLWiyTm4iv7hn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>