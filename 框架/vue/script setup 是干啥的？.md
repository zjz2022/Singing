## script setup 是干啥的？

scrtpt setup 是 vue3 的语法糖，简化了组合式 API 的写法，并且运行性能更好。使用 script setup 语法糖的特点：

* 属性和方法无需返回，可以直接使用。
* 引入组件的时候，会自动注册，无需通过 components 手动注册。
* 使用 defineProps 接收父组件传递的值。
* useAttrs 获取属性，useSlots 获取插槽，defineEmits 获取自定义事件。
* 默认不会对外暴露任何属性，如果有需要可使用 defineExpose 。