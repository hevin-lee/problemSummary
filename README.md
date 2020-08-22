# problemSummary
vue各种奇葩问题汇总

## 问题1：组件循环引用踩坑，组件未注册问题
解决方案  在生命周期中临时注册一下：

    beforeCreate() {
      this.$options.components.TreeFold = require('./treefold.vue').default
    }
参考地址：https://blog.csdn.net/weixin_34267123/article/details/91427657
