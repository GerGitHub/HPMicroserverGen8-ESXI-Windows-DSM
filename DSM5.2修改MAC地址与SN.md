# DSM5.2修改MAC地址与SN      

### 本例是以VMDK分区镜像文件方式安装虚拟DSM, ESXI中建立或复制多个DSM时修改MAC和SN     

+ 1. 先把已安装完成的DSM在ESXI中导出，会有3个文件.ovf/*0.vmdk/*1.vmdk ，*0.vmdk可能是主板硬件配置虚拟镜文件，可用ZIP查看其中的文件，主要是syslinux.cfg
   
+ 2. 把网上原下载的DSM安装引导分区镜像文件XPEnoboot_DS3615xs_5.2-5967.1.vmdk,用DiskGenius加载硬盘镜像文件，其中的文件与1中的文件结构一致，主要是syslinux.cfg内容不同

+ 3. 在DiskGenius中把原有的syslinux.cfg导出并且修改，主要修改SN=xxxxxx 和 MAC1=xxxxxx, 算号获取新MAC与SN, DiskGenius中删除原有syslinux.cfg，并重新写入新改的syslinux.cfg
，保存关闭回载镜像文件    

+ 4. 在ESXI新建一个DSM虚拟机，选择以OVF方式新建，然后导入1中导出的3个文件，完成新DSM虚拟机部署    

+ 5. 在ESXI中编辑新建DSM, 删除原有引导分区, 24M的那个分区； 回到ESXI存储管理，在文件浏览中上3修改后何存的镜像文件，注意先改一下文件名     

+ 6. 在ESXI中编辑新建DSM, 把网卡MAC也修改为新的MAC地址       

OK, 新的DSM建立完毕；
