# vue-全屏指令
这是一个可以在全屏之后插入筛选器的基于element-ui组件封装的vue-全屏指令

## 使用方式如下:
### 对于指令参数的说明
updateFullScreen参数是在不展示icon的情况下配置的触发全屏的参数用于写在触发全屏的函数中 值是true进入全屏 值是false退出全屏

showIcon true是展示全屏icon 通过点击icon触发全屏 false则不展示全屏icon

insertNode 是在全屏时插入的dom节点的id 可用于全屏之后插入一些筛选条件用来筛选

index 是页面中全部全屏指令的标识 注意 每个指令的标识应当不相同 用来区分全屏指令

fn 是全屏之后可以做的一些样式调整 以及别的操作 它有两个参数一个是binding 一个是el el是插入全屏指令的节点本身

top && right: 是全屏指令在插入节点的位置

#### 第一种配置方案
如果不想展示全屏icon 想通过一种方式触发全屏操作的话请采用如下配置方案
```
v-fullScreen="{
    updateFullScreen:updateFullScreen,
    showIcon:'false',
    insertNode:'fullScreenFilter',
    index:index,
    isNeedInsertNode:chart.config.extends.hasFilter
}"
```
#### 第二种配置方案

如果想展示icon，通过点击icon触发全屏，请采用如下配置方案
```
v-fullScreen="{
    showIcon:'true',
    insertNode:'fullScreenFilter',
    index:index,
    top:20,
    right:20
}"
```
