## 问题描述1
* `Avoid mutating a prop directly since the value will be overwritten whenever`

## 原因
* vue中的父子组件是单向数据流，避免子组件修改父组件的状态

## 解决办法
* 在子组件中添加新的变量接收props值
```javascript
props:['active'],
data(){
  return {
    curActive:this.active
  }
}
```