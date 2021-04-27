<template>
    <header>
        <h1>{{title}}</h1>
        <Button v-show="inHomePage" @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask ? 'black' : 'green'" />
    </header>
</template>

<script>
import Button from './Button'
export default {
    name:'Header',
    components: {Button},
    computed:{
        inHomePage(){
            return this.$route.path === "/"
        }
    },
    props: {
        title:{
            type:String,
            default:'Header title'
        },
        showAddTask:{
            type:Boolean,
            default:false
        }
    }
}
</script>

<style scoped>
header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>