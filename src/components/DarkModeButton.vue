<template>
    <div id="div-theme-btn">
        <button @click="toggleDarkMode" class="theme-btn">
            <img v-bind:src="getImageURL()" class="theme-btn-img">
            <h3 id="theme_but_text">{{ this.isDarkMode ? 'Dark' : 'Light' }}</h3>
        </button>
    </div>
</template>
  
<script>
export default {
    name: 'DarkModeButton',
    data() {
        return {
            isDarkMode: true,
        }
    },
    methods: {
        getImageURL() {
            return this.isDarkMode ? '/images/moon.svg' : '/images/light.svg';
        },
        toggleDarkMode() {
            this.isDarkMode = !this.isDarkMode;
            document.body.classList.toggle('dark-mode', this.isDarkMode);
            document.documentElement.setAttribute('data-theme', this.isDarkMode ? 'dark' : 'light');
            localStorage.setItem('darkMode', this.isDarkMode);
        }
    },
    mounted() {
        const darkMode = localStorage.getItem('darkMode');
        if (darkMode !== null) {
            this.isDarkMode = JSON.parse(darkMode);
            document.body.classList.toggle('dark-mode', this.isDarkMode);
        }
    }
}
</script>
  
<style scoped>
button {
    /* border: 1px solid #ccc; */
    padding: 10px 20px;
    cursor: pointer;
}

.dark-mode button {
    background-color: black;
    color: #fff;
}


.div-theme-btn {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: flex-end;
    height: 3.7em;
    padding-right: 1em;
}

.theme-btn {
    border: none;
    border-radius: 100vmin;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 5px 25px;
    justify-content: flex-end;
    width: max-content;
    transition: 0.2s ease-in-out;
    outline: none;
}

.theme-btn>img {
    height: 1.1em;
    margin-right: 0.2em;
}

.theme-btn:hover {
    background-color: var(--theme_button_hover_color);
    cursor: pointer;
    color: var(--theme_button_hover_text_color);
}

.theme_but_text {
    font-family: 'Manrope';
    font-size: 1rem;
    font-weight: 100;
    margin: 0.2em;
}
</style>
  