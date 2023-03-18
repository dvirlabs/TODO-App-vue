<template>
    <div class="main_page">
        <ListOfTables />
        <TodoListTable />
    </div>
</template>

<script>
import ListOfTables from './ListOfTables.vue';
import TodoListTable from './TodoListTable.vue';

export default {
    components: {
        ListOfTables,
        TodoListTable
    }
}
</script>

<style scoped>
.main_page {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    height: 70%;
    align-items: center;
    padding: 0.5em;
}
</style>