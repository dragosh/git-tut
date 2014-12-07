# Based of [http://nvie.com/posts/a-successful-git-branching-model]

git init
git remote add origin [repo-url]
git push -u origin master
git checkout -b develop master
git branch -a
git checkout -b feature-one develop

// Switched to branch 'develop'
git checkout develop

git merge --no-ff feature-one

//delete the branch after merge
git branch -d feature-one
