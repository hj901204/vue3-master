<template>
  <router-link to="/">点这里去首页</router-link>
    <hr>
  <dl>
    <dt>{{state.name}}</dt>
    <dd>性别：{{state.sex}}</dd>
    <dd>地址：{{state.address}}</dd>
  </dl>
  <button @click="addressChange">更新地址</button>
</template>
<script>
import {reactive} from 'vue'
export default {
    setup() {
        const state = reactive({
            name:'funleo',
            sex:'boy',
            address:'shagnhai'
        })
        console.log(state)
        const addressChange = () =>{
            state.address +='pudong'
        }
        return {
            state,
            addressChange
        }
    }
}
</script>

