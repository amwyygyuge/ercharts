## 安装

```js
npm install baishancloud-charts --save
```



## 引用示例



```jsx
import React, { Component } from 'react';
import {Bar} from 'baishancloud-charts'

class BarDemo extends Component {
    state = {
        data: [],
        col: ["date", "page", "food"]
    }
    componentDidMount() {
        this.setState({
            data: this.getData(10)
        })
    }
    getData = (times) => {
        let data = [],
            stateDate = +new Date(2011, 1, 2),
            day = 1000 * 60 * 60 * 24;
        for (let i = 0, n = times; i < times; ++i) {
            let now = new Date(stateDate += day);
            data.push({
                date: [now.getFullYear(), now.getMonth() + 1, now.getDate()].join('/'),
                page: Math.floor(Math.random() * 300),
                food: Math.floor(Math.random() * 300),
                tool: Math.floor(Math.random() * 300)
            })
        }
        return data
    }
    render() {
        return (
            <div>

                <Bar
                    data={this.state.data}
                    col={this.state.col}
                    width={800}
                    height={1000}
                    setting={{
                        backgroundColor:'#000'
                    }}
                >
                </Bar>
            </div>

        );
    }
}

export default BarDemo;
```



