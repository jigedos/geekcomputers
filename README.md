不懂java代码，在开源项目中做一些常见的小修改。 改APP名字，版本号，替换app图标，替换背景图片，内置源。共存（com.github.tvbox.osc）。

![image](https://user-images.githubusercontent.com/87001834/193199842-ccf4a5ff-ac2b-4153-ba1e-5a7ce52860a0.png)

改APP版本号:TVBoxOS-junlao/app/build.gradle 　　　　　　versionName '2.0.0'

![image](https://user-images.githubusercontent.com/87001834/193199911-0df430c2-3364-4b6d-b9bc-a66baf2fd417.png)
![image](https://user-images.githubusercontent.com/87001834/193199944-1bbf53dd-f9f2-4c61-917b-616fe4fd7c4a.png)
![image](https://user-images.githubusercontent.com/87001834/193200018-4c134273-bee9-41dc-ab17-27d1c24345d0.png)

调整设置画面选项的位置方法：打开，两块复制调换一下就行。

![image](https://user-images.githubusercontent.com/87001834/193200047-24d9d5e1-79c8-4369-ba4c-53eea71352f9.png)

修改内置源

俊老仓库打开下面,第83行 https://github.com/dabbing2019/TVBoxOS/blob/main/app/src/main/java/com/github/tvbox/osc/api/ApiConfig.java

takagen99大佬仓库 改这里;app/src/main/res/values-zh/strings.xml

修改默认缩略图、硬解、dns 地址：

https://github.com/dabbing2019/TVBoxOS/blob/main/app/src/main/java/com/github/tvbox/osc/base/App.java

代码

@@ -53,9 +53,19 @@ private void initParams() {

   if (!Hawk.contains(HawkConfig.PLAY_TYPE)) 
    
    {
        Hawk.put(HawkConfig.PLAY_TYPE, 1);
        
    }
    
    //自定义默认配置-硬解-安全dns-缩略图
    
    if (!Hawk.contains(HawkConfig.IJK_CODEC)) 
    
    {
        Hawk.put(HawkConfig.IJK_CODEC, "硬解码");
    }
    
    if (!Hawk.contains(HawkConfig.DOH_URL)) 
    
    {
        Hawk.put(HawkConfig.DOH_URL, 2);
    }
    
    if (!Hawk.contains(HawkConfig.SEARCH_VIEW))
    
    {
        Hawk.put(HawkConfig.SEARCH_VIEW, 2);
    }
}

public static App getInstance() 

{
    return instance;
}




TVBox资源接口外链托管网址：感觉哪个好用用哪个，能不能用，好不要用，有没有坑，自己测试。网上的东西，只是收集，不做测试推荐。
1、https://gitea.com/ 已开始限制，清理

2、https://gitee.com/

3、https://agit.ai/

4、云储： https://yunchu.cxoip.com/

5、腾讯云： https://coding.net/

6、瑞典外链网盘：https://anonfiles.com/

7、比邻： https://pan.bilnn.com 收费了，能在线编辑

8、惜染 https://mpimg.cn/ 不能在线编辑

9、枫铭网盘： https://pan.dkpoi.com 不能编辑

10、https://out.zxglife.top 不能编辑

11、OpenDrive: https://www.opendrive.com/ 能在线编辑，慢

12、nite07网盘 https://share.nite07.com

13、ifilespace https://demo.ifile.space/main

14、七彩云存储： https://cloud.06dn.com/login

15、豆子外链： http://zuoye.free.fr/index.php 限制文件格式

16、棱束链： https://www.lingshulian.com/

17、凯速网https://my.ksust.com

18、乐分发存储：https://pan.leffs.cn/Login

19、https://www.jsdelivr.com/

20、恩华云盘：https://pan.ehvip.cn

21、诺灸：https://www.cloudewl.cn

22、https://gitcode.net/explore

23、吾爱云盘：http://52bsj.vip:81/login

24、https://codeberg.org/

25、https://www.notabug.org

26、书源 http://shuyuan.miaogongzi.net/index.php

短链接制作网址：哪个稳定自己测试。
https://gg.gg

https://qiu.moe

https://www.c1n.cn

https://0dlj.cn

https://0a.fit

http://mtw.so

https://sd4.cn

https://pqu.cn

https://88d.cn

https://loveer.win

https://mtool.chinaz.com/dwz

https://waurl.cn

https://dwz.dk

壁纸：
http://www.kf666888.cn/api/tvbox/img

https://picsum.photos/1280/720/?blur=10

https://qiu.moe/a723

解析测试：
http://www.36nu.com/apiTest

更新
多jar链接写法，根据app版本来：
Pluto Player版本：
{"key":"","name":"","api":"","type":3,"filterable":1,"quickSearch":1,"searchable":1,"plugin":"http:///.jar"},

这个：
{"key":"","name":"","type":3,"api":"","searchable":1,"quickSearch":1,"filterable":1,"spider":"http:///.jar"},

俊佬版本多jar链接写法：
{"key":"","name":"","type":3,"api":"***","searchable":1,"quickSearch":1,"filterable":1,"jar":"your_other_jar"},

牛人制作网站：版本收集、接口收集、TG群收集，小白有这个网站能躺平了！也可以自己微信公众号搜集。
云星：https://shou.eruu.cn/

奇奇：http://bbs.qiqiv.cn/thread-11973-1-1.html

https://github.com/tv-player/TvBox

TVBox配置编辑器：
https://kvymin.github.io/CatVodTVJsonEditor/
