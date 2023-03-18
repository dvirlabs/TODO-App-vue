<template>
    <div class="right_side">
        <h1 class="pageTitle">TODO List</h1>
        <div class="div_pg_table">
            <table class="pg_table">
                <tr>
                    <td class="task_id">#138</td>
                    <td class="task_data">Do not forget to send me an email.</td>
                    <td class="task_status">complited</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
</script>

<style>
    .right_side {
        width: 70%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .right_side>h1 {
        font-family: 'Manrope';
        font-size: 1.7rem;
        font-weight: 900;
        color: var(--midwin_titles_color);
    }

    .div_pg_table {
        background-color: var(--task_div_bacground_color);
        height: 80%;
        width: 70%;
        border-radius: 0.3em;
        box-shadow: 0px 0px 4px #00000069;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .div_pg_table>table {
        display: block;
        height: 100%;
        width: 100%;
        overflow: overlay;
        padding-inline: 1em;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .div_pg_table>table::-webkit-scrollbar {
        background-color: #21212133;
    }

    .div_pg_table>table::-webkit-scrollbar-thumb {
        background-color: rgb(123, 123, 123);
        border-radius: 100vmin;
    }

    .div_pg_table>table::-webkit-scrollbar-thumb:hover {
        background-color: rgb(235, 235, 235);
    }

    .div_pg_table>table>tbody {
        width: 100%;
    }

    .div_pg_table>table>tbody>tr {
        font-family: 'Manrope';
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 0.5em;
        background-color: var(--task_backgruond_color);
        border: 2px solid var(--task_border_color);
        margin: 0.5em 1em;
        border-radius: 0.3em;
    }

    .div_pg_table>table>tbody>tr>td {
        padding: 0.5em;
    }

    .task_id {
        color: var(--task_id_color);
    }

    .task_data {
        color: var(--task_data_color);
    }

    .task_status {
        color: #00d700;
    }
</style>