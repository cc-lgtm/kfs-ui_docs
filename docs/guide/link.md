# Link
*用于跳转到指定地址*
#### 不同类型
:::demo 使用`type`属性来定义 Link 的类型。
```vue
<template>
  <div class="box">
    <cc-link>link</cc-link>
    <cc-link type="primary">link</cc-link>
    <cc-link type="success">link</cc-link>
    <cc-link type="warning">link</cc-link>
    <cc-link type="danger">link</cc-link>
    <cc-link type="info">link</cc-link>
  </div>
</template>

<style>
.box {
  width: 50%;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
}
</style>
```
:::

#### 不带下划线
:::demo 使用`underline`属性来定义 Link 的是否显示下划线。
```vue
<template>
  <div class="box">
    <cc-link :underline="underline">link</cc-link>
    <cc-link type="primary" :underline="underline">link</cc-link>
    <cc-link type="success" :underline="underline">link</cc-link>
    <cc-link type="warning" :underline="underline">link</cc-link>
    <cc-link type="danger" :underline="underline">link</cc-link>
    <cc-link type="info" :underline="underline">link</cc-link>
  </div>
</template>

<script lang="ts">
import {ref} from 'vue'
export default {
  setup() {
    const underline = ref<boolean>(false)
    return {
      underline
    }
  }
}
</script>

<style>
.box {
  width: 50%;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
}
</style>
```
:::

#### 禁用
:::demo 使用`disabled`属性来定义 Link 不可点击。
```vue
<template>
  <div class="box">
    <cc-link disabled>link</cc-link>
    <cc-link type="primary" disabled>link</cc-link>
    <cc-link type="success" disabled>link</cc-link>
    <cc-link type="warning" disabled>link</cc-link>
    <cc-link type="danger" disabled>link</cc-link>
    <cc-link type="info" disabled>link</cc-link>
  </div>
</template>

<style>
.box {
  width: 50%;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
}
</style>
```
:::

#### 跳转
:::demo 使用`href`属性来定义 Link 跳转连接。
```vue
<template>
  <div class="box">
    <cc-link href="https://www.npmjs.com/package/kfs-ui" type="success">link</cc-link>
  </div>
</template>

<style>
.box {
  width: 50%;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
}
</style>
```
:::

#### 属性
| 属性 | 描述 | 类型 | 可选值 | 默认 |
| ------------- |:-------------:| -----:|:-------------:| -----:|
| underline | 是否带下划线 | `boolean` | `true`,`false` | `true`  |
| type  | 按钮的类型 | `string` | `default`,`primary`,`success`,`warning`,`danger`,`info` | `default` |
| href | 跳转的地址 | `string` | `-` | `-` |
| disabled | 是否禁止点击 | `boolean` | `true`,`false` | `false` |

#### slots
| 名称 | 描述 |
| ------------- |:-------------:|
| `-` | `Link`内自定义内容 |