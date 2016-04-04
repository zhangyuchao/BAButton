# BAButton
自定义button

>**开发中如有问题，可以联系本人**

**新浪微博：@博爱1616**

**QQ：     137361770**

#### 对pod还是不熟的同学，可以看下我的博客，是最新的pod安装和使用方法，

###### http://www.cnblogs.com/boai/p/4977976.html

# 更新记录：

## 2016.04.4 --- 

>##完全实现button的自定义，

![image](https://github.com/boai/BADemoTest/blob/master/Image/gif6.gif)

``` 用枚举展示button的类型：
BAAligenmentStatusNormal, // 默认
BAAligenmentStatusLeft, // 左对齐
BAAligenmentStatusCenter, // 居中对齐
BAAligenmentStatusRight, // 右对齐
BAAligenmentStatusTop, // 图标在上，文本在下(居中)
BAAligenmentStatusBottom, // 图标在下，文本在上(居中)

```
BACustomButton *btn1 = [BACustomButton BA_ShareButton];
[btn1 setBackgroundColor:[UIColor greenColor]];
[btn1 setImage:[UIImage imageNamed:@"btn_share"] forState:UIControlStateNormal];
[btn1 setTitle:@"左对齐[文字左图片右]" forState:UIControlStateNormal];
[btn1 setTitleColor:[UIColor blackColor] forState:UIControlStateNormal];
btn1.buttonStatus = BAAligenmentStatusLeft;
btn1.buttonCornerRadius = 5.0;
btn1.titleLabel.font = [UIFont systemFontOfSize:15];
btn1.frame = CGRectMake(CGRectGetMinX(btn.frame), CGRectGetMaxY(btn.frame) + 10, 200, 50);
[self.view addSubview:btn1];

```
BACustomButton *btn5 = [[BACustomButton alloc] initWitAligenmentStatus:BAAligenmentStatusTop];
[btn5 setBackgroundColor:[UIColor greenColor]];
[btn5 setImage:[UIImage imageNamed:@"btn_share"] forState:UIControlStateNormal];
[btn5 setTitle:@"图片在上，文字在下" forState:UIControlStateNormal];
btn5.titleLabel.font = [UIFont systemFontOfSize:10];
btn5.buttonCornerRadius = 5.0;
[btn5 setTitleColor:[UIColor blackColor] forState:UIControlStateNormal];
btn5.frame = CGRectMake(CGRectGetMinX(btn.frame), CGRectGetMaxY(btn4.frame) + 10, 200, 80);
[self.view addSubview:btn5];



