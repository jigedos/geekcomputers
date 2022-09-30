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
