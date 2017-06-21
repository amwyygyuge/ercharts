## 通用属性

---

### 关键配置

该组件**最关键最基础**的两个配置项目，分别是用来传入数据以及数据的映射关系，包括一系列配置的自动生成。



| 配置项 | 简介 | 类型 | 备注 |
| :--- | :--- | :--- | :--- |
| data | 图表的数据来源 | array\[object\] | 其中一项作为X轴，其他项目作为数据源 |
| col | 图表与数据的映射关系 | array\[string\|object\] | 默认第一项用来作为X轴，其余会作为数据映射到图表上。假如作为对象，会直接作为该数据的配置项。 |



这边给出一组简单的数据配置案例

```js
 const data=  [
       {
           date:"2016/05/08",
           sold:50,
           pay:400
       },
       {
           date:"2016/05/09",
           sold:500,
           pay:40
       }
    ];
const col=[ "date"，{ name:"sold",step:true },"pay"  ]
```

#### 基础配置



这边会罗列出替使用者做出处理的配置，其他没有列出来的需要引用的请自行使用**对象**形式传入，也可以通过setting进行补充配置。

| 配置项 | 简介 | 类型 | 备注 |
| :--- | :--- | :--- | :--- |
| title | 图表标题 | string |  |
| legend | 图例按钮 | boolean | 图例是否显示，会根据col的数据自动生成 |
| xAxis | X轴配置 |  | 默认生产 |
| yAxis | Y轴配置 |  | 默认生成 |
| dataZoom | 缩放功能 | string | 三种模式:inside/slider/both |
| tooltip | 数据提示工具 | string | 两种模式:shadow/cross |
| toolbox | 工具类 | string\(string\|object\) | 支持的工具类:dataZoom/dataViwer/magicType/restore/saveAsImage/brush |
| brush | 刷子工具 | array\(string\) | 刷子类型:rect/polygon/lineX/lineY/keep/clear |
| clolor | 配色 | array\(string\) | 默认为echarts配色 |
| backgroundColor | 背景颜色 | string |  |

### 扩展配置

| 配置项 | 简介 | 类型 | 备注 |
| :--- | :--- | :--- | :--- |
| width | 宽 | string | 默认继承父级宽度 |
| height | 高 | string | 默认继承父级高度 |
| legendLimit | 图例数量限制 | number |  |
| loading | 加载状态 | boolean |  |
| reverse | X轴与Y轴置换 | boolean |  |
| percent | 显示Y轴百分比 | boolean |  |
| legendSelectedMode | 图例选择模式 | string | single/multiple |



