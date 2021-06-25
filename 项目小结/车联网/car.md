## 车联网
> 第一个实战项目
### 开发过程中学到的
#### 一、技术方面
##### 1.可视化库
###### 1) Echarts
* 一开始不熟悉开发流程，不知道项目中的一些特效怎么来的，后来接触到了源码，了解到用的是`Echarts`库
* Echarts库中包含了多种图表和样例，其中包括柱状图、饼状图、折线图、关系图、地图
* 知识点
  * 使用流程：获取dom(dom)->初始化dom(myChart)->添加配置项(option)->设置配置项`myChart.setOptions(option)`
  * 可动态显示数据
    * 把开始的option中的data置为空数组，其他的都填上
    * 数据获取之后把一个带有数据的对象放到`setOptions`中
> https://echarts.apache.org/zh/index.html
###### 2) Vis
* Vis这个框架是后期开发时遇到的，使用起来也很方便，可适用于展示拓扑关系
> https://visjs.org/
##### 2.框架
###### 1) Element UI
* Element UI适用于管理系统的开发，里边包含了需要的组件以及对应的事件，可自定义开发
###### 2) Vue
* 方便处理数据逻辑以及交互过程，让重心由之前频繁操作dom来触发事件转移到后面可以直接去思考事件交互
* 知识点
  * 生命周期函数(按照执行顺序)
    * beforeCreated
    * created
    * beforeMounted
    * mounted
    * beforeUpdated
    * updated
    * beforeDestroyed
    * destroyed
  * v-指令
    * v-if/v-else-if/v-else/v-show
      * 控制显示和隐藏
      * v-if为false时，dom元素消失；v-show没有，而是对应的dom元素display为none
    * v-model
      * 双向绑定数据
    * v-on/@
      * 事件
    * v-bind/:
      * 自定义属性
  * watch属性
    * 监听数据变化，可作为值
    * 深层监听会失效，得添加`deep: true`
      ```js
      test:{
        handler(oldName, newName) {

        },
        deep: true
      }
      ```
> 可用JSON.stringify来判断两个对象是否一样
###### 3) Bootstrap、jQuery
* 公司最开始的框架是Bootstrap、jQuery和Vue，不过最开始使用的Vue是单个元素进行引用；后期是整个系统都是基于Vue进行开发
#### 二、设计方面
##### 1.交互
* 尽量减少用户的操作但是能让用户了解到自己正在做的事(需要对事件交互处理得更简单)
* 了解用户的使用习惯，根据用户的使用习惯设计布局以及交互
##### 2.配色
* 暗色背景适合浅色
