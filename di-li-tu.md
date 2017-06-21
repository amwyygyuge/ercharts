## 饼图/环图

---

#### 特殊配置

| 配置项 | 简介 | 类型 | 备注 |
| :--- | :--- | :--- | :--- |
| mapType | 地图类型 | string | china/world |
| label | 地名显示 | boolean |       |
| visualMap | 数据范围 | object | 配合mp使用来体现数据在地图上的颜色，具体配置参见官方文档。 |

#### 示例

```jsx
                    <Map
                        data={this.state.data}
                        col={this.state.col}
                        label
                        mapType='china'
                        visualMap={{
                            min: 0,
                            max: 1000,
                            type: 'continuous',
                            realtime: false,
                            calculable: true,
                            color: ['#d94e5d', '#eac736', '#50a3ba'],
                            textStyle: {
                                color: '#000'
                            }
                        }}
                    >
                    </Map>
```



#### 备注

使用地图是，col的第一个作为指标的关键词应对应为city或者country才能正确显示。

