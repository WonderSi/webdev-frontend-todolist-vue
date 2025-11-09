<template>
    <div class="app">
        <div class="app__container">
            <Header/>
            <TodoList/> 
            <AddButton @click="openModal"/>
            <AddTaskModal :open="modalOpen" @close="closeModal"/>
        </div>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import Header from '@/components/Header.vue';
    import TodoList from '@/components/TodoList.vue';
    import AddButton from '@/components/AddButton.vue';
    import AddTaskModal from './components/AddTaskModal.vue';

    const modalOpen = ref(false)

    function openModal() {
        modalOpen.value = true;
    }

    function closeModal() {
        modalOpen.value = false;
    }
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
