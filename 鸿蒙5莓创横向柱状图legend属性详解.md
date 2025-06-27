大家好，欢迎回来鸿蒙5莓创图表组件的专场，我们这一期来讲解组合图组件中legend属性的详细用法。legend（图例）是图表中非常重要的组成部分，它帮助用户理解图表中不同颜色或形状所代表的数据系列。下面我们将全面解析legend的各个属性及其用法。

## 1. show - 是否显示图例

作用：控制是否显示图例组件 类型：Boolean 默认值：true 可选值：true | false 场景：当需要隐藏图例时设置为false

完整代码示例：

```
legend: {
  show: false  // 隐藏图例
}
```

## 2. orient - 图例的方向

作用：设置图例的排列方向 类型：String 默认值：'horizontal' 可选值：'horizontal' | 'vertical' 场景：水平排列适合较少的图例项，垂直排列适合较多的图例项

完整代码示例：

```
legend: {
  orient: 'vertical'  // 垂直排列图例
}
```

## 3. left/right/top/bottom - 图例位置

作用：控制图例在图表中的位置 类型：String | Number 默认值：'auto' 可选值：'auto' | '10%' | 10（像素值） 场景：精确控制图例位置时使用，百分比相对于图表容器

完整代码示例：

```
legend: {
  left: '10%',   // 距离左侧10%
  top: 20,       // 距离顶部20像素
  right: 'auto', // 右侧自动
  bottom: '5%'   // 距离底部5%
}
```

## 4. icon - 图例项的图标形状

作用：设置图例项的图标形状 类型：String 默认值：'roundRect' 可选值：'rect' | 'circle' | 'roundRect' 场景：根据图表风格选择合适的图标形状

完整代码示例：

```
legend: {
  icon: 'circle'  // 使用圆形图标
}
```

## 5. iconRadian - 图例图标的圆角

作用：设置圆角矩形的圆角大小（仅当icon为'roundRect'时有效） 类型：Number 默认值：2 场景：调整圆角矩形的圆角程度

完整代码示例：

```
legend: {
  icon: 'roundRect',
  iconRadian: 5  // 更大的圆角
}
```

## 6. itemGap - 图例项之间的间距

作用：设置图例项之间的间隔距离 类型：Number 默认值：10 场景：调整图例项之间的紧凑程度

完整代码示例：

```
legend: {
  itemGap: 20  // 更大的间距
}
```

## 7. itemTextGap - 图形与文本的距离

作用：设置图例图标与文本之间的距离 类型：Number 默认值：5 场景：调整图标与文本的间距

完整代码示例：

```
legend: {
  itemTextGap: 8  // 更大的间距
}
```

## 8. align - 图例标记和文本的对齐

作用：设置纵向布局时图例标记和文本的对齐方式 类型：String 默认值：'auto' 可选值：'auto' | 'left' | 'right' 场景：控制纵向布局时的对齐方式

完整代码示例：

```
legend: {
  orient: 'vertical',
  align: 'right'  // 右对齐
}
```

## 9. itemWidth/itemHeight - 图标尺寸

作用：设置图例图标的宽度和高度 类型：Number 默认值：itemWidth=8, itemHeight=8 场景：调整图标大小以适应不同设计需求

完整代码示例：

```
legend: {
  itemWidth: 12,
  itemHeight: 12  // 更大的图标
}
```

## 10. selectAble - 图例项是否可选

作用：控制图例项是否可以被点击选择 类型：Boolean 默认值：true 场景：需要禁用图例交互时设置为false

完整代码示例：

```
legend: {
  selectAble: false  // 禁用图例选择
}
```

## 11. data - 图例数据

作用：设置图例的数据内容 类型：Array 默认值：[] 场景：自定义图例内容时使用

完整代码示例：

```
legend: {
  data: ['系列1', '系列2', '系列3']  // 自定义图例文本
}
```

## 12. textStyle - 图例文字样式

作用：设置图例文字的样式

### 子属性详解：

#### fontFamily - 字体

作用：设置字体 类型：String 默认值：'sans-serif'

#### fontWeight - 字重

