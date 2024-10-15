# GitTools

CopyName
echo $(echo $filename | cut -d . -f1) | clip

撤销commit
git reset --soft HEAD^

本地忽略跟踪
git update-index --assume-unchanged ${file}

取消所有本地忽略
git ls-files -v | grep '^h' | awk '{print $2}' |xargs git update-index --no-assume-unchanged  

显示本地忽略跟踪文件
git ls-files -v | grep '^h\ '
