####  一、python+jira的使用

（1）安装jira模块：pip install jira。

（2）导入jira：from jira import JIRA

（3）和jira服务器建立连接：

​	jira = JIRA('http://localhost/jira/',basic_auth=('username', 'password'))

（4）创建issue

（5）修改issue

（6）查询issues

（7）获取特定issue



```
from jira import JIRA

jira = JIRA('https://jira.atlassian.com')

issue = jira.issue('JRA-9')
print issue.fields.project.key             # 'JRA'
print issue.fields.issuetype.name          # 'New Feature'
print issue.fields.reporter.displayName    # 'Mike Cannon-Brookes [Atlassian]'
```
### 语法知识记录

### 字符串前加 u

后面字符串以 Unicode 格式 进行编码，一般用在中文字符串前面，防止因为源码储存格式问题，导致再次使用时出现乱码。