<template>
    <div v-if='isVisible'>
        <h1>Directive</h1>
        <ul>
            <template v-for="fruit in fruits" >
                <li v-if="fruit !== 'mango'" :key="fruit" >{{fruit}}</li>
            </template>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'DirectiveTest',
        data(){
            return{
                isVisible:true,
            fruits:['banana', 'apple', 'orange', 'mango']
                }
        }
    }
</script>

<style lang="scss" scoped>

</style>