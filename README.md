# Gitの基本操作方法

## ローカルリポジトリの作成　※作成したいディレクトリ内で実行
```bash
git init
```

## Githubと接続
```bash
git config --global user.name "ShuheiKuraoka"
git config --global user.email "92.sky.428@gmail.com"
```

## リモートレポジトリとローカルリポジトリを紐付け
```bash
git remote add origin https:/github.com/ShuheiKuraoka/local-test.git

# リモートの確認と削除
git remote -v
git remote rm origin
```

## 変更を反映しコミット→プッシュ
```bash
git add app.py requirements.txt 
git commit -m "メッセージ"
git push origin master
# ローカルブランチ「master」を、リモートブランチ「master」に push 
git push origin master:master
# リモートブランチ「tmp」の削除
git push origin :tmp

```
## リポジトリのcloneからブランチを作成しpushまで
```bash
# `owner/repo` を変更
git clone https://github.com/owner/repo.git
# `repo`ディレクトリへ移動
cd repo
# 新しいブランチを作成して変更を保存
git branch my-branch
# ブランチの切り替え
git checkout my-branch
# 変更をステージング
git add file1.md file2.md
# 変更をコミット
git commit -m "my snapshot"
# pushして変更をGithubに反映
git push --set-upstream origin my-branch
```
