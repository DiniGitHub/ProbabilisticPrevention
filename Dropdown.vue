<template>
    <select 
        v-model="internalSelection"
        @change="updateValue"
    >
        <option v-if="isBlankIncluded" :value="null"> Please Select an Option</option>
    
        <option 
            v-for="option in options"
            v-bind:key="option.value"
            :value="option.value"
        >
            {{ option.label }}
        </option>
    </select>
</template>
  
<script>
import { computed } from 'vue'

export default {
    name: 'App',
    props: {
        modelValue: {
            type: [String, Object],
            default: null
        },
        options: {
            type: Array,
            required: true
        },
        isBlankIncluded: {
            type: Boolean,
            default: true
        }
    },
    setup (props, { emit }) {
        return {
            selectedValue: computed({
                get: () => props.modelValue,
                set: (value) => emit('update:modelValue', value)
            })
        }
    },
    data () {
        return {
            internalSelection: null
        }
    },
    methods: {
        updateValue () {
            this.selectedValue = this.internalSelection
        }
    }
}
</script>
  
<style>
</style>
  