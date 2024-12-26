
# 1. 初始化一個 Git repository
你可以在現有的專案目錄中初始化一個 Git repository。
```
git init
```
這樣會在當前目錄下建立一個 .git 資料夾，用來追蹤版本歷史。

---
# 2. 配置 Git
在使用 Git 前，你應該設定你的用戶名稱和郵件，這些資訊會被記錄在每次commit中。
```
git config --global user.name "你的名字"
git config --global user.email "你的郵箱"
```
---
# 3. 基本操作
## - 查看 Git 的狀態
使用 git status 可以查看目前目錄中有什麼變更（尚未commit的檔案）。
```
git status
```
## - 新增檔案到 Git 的追蹤清單
使用 git add 把檔案加入 Git 的追蹤清單，準備commit。
```
git add <檔案名>
```
如果想要把所有變更的檔案都加到追蹤清單中，可以用 .
```
git add .
```
## - commit更改
使用 git commit 來commit已經加到追蹤清單中的檔案，並附上commit訊息。
```
git commit -m "你的commit訊息"
```
## - 查看commit紀錄
使用 git log 查看commit歷史紀錄。
```
git log
```
# 4. Git 分支操作
Git 的分支讓你可以在不同的工作流中同時開發，不會互相干擾。

## - 查看所有分支
使用 git branch 來查看目前所有的分支，並標註當前所在的分支。
```
git branch
```
## - 創建新分支
使用 git branch 創建一個新的分支。
```
git branch <新分支名稱>
```
## - 切換分支
使用 git checkout 切換到其他分支。
```
git checkout <分支名稱>
```
## - 合併分支
當你完成某個分支的開發，可以將它合併到主分支（例如：master 或 main）
```
git checkout main   # 切換到主分支
git merge <分支名稱> # 合併分支
```
# 5. 遠端repository
遠端repository讓你可以和其他人協作，將本地repository與遠端repository（如 GitHub）同步。

## - 連接遠端repository
將本地repository和遠端repository連接，通常這是遠端Git repository的 URL。
```
git remote add origin <遠端repositoryURL>
```
## - 查看遠端repository
查看已設定的遠端repository：
```
git remote -v
```
## - 推送本地更改到遠端repository
將本地commit推送到遠端repository的某個分支。
```
git push origin <分支名稱>
```
## - 拉取遠端repository的更改
從遠端repository拉取最新的更改。
```
git pull origin <分支名稱>
```
# 6. 撤銷更改
有時候你可能會犯錯或不小心commit了錯誤的內容。Git 提供了多種方式來撤銷變更。

## - 撤銷未commit的變更（會丟失未commit的修改）：
```
git checkout -- <檔案名>
```
## - 撤銷最近的commit（保留變更但不commit）：
```
git reset --soft HEAD^
```
