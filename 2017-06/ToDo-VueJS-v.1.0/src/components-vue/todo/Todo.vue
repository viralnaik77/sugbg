<template>
    <div>
     
        <div id="new-todo">
            <input type="text" @keyup.enter="addTodo" v-model="todoTitle" placeholder="what needs to be done?">
        </div>
        <ul>
            <todo-item v-for="(todo, index) in mytodos" :key="index + todo" :todoText="todo" v-on:completed="completed"></todo-item>
        </ul>        
    </div>
</template>

<script>
    module.exports = require('./todo');
</script>

<style scoped src="./todo.scss" lang="sass"></style>