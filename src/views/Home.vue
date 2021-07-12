<template>
  <router-link to="/about">点这里去关于我们页面</router-link>
  <div>
      这里是一个计数器 >>> <span class="red">{{count}}</span> <br>
    <button @click="countAdd">{{btnText}}</button>

  </div>
</template>
<script>
import {ref} from 'vue'
export default {
    setup() {
        const btnText = 'dianzhgekjfd'
        const count = ref(0)
        const countAdd = () => {
            count.value++
        }
        return {
            btnText,
            count,
            countAdd
        }
    }
}
</script>

