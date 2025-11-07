<template>
    <div class="app">
        <div class="app__container">
            <Header/>
            <TodoList/> 
            <AddButton/>
        </div>
    </div>
</template>

<script setup>
    import Header from '@/components/Header.vue';
    import TodoList from '@/components/TodoList.vue';
    import AddButton from '@/components/AddButton.vue';
</script>

<style scoped lang="scss">
    .app {
        display: flex;
        justify-content: center;
        width: 100%;
        height: 100vh;

        &__container {
            width: fit-content;
            height: 100%;
            position: relative;
            box-sizing: border-box;
        }
    }
</style>
