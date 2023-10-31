<template>
    <div>
        <p ref="pElementRef">Vue Template Ref</p>
    </div>
</template>

<script>
import { ref, onMounted } from 'vue'
export default {
    
    setup () {
        const pElementRef = ref(null)
        
        onMounted(() => {
        pElementRef.value.textContent = "mouted!";
        })
        return {
            pElementRef
        }
    }
   
}
</script>

<style lang="scss" scoped>

</style>