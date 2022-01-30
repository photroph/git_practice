Git commands usage memo


## addする前の変更をstageの内容に戻す
git restore <file>..." to discard changes in working directory

## stageにaddした変更を取り消す
git restore --staged <file>

## 直前のcommitをstageの内容でやり直す
stageに変更を反映した状態で
!!! remoteにpushしたものは使わない
git commit --amend

## branch
branchは単にcommitを指すポインタ
git branchでリスト表示，-aでリモートも表示
git checkoutでHEADの参照先branchを切り替える

### merge
fast forward merge ... pointerがbranchの先側に移動するだけのmerge
auto merge ... 新たにcommitが作成され，parentが2つできるmerge


# REMOTE
pull = fetch + merge (*
* pullすると現在自分がいるbranchに対象remote repositoryの内容を反映する
fetch ... remoteの内容をlocalのrepositoryに読み込む
mergeでfetchしたbranchをlocalのworktreeに反映できる