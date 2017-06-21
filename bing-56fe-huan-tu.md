## 饼图/环图

---

#### 特殊配置

| 配置项 | 简介 | 类型 | 备注 |
| :--- | :--- | :--- | :--- |
| ring | 显示为环图 | boolean |  |
| rose | 面积受数值影响 | boolean |  |

#### 示例

```jsx
                    <Pie
                        ring
                        rose
                        data={this.state.data}
                        col={this.state.col}
                    >
                    </Pie>
```



#### 备注

使用饼图时暂时只支持单一维度的数据，如果是多维度数据不建议使用饼图来展示。



