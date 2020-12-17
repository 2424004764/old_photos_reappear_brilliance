# old_photos_reappear_brilliance
让你的老照片重现光彩-基于docker的容器，容器我采用的是debian，语言是python


本项目基于微软的 https://github.com/microsoft/Bringing-Old-Photos-Back-to-Life 项目做成了docker容器，不需要自己折腾各种环境、配置了，只需要有一台安装了docker的机器即可使用

使用方式：

  1、下载
    百度网盘：因为容器有7.64GB，所以转存到了百度网盘，下载地址
      链接：https://pan.baidu.com/s/1z8DD8M1M17oWUGEcfgKbOA 
      提取码：5it0 
    
    下载的tar格式的镜像使用方式：
      docker import face_fix.tar face_fix:1.0
      这里导入成功后生成的image id会不一样
![](http://cdn.fologde.com/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20201217180425.png)
  
  2、阿里云容器仓库
    
    
