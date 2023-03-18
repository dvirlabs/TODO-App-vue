<template>
    <div class="left_side">
        <h1>Lists</h1>
        <div class="all_lists">
            <div class="chosen_list">
                <h2>Work</h2>
                <h3>Tasks:3</h3>
            </div>
            <div class="normal_list">
                <h2>Home</h2>
                <h3>Tasks:6</h3>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style>
.left_side{
    width: 30%;
    border-right: 2px solid var(--middle_line_color);
}
.right_side{
    width: 70%;
}
.left_side , .right_side{
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.left_side > h1{
    font-family: 'Manrope';
    font-size: 1.5rem;
    font-weight: 500;
    color:var(--midwin_titles_color);
}
.left_side > div > div{
    width: 12em;
    display: flex;
    flex-direction: column;
    border-radius: 0.3em;
    box-shadow: 0px 0px 3px #00000065;
    font-family: 'Manrope';
    cursor: pointer;
    transition: 0.1s ease-in-out;
    margin: 0.5em;
}
.left_side > div > div:hover{
    /* width: 13em; */
    transform: scale(102%);
    box-shadow: 0px 0px 11px 1px #00000069;
}
.chosen_list{
    background-color:var(--chosen_list_color) ;
    padding: 0.6em;
}
.normal_list{
    background-color: var(--normal_list_color);
    padding: 0.6em;
}
.left_side > div > div > h2{
    margin: 0px;
    font-size: 1.2rem;
    font-weight: 700;
}
.chosen_list > h2{
    color: var(--chosen_list_text_color);
}
.left_side > div > div > h3{
    font-weight: 400;
    margin: 0px;
    font-size: 0.85rem;
}
.normal_list h2{
    color: var(--normal_list_text_color);
}
.chosen_list > h3{
    color: var(--chosen_list_sub_text_color);
}
.normal_list h3{
    color:var(--normal_list_sub_text_color);
}

</style>