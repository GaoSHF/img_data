

# Hough transform

![](/home/gao/Documents/Markdown/assets/hough_transform1.png)

**直角坐标系中**

> In image space, a line is plotted as x vs. y, but in 1962, Paul Hough devised a method for representing lines in parameter space, which we will call “Hough space” in his honor.
>
> In Hough space, I can represent my "x vs. y" line as a point in "m vs. b" instead. The Hough Transform is just the conversion from image space to Hough space. So, the characterization of a line in image space will be a single point at the position (m, b) in Hough space.

![](/home/gao/Documents/Markdown/assets/hough_transform3.png)

上图所示在`images space`中所表示的两条直线相互平行,根据直线的表达式 `y = mx +b`,由于直线平行,故两者斜率相同,在`Hough Space`中`m`所表示的横坐标应相同,`b`所代表的截距不同,故对应于`Hough Space`中的`C`选项.

![](/home/gao/Documents/Markdown/assets/hough_transform4.png)

对于图像空间中的一点,可以有无数条直线穿过,与图像空间相对应的霍夫空间中,其表达式可以表示为`b=-xm+y`,由于`(x,y)`的值已经确定,则图像空间中的一点对应与霍夫空间中的斜率确定的一条直线,故`A`选项正确

![](/home/gao/Documents/Markdown/assets/hough_transform5.png)

上图所示在图像空间中两个点转换为霍夫空间后,对应两条直线,但由于图像空间中的横坐标值不相同,故在霍夫空间中,两直线的斜率不同,因此,两直线必相交,所以在转换到霍夫空间中后为两条相交的直线.

![](/home/gao/Documents/Markdown/assets/hough_transform6.png)

有上述知识可知,霍夫空间中的一条直线可由图像空间中的一个点转换到,由于霍夫空间中两直线相交于`(b0,m0)`所以在图像空间中两个点必定位于一条斜率为`-b0`,截距为`m0`的直线上,故对应于图像空间中的`A`选项.

**极坐标系中**

![](/home/gao/Documents/Markdown/assets/hough_transform.png)

由于在直角坐标系中,当直线的倾斜交为90°时,直线的斜率就无法表示,为了更方便的解决这一问题,可以利用极坐标系来表示.

如上图所示,`ρ`表示原点到直线的距离,`Θ`表示直线法线与坐标轴的夹角.

![](/home/gao/Documents/Markdown/assets/hough_transform2.png)

由于图像空间中所表示的点都在一个直线内,所以在利用极坐标进行表示时,其必有一处`(Θ,ρ)`是相等的,即在霍夫空间中必定所有曲线都会相交与一点.

![Θ0](/home/gao/Documents/Markdown/assets/hough_transform7.png)

由上述知识可知,所有在一条直线上的点,其在霍夫空间中的曲线必定会相交于一点,在图像空间中,所有点构成的矩形中,位于矩形左右两条边的点构成的直线的`Θ`相同,但是原点到矩形左右两边上的点构成的直线的距离不同,故左右两边上的点,变换到霍夫空间中的为部分曲线相交于空间中`Θ`相同,`ρ`不同的两点,同理,可知矩形上下两条边上的点转换到霍夫空间中的曲线也有两个`Θ`相同,`ρ`不同的两点,矩形左右边与上下边相对于坐标系的夹角不相等,故在进行霍夫变换后应该有四个交点,分别有两组的`Θ`值相等,`C`