作用：设置字体粗细 类型：String 默认值：'normal'

#### fontSize - 字号

作用：设置字体大小 类型：Number 默认值：30

#### color - 颜色

作用：设置字体颜色 类型：String 默认值：'#333'

#### formatter - 格式化

作用：格式化图例文本 类型：String | Function 默认值：null 可选值：'{value}件' 或 格式化函数

完整代码示例：

```
legend: {
  textStyle: {
    fontFamily: 'Arial',
    fontWeight: 'bold',
    fontSize: 14,
    color: '#666',
    formatter: '{value}项'  // 添加单位
  }
}
```

## 13. iconStyle - 图例图标样式

作用：设置图例图标的样式 类型：Object 默认值：{} 场景：自定义图标样式

完整代码示例：

```
legend: {
  iconStyle: {
    color: '#FF0000',  // 红色图标
    borderColor: '#000',
    borderWidth: 1
  }
}
```

## 14. textUnselectedStyle - 未选中状态的文字样式

作用：设置未选中状态的图例文字样式

### 子属性详解：

#### fontFamily - 字体

类型：String 默认值：'sans-serif'

#### fontSize - 字号

类型：Number 默认值：30

#### color - 颜色

类型：String 默认值：'#999'

完整代码示例：

```
legend: {
  textUnselectedStyle: {
    fontFamily: 'Arial',
    fontSize: 12,
    color: '#CCC'  // 更浅的颜色
  }
}
```

## 15. iconUnselectedStyle - 未选中状态的图标样式

作用：设置未选中状态的图例图标样式 类型：Object 默认值：{color: '#999'} 场景：自定义未选中状态的图标外观

完整代码示例：

```
legend: {
  iconUnselectedStyle: {
    color: '#DDD',  // 更浅的颜色
    opacity: 0.5    // 半透明
  }
}
```

## 16. rLevel - 图例渲染级别

作用：设置图例的渲染优先级 类型：Number 默认值：20 场景：控制图例与其他组件的层叠关系

完整代码示例：

```
legend: {
  rLevel: 30  // 提高渲染优先级
}
```

## 17. animationCurve - 图例动画曲线

作用：设置图例动画的缓动曲线 类型：String 默认值：'easeOutCubic' 场景：调整图例交互时的动画效果

完整代码示例：

```
legend: {
  animationCurve: 'linear'  // 线性动画
}
```

## 18. animationFrame - 图例动画帧数

作用：设置图例动画的帧数 类型：Number 默认值：0 场景：控制动画流畅度，0表示不使用动画

完整代码示例：

```
legend: {
  animationFrame: 30  // 使用30帧动画
}
```

## 实际应用案例

下面是一个完整的组合图配置示例，展示了legend属性的实际应用：

```
{
  legend: {
    show: true,
    orient: 'horizontal',
    left: 'center',
    top: '5%',
    icon: 'roundRect',
    iconRadian: 4,
    itemGap: 15,
    itemTextGap: 8,
    itemWidth: 12,
    itemHeight: 12,
    selectAble: true,
    data: ['第一季度', '第二季度', '第三季度', '第四季度'],
    textStyle: {
      fontFamily: 'Microsoft YaHei',
      fontWeight: 'normal',
      fontSize: 12,
      color: '#333',
      formatter: '{value}销售'
    },
    iconStyle: {
      color: '#FFF',
      borderColor: '#666',
      borderWidth: 1
    },
    textUnselectedStyle: {
      color: '#AAA',
      fontSize: 11
    },
    iconUnselectedStyle: {
      color: '#EEE',
      opacity: 0.7
    },
    animationCurve: 'easeOutQuad',
    animationFrame: 20
  },
  // 其他图表配置...
}
```

这个配置创建了一个水平居中的图例，使用圆角矩形图标，有自定义的文本格式和样式，并启用了平滑的动画效果。

好，这期讲到这里就结束了，希望大家通过这篇文章能够全面掌握莓创图表组件中legend属性的使用方法，在实际开发中灵活运用这些属性创建出美观实用的图表图例。如果有任何问题，欢迎在评论区留言讨论！