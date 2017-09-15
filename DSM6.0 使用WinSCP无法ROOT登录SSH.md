# DSM6.0 使用WinSCP无法ROOT登录SSH

## 简单教程      
进入putty    
第一步 输入账号 密码（我是用admin进入-成功修改）   
第二步 确定是admin@xxx 然后输入
  
    sudo su -

再次输入密码 就会变root@xxx 确定一下    
第三步 输入(xxx是你root的密码 我是放跟admin一样） 
  
    synouser --setpw root xxx

就成功了 这样你就可以进winscp 用root登入    
（如果是要装tr web界面的 可以不要退出 输入killall transmission-daemon 这是系统停用transmission)可以直接输入 然后跟着网上步骤

提醒下 remote gui    
5.01-有中文 5.03-没有中文    
需要中文可以安装5.01   
