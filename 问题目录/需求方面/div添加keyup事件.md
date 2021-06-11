## 需求
### 需求描述
* `div`添加`keyup`事件
### 存在的问题
* `div`无法直接使用`keyup`事件
### 解决办法
* 添加`tabindex`属性(tabindex = '1')
* 触发`focus`事件
* 修改`:focus-visible`属性的`outline`