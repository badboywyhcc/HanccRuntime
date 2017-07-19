# HanccRuntime
这是一个轻型的runtime使用用例，用于定制全局的UI。
## cocoapods 获取
```
pod 'HanccRuntime'
```
## 场景1:交换方法
```
#import "AppDelegate.h"
#import "HanccCommonComponentsConfig.h"

@interface AppDelegate ()

@end

@implementation AppDelegate


- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    // Override point for customization after application launch.
    
    [HanccCommonComponentsConfig Hancc_viewDidLoad:^(UIViewController *vc) {
        vc.view.backgroundColor =[UIColor yellowColor];
        [vc.navigationController.navigationBar setTranslucent:YES]; // 设置navigationBar的透明效果
        [vc.navigationController.navigationBar setBackgroundImage:[UIImage imageNamed:@"navigationbar"] forBarMetrics:UIBarMetricsDefault];
    }];
    return YES;
}
```
### 现象:

![](file:///Users/hcc/Desktop/Screen Shot 2017-07-19 at 下午4.10.18.png)

