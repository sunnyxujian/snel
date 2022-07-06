# snel

**基于element，快速构建界面的ui库，她再也不会苦苦等我下班了**

## 工程化思路

- [ ] 使用monorepo管理各个子模块，增加changelog

- [ ] 使用rollup打包项目，做好treeshaking，支持css和js单独引用，排除vue和element-ui

- [ ] 使用sass编写样式，支持css变量定义主题

- [ ] 使用vuepress渲染md文档，并且编写插件支持在线编辑实时预览效果，可能还需要编写主题

- [ ] 使用karma编写单元测试


## 代码思路

- [ ] 主要用配置项描述UI界面，可以通过slot和render函数进行自定义渲染  

- [ ] 跟elementUI的API保持一致，中划线改小驼峰，组件划分尽量细致，保证组件性能

- [ ] 能设计默认值的必须设计合理的默认值，并且所有默认值尽可能的全局自义定

- [ ] 核心组件如何设计: `Table`、`Form`、`Detial`、`EditTbale`、`CRUD`、`Group` 

- [ ] 各个组件的combo如何整合，HOC？render？v-if？

- [ ] `CRUD`组件如果传入接口交互方法，和出入参数据处理函数来操作增删改查等基础操作，如果`pageination`不为`false`，还要整合分页逻辑，如果传入了路由配置则带上参数进行路由跳转，什么都没传的时候抛出事件。此外还有支持默认权限、虚拟滚动，动态列，隐藏查询，以及全部的el-table功能

- [ ] 表单组件的联动如何设计?  传入如下配置：`reaction:{ deps: [...], action: (data) => {...} }` ，不传`action`的时候走默认联动：如果是配置request相关属性(url,methed,params,error)，则触发重新请求（实现方式：链表？MAP？）

- [ ] 全局配置的设计，例如：设置request请求工具方法，默认接口的数据的取值，默认展示文本的字段，默认传值字段。表格单元格和查看组件空数据展示`--`？配置项schema提示？等等。。。

- [ ] 支持注入自定义组件，后续直接通过配置渲染出来（自定义组件是否需要符合设计规范？）

- [ ] 支持国际化翻译，并且支持自定义翻译

- [ ] 主题配置，支持暗黑模式

- [ ] 文档设计需要**斟酌**，如何直观的展示组件的各项功能：
   - 类似后管界面？
   - 动态支持页面增加？
   - tag页签交互？
   - 实时展示配置代码且可以修改并触发页面更新？
   - 支持界面设计器
   - 支持直接导出`.vue`文件



