# css

## 定位

![image-20240202000305299](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240202000305299.png)

- **静态定位：static**：元素按照标准流布局，left 、right、top、bottom没有任何作用
- **相对定位：relative**：按照标准流布局，可以通过left 、right、top、bottom定位（定位对象参照自己原来的位置
  - **应用场景**:在不影响其他元素的前提下，对当前元素进行微调

- **固定定位：fixed**：脱离标准流，可以通过left 、right、top、bottom定位，参照对象是视口，当画布滚动时，固定不动
  - **视口：**文档可视区域
  - **画布：**渲染文档的区域，画布超出视口范围，通过滚动查看，一般画布大于视口
- **绝对定位：absolute：**脱离标准流，left 、right、top、bottom定位，定位参照临近的祖先元素，如果没有祖先元素，则参照对象为视口
- **粘性定位：sticky：**相对定位＋固定定位，允许被定位的元素表现像相对定位一样，滚到某个阈值时，变成固定定位

**将position设置为absolute/fixed元素的特点(一)**：

◼ **可以随意设置宽高**

◼ **宽高默认由内容决定**

◼ **不再受标准流的约束**

 不再严格按照从上到下、从左到右排布

 不再严格区分块级、行内级，块级、行内级的很多特性都会消失

◼ **不再给父元素汇报宽高数据**

◼ **脱标元素内部默认还是按照标准流布局**

**如果希望绝对定位元素的宽高和定位参照对象一样，可以给绝对定位元素设置以下属性**

> left: 0、right: 0、top: 0、bottom: 0、margin:0

**如果希望绝对定位元素在定位参照对象中居中显示，可以给绝对定位元素设置以下属性**

> left: 0、right: 0、top: 0、bottom: 0、margin: auto
>
> 另外，还得设置具体的宽高值（宽高小于定位参照对象的宽高）

### z-index

​	设置元素层叠顺序，仅对定位元素有效

**比较方式**

- **兄弟关系：**直接比较z-index

- **非兄弟关系：**从自己以及祖先元素中找出邻近两个定位元素比较



## 浮动

![image-20240202003922189](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240202003922189.png)

**元素脱离标准流**

- 会往左右方向移动，紧贴着父元素，或者其他元素边界为止，定位元素会层叠在浮动元素上面

- 如果一个元素浮动另一个元素已经在那个位置，会紧贴那个元素

  ![image-20240202004927854](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240202004927854.png)

- **浮动元素不能与行内级内容层叠，行内级内容将会被浮动元素推出**：比如行内级元素、inline-block元素、块级元素的文字内容

- ![image-20240205231324487](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240205231324487.png)

- **行内级元素、inline-block元素浮动后，其顶部将与所在行的顶部对齐**

- ![image-20240205231348307](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240205231348307.png)

### 浮动问题--高度塌陷



## 布局方案总结

![image-20240205231013961](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240205231013961.png)

## flex布局

**什么是flexbox**

​	弹性盒子，一种按行或者按列布局元素的一维布局方法，可以膨胀填充额外空间，收缩适应空间，通常使用flexbox方案称为flex布局

**浮动布局解决了什么**

- 在父元素里面垂直居中一个块
- 所有子项等分可用高度或宽度，不需要管多少高度和宽度
- 多列布局中使用所有列采用相同高度，和内容量包含不同

**开启布局的元素叫flex container，里面的直接子元素叫flex item**

**flex item 特点：**

- flex item的布局将受flex container属性的设置来进行控制和布局;
- flex item不再严格区分块级元素和行内级元素;
- flex item默认情况下是包裹内容的, 但是可以设置宽度和高度;

如何开启

display：flex



### flex container属性

![image-20240205234241844](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240205234241844.png)

### flex item属性

![image-20240205234716534](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240205234716534.png)





## css函数

![image-20240206010217646](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240206010217646.png)

![image-20240206010325718](C:\Users\听风\AppData\Roaming\Typora\typora-user-images\image-20240206010325718.png)
