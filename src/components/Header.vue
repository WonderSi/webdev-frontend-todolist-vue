<template>
    <header class="header">
        <h1 class="header__name">TODO LIST</h1>
        <div class="header__nav">
            <SearchBar/>
            <FiltersDropdown/>
            <ThemeToggle/>            
        </div>
    </header>
</template>

<script setup>
    import SearchBar from '@/components/SearchBar.vue'
    import FiltersDropdown from '@/components/FiltersDropdown.vue'
    import ThemeToggle from '@/components/ThemeToggle.vue'
</script>

<style scoped lang="scss">

</style>
