# old_photos_reappear_brilliance
让你的老照片重现光彩-基于docker的容器，容器我采用的是debian，语言是python


本项目基于微软的 https://github.com/microsoft/Bringing-Old-Photos-Back-to-Life 项目做成了docker容器，不需要自己折腾各种环境、配置了，只需要有一台安装了docker的机器即可使用

使用方式：

  1、下载   
    i、百度网盘：因为容器有7.64GB，所以转存到了百度网盘，下载地址
      链接：https://pan.baidu.com/s/1z8DD8M1M17oWUGEcfgKbOA 
      提取码：5it0 
    
    下载的tar格式的镜像使用方式：
      docker import face_fix.tar face_fix:1.0
      这里导入成功后生成的image id会不一样
![](http://cdn.fologde.com/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20201217180425.png)
  
    ii、阿里云容器仓库   大小：4.7G
    registry.cn-shenzhen.aliyuncs.com/docker_study_nanxun/face_fix:1.0
    
  2、使用   
  i、新建容器
      docker run -it --name face_fix [镜像id] bash
      这里可以做一下目录映射的处理，这样，处理好的照片就可以同步到主机了
         
   ii、老照片修复   
      进入容器  docker exec -it [容器id] bash   
      切换到目录   
        cd /usr/yifang/photo_restoration
      python3.8 run.py --input_folder /usr/yifang/photo_restoration/test_images/old --output_folder /usr/yifang/photo_restoration/output --GPU -1


官方效果：   
  ![](http://cdn.fologde.com/face_pipeline.jpg)
  ![](http://cdn.fologde.com/face_fix/face.png)
  ![](http://cdn.fologde.com/face_fix/0001.jpg)
  ![](http://cdn.fologde.com/face_fix/pipeline.PNG)
  ![](http://cdn.fologde.com/face_fix/global.png)
  ![](http://cdn.fologde.com/face_fix/scratch_detection.png)
  
  
