# git对一个目录进行版本控制
+ 进入要管理的文件夹
+ 执行初始化命令  
  ```
    git init
  ```
+ 管理目录下的文件状态  
  ```
    git status    
    注：新增的文件和修改过后的文件都是红色
  ```   
+ 管理指定文件(红变绿)
  ```
    git add 文件名  
    git add .
  ```
+ 个人信息配置：用户名、邮箱(最初执行一次)
  ```
    git config --global user.email "you@example.com"  
    git config --global user.name "Your Name"
  ``` 
+ 生成版本
  ```
    git commit -m '描述信息'
  ```
+ 查看版本记录
  ```
    git log
  ```
- 版本回滚  
  1. 回滚到之前的版本
  ```
    git log //查找版本号
    git reset --hard 版本号
  ``` 
  2.  回滚到之后的版本
  ```
    git reflog
    git reset --hard 版本号
  ```

- 查看分支
```
  git branch
```
- 创建分支
```
  git branch 分支名称
```
- 切换分支
```
  git checkout 分支名称
```
- 分支合并(可能产生冲突)
```
  git merge 要合并的分支
  注意： 切换分支再合并
```
- 删除分支
```
  git branch -d 分支名称
```
# Github托管

  1. 给远程仓库起名
   ```
   git remote add origin 远程仓库地址
   ```
  2. 向远程推送代码
   ```
   git push -u origin 分支
   ```
  3. 克隆远程仓库代码
  ```
  git clone 远程仓库地址
  ```
  4. 切换分支
   ```
   git checkout 分支
   ```
  
## 设备1
  1. 切换到dev分支进行开发  
   `git checkout dev`
  2. 把master分支合并到dev[仅第一次]  
   `git merge master`
  3. 修改代码
  4. 提交代码
   ```
   git add .
   git commit -m 'xx'
   git push origin dev
   ```

## 设备2
  1. 切换到dev分支开发  
  `git checkout dev`
  2. 拉代码
  `git pull origin dev`  
  3. 继续开发
  4. 提交代码
   ```
   git add .
   git commit -m 'xx'
   git push origin dev
   ```

