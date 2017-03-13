先前在使用gitlfow的时候不注意，合并代码导致分支丢失，结果一个个类比较，走了很多的弯路。要吸取教训，以后不犯同样的错误。
1. 使用git flow 初始化一个git库 
·git flow init·

2.开启一个新的分支 这个操作创建了一个基于'develop'的特性分支，并切换到这个分支之下。
`git flow feature start featurename`

3. 很关键的一步:当别人去develop更新合并了代码之后，你不小心结束了代码就会出现新旧代码的合并问题、
首先 `git checkout develop` 然后 `git pull origin develop`将代码更新到最新 

4.最后结束分支 
`git flow feature finish featurename`