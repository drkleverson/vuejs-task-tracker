<template>
    <button @click="$emit('btn-click')" :style="{background:color}" class="btn">{{text}}</button>
</template>

<script>
export default {
    name:'Button',
    props:{
        text:{
            type:String,
            default:'Add'
        },
        color:{
            type:String,
            default:'black'
        }
    },
}
</script>