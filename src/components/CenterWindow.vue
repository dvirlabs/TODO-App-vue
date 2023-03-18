<template>
    <div>
        <DarkModeButton />
        <MainPage />
        <ActionButtons />
    </div>
</template>


<script>
import DarkModeButton from './DarkModeButton.vue';
import MainPage from './MainPage.vue';
import ActionButtons from './ActionButtons.vue';

export default {
    name: 'CenterWindow',
    components: {
        DarkModeButton,
        MainPage,
        ActionButtons,
        
    }
}
</script>


<style>
div {
    width: 70%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

div>h1 {
    font-family: 'Manrope';
    font-size: 1.7rem;
    font-weight: 900;
    color: var(--midwin_titles_color);
}

table {
    display: block;
    height: 100%;
    width: 100%;
    overflow: overlay;
    padding-inline: 1em;
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>