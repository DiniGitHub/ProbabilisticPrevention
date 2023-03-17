<template>
    <div>    
        <input 
            :placeholder="placeholder"
            class=""
        />
        <span v-if="!isValid">Invalid</span>
    </div>  
</template>
  
<script>
    export default {
    name: 'App',
    props: {
        placeholder: {
            type: String,
            default: 'Name'
        }
    },
    components: {},
    computed: {
        isValid () {
            return true
        }
    }
}
</script>
  
<style>
</style>
  