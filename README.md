# git-strawberry

# Plain Dosa
git add .;git commit -m"plain dosa started ,dosa batter added";git push origin plain-strawberry
git log --one-line
git cat-file -p <commit>
ex: git cat-file -p a32def

* Merge Commit is a special commit which has 2 parents
* Other commits has only 1 parent

* Merge vs Rebase ?
a) merge creates extra commit called merge commit, Rebase does not create extra commit
b) merge preserves the history , rebase does not preserve the history
c) Rebase rewrites the history, it will change commit id.
d) Rebase has linear history, merge has circular history

when to use Merge vs Rebase ?
* if a branch is shared among multiple members, if you want to preserve the history, go for merge. Long releases, waterfall model
* if it is vigirous agile or microservices development, usually a branch is owned by single person , then go for rebase..



#karam Dosa
* Dosa batter
* Errakaram

- Merge Conflicts
* git checkout main; git pull
* git checkout egg-dosa-ramesh
* git merge main
* sit & resole conflicts
* git commit <resolved conflicts>

### Branching Strategy