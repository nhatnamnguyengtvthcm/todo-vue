<template>
    <div>
        <h2>{{ msg || 'No props passed yet!' }}</h2>
    </div>
</template>

<script>
import {  } from 'vue'
export default {
    props: {
        msg: String
    },
    setup () {
        

        return {
          
        }
    }
}
</script>

<style lang="scss" scoped>

</style>