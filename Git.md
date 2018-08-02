Command line instructions

Git global setup
git config --global user.name "xxx"
git config --global user.email "xxx@xxx.163.com"

Create a new repository
git clone git_url
cd Robot
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master

Existing folder
cd existing_folder
git init
git remote add origin git_url
git add .
git commit -m "Initial commit"
git push -u origin master

Existing Git repository
cd existing_repo
git remote add origin git_url
git push -u origin --all
git push -u origin --tags

查看用户名和地址
git config user.name
git config user.email

修改用户名和地址
git config --global user.name "your name"
git config --global user.email "your email"


