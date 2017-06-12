# NFS-Server

## Windows NFS工具
+ Windows早期提供的NFS服务器工具已经老旧没有再更新推出无法使用了, 后Windows系统有部分有NFS功能,但仅作为终端可以加载服务器端NFS共享文件夹,
新的Windows Server系列自身带有NFS服务端功能,可以开启NFS文件服务共享服务功能,但有反应中文文件会出现乱码,这是可能是windows对utf8输出不支持或支持不好的原因;

+ 现在在Windows上作NFS共享服务大部人使用HaneWin这个应用工具,有中文版, 对中文输出支持也很好,在server选项勾选启用UTF-8 character set就可以了

+ HaneWin的设置用法

  + 例如:
   * D:\AA  -name:AA      -public -readonly -range 192.168.1.158 192.168.1.199  192.168.1.200-192.168.1.254
  + D:\AA是被共享的服务器端本地磁盘分区或文件夹名
  + -name:AA是NFS共享后分享出去的名称,名称可另设
  + -public表示启用WebNFS访问,DSM挂载时必须开启该项
  + -readonly表示仅以只读方式共享
  + -range 192.168.1.xxx-192.168.1.XXX表示仅对特定IP地址开放共享
  + -alldirs允许主机在文件系统中的任意位置安装。
  + -umask：<mask>设置文件系统上的组和世界权限的umask，默认为022
  + -lowercase将所有文件名映射到小写，否则保留。
  + -exec强制访问权限为所有文件的x位。
  + -mapall：<uid> [：<gid>]将所有的Unix user-id和group-id映射到指定的user-id和group-id。
  + -maproot：<uid> [：<gid>]将Unix超级用户根映射到指定的用户标识，group-id。没有映射条目根将映射到用户和组nobody

## linux DSM 挂载NFS
+  挂载mount

+  卸载umount




