配置:
小米游戏本7代   
i5 7300hq 
显卡1060(独显不能用)  
用[这个EFI文件](https://github.com/chengziqaq/mac/raw/master/clover/CLOVER-2020-5-9%E5%B0%8F%E7%B1%B3%E6%B8%B8%E6%88%8F%E6%9C%AC15.67%E4%BB%A3i57300hqmacos10.15.3%E5%BC%80%E6%9C%BA20s.zip)  
蓝牙不可用  
系统镜像用这个[黑果小兵](https://blog.daliansky.net/macOS-Catalina-10.15.4-19E266-Release-version-with-Clover-5107-original-image-Double-EFI-Version-UEFI-and-MBR.html)
# 添加双系统启动,在win下使用easyefi,新建启动项,具体谷歌
# 2020/5/4新加固态硬盘双系统中.mac系统启动失败解决办法
问题描述:先从机械硬盘里用时间机器恢复mac系统到SSDmac分区,再安装win10系统到SSDwin10分区,  
结果去win10里面配置了一下电脑(包括更新win系统,显卡驱动),玩了玩游戏,  
给机械硬盘加了个efi分区(因为想分一个机械硬盘的区来备份mac,而备份mac需要格式化那个分区,而格式化需要那个盘有efi分区),再去启动mac,发现进不去,机械硬盘成了硬盘1(在win10下看到的)  
但是能用u盘启动,试了重新将u盘里能正确启动mac系统+win10系统的clover文件重新复制到了500g固态硬盘EFI分区里(即clover引导文件和win10的引导文件位于500g固态  
的efi分区下,为同级目录),多次尝试,依然不能启动,推测是win10更新了什么东西限制了mac系统的启动,或者因为加了机械硬盘的efi分区?,具体咋也不清楚.  
## 解决:clover引导文件放在了机械硬盘的efi分区里面,win的efi文件放在了固态里面,从机械硬盘里启动clover,进入之后双系统能正常启动  
