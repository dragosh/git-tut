# Based of [http://nvie.com/posts/a-successful-git-branching-model]

git init

git remote add origin [repo-url]

git push -u origin master

git checkout -b develop master

git branch -a

git checkout -b feature-one develop

// Switched to branch 'develop'
git checkout develop

//The --no-ff flag causes the merge to always create a new commit object, even if the merge could be performed with a fast-forward. This avoids losing information about the historical existence of a feature branch and groups together all commits that together added the feature.

git merge --no-ff feature-one

//delete the branch after merge
git branch -d feature-one

git push origin develop

git checkout master
git merge --no-ff release-0.1
git tag -a 0.1


git checkout develop
git merge --no-ff release-0.1

git branch -d release-0.1
