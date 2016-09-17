## SGActionSheet

![](https://github.com/kingsic/SGTopTitleView/raw/master/Picture/sorgle.png) 

![](https://github.com/kingsic/SGTopTitleView/raw/master/Picture/sorgle2.png)

![](https://github.com/kingsic/SGTopTitleView/raw/master/Picture/sorgle3.png)

### * `自定义的UIActionSheet`<br>


* SGActionSheet使用方法一：

  * 将项目中SGActionSheet文件夹拖入工程

  * 导入#import "SGActionSheet.h"头文件

  * 对象方法创建
  ```Objective-C
  - (instancetype)initWithFrameWithTitle:(NSString *)title delegate:(id<SGActionSheetDelegate>)delegate cancelButtonTitle:(NSString *)cancelButtonTitle otherButtonTitleArray:(NSArray *)otherButtonTitleArray 
  ｀｀｀

  * 类方法创建
  ```Objective-C
  * + (instancetype)actionSheetWithTitle:(NSString *)title delegate:(id<SGActionSheetDelegate>)delegate cancelButtonTitle:(NSString *)cancelButtonTitle otherButtonTitleArray:(NSArray *)otherButtonTitleArray
  ｀｀｀

  * sheet.titleColor = [UIColor redColor]; // 设置提示信息文字颜色 （默认为黑色）
 
  * sheet.otherTitleColor = [UIColor brownColor]; // 设置其他按钮文字颜色 （默认为黑色）
 
 
  * 遵循SGActionSheetDelegate协议的delegate_SG方法
  ```Objective-C
  - (void)SGActionSheet:(SGActionSheet *)actionSheet didSelectRowAtIndexPath:(NSInteger)indexPath；
  ```
  
* SGTopTitleView使用方法二：（详细使用方法，请参考Demo）

* 提示信息文字，根据内容自动调节
```Objective-C
- (CGRect)boundingRectWithSize:(CGSize)size options:(NSStringDrawingOptions)options attributes:(nullable NSDictionary *)attributes context:(nullable NSStringDrawingContext *)context;
```
