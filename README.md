# CopySource
iOS项目框架问题（baseVC，baseNav、全屏返回手势、旋转屏幕、截获back返回事件、定制不同VC的返回按钮等等）

//-------*****************项目涵盖知识点*******************-----------

//1、全屏返回（cell左滑动删除的手势冲突，支持全屏和不支持全屏）

//2、左边返回按钮POP点击事件拦截（获取）

//3、BaseNav和BaseVC封装

//4、关于rootVC（登录登出设计）

//5、关于launchImage（删除了之前旧的image并且删除了手机APP，安装后还是旧图，上线后App Store上下载的也还是旧图，WTF！）

//6、iOS旋转屏幕(视频WMPlayer+浏览器+VR)

//7、“让我们一次性解决导航栏的所有问题”（设计思路或bug或技术问题）

    //7.1、透明导航栏
    
    //7.2 不同颜色的导航栏
    
    //7.3 不同返回按钮
    
    //7.4 不带导航-->push 到 带导航的页面，手势返回bug
    
    //7.5 动态改变导航栏的透明度
    

//8、适配iPhone X和iOS 11
 
    
    //8.1 扩大iOS 11上返回按钮的点击范围，解决iOS 11上难点击导航栏按钮的bug
    
   
    //8.2 导航栏nav和Tabbar的适配
    
    
    //8.3 添加和修改了一些适配iOS 11的宏
    
    
    //8.4 修正push过程中tabbar上移问题
    if (@available(iOS 11.0, *)){
        // 修改tabBra的frame
        CGRect frame = self.tabBarController.tabBar.frame;
        frame.origin.y = [UIScreen mainScreen].bounds.size.height - frame.size.height;
        self.tabBarController.tabBar.frame = frame;
    }
    
    
    
 

    
    
