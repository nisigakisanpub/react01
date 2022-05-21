# React を 脱 create-react-app でやってみた

### workspace01_seed
React with create-react-app（脱 create-react-app）＋ Typescript で SPA 作成

### workspace02_seed
workspace04 の成果物を Heroku へデプロイ


### フォルダ内に submodule が含まれる場合のこと
- git add でこのメッセージ
```
warning: adding embedded git repository: workspace05
hint: You've added another git repository inside your current repository.
hint: Clones of the outer repository will not contain the contents of
hint: the embedded repository and will not know how to obtain it.
hint: If you meant to add a submodule, use:
hint:
hint:   git submodule add <url> workspace05
hint:
hint: If you added this path by mistake, you can remove it from the
hint: index with:
hint:
hint:   git rm --cached workspace05
hint:
hint: See "git help submodule" for more information.
nisigaki@AMD-win11-64:~/python01$
```

- なぜなら、workspace05 は git 管理下にあるから
```
nisigaki@AMD-win11-64:~/python01/workspace05$ git remote -v
heroku  https://git.heroku.com/morning-peak-09108.git (fetch)
heroku  https://git.heroku.com/morning-peak-09108.git (push)
```

- そこで
```
git submodule add https://git.heroku.com/morning-peak-09108.git workspace05
```
