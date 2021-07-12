<template>
    <div>
        <div>{{id}}</div>
        <button @click="isAdd">id++</button>
    </div>
</template>
<script>
import {useStore} from 'vuex'
import { ref, computed } from 'vue'

export default {
    setup() {
        const store = useStore()
        const id = computed(()=> store.state.id)
        return {
            id,
            isAdd:()=>store.commit('isAdd')
        }
    }
}
</script>

