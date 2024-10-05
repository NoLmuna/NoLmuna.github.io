<script>
    import "../app.css"; // Import your styles

    let isDarkMode = true;

    function toggleTheme() {
        isDarkMode = !isDarkMode;
    }
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous">
    <link href="https://fonts.googleapis.com/css2?family=Comfortaa:wght@300..700&family=Manrope:wght@200..800&display=swap" rel="stylesheet">
</svelte:head>

<style>
    :global(html), :global(body) {
    margin: 0;
    padding: 0;
    height: 100%;
    overflow-x: hidden; 
    font-family: 'Comfortaa', sans-serif;
}

.main-container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    background-color: var(--background);
    color: var(--text-color);
}

.navbar {
    display: flex;
    gap: 1rem;
    justify-content: flex-end;
    align-items: center;
    padding: 1rem 2rem;
    border-bottom: 1px solid var(--text-color);
}

.navbar a {
    text-decoration: none;
    color: inherit;
}

.theme-toggle {
    cursor: pointer;
    font-size: 1.5rem;
    background: none;
    border: none;
    color: inherit;
    padding: 0.5rem;
}

.main-content {
    flex: 1; 
    padding: 2rem; 
    display: flex; 
    flex-direction: column; 
    gap: 1rem; 
    justify-content: center;
    align-items: center;
    background-color: var(--background);
    color: var(--text-color);
}

/* Dark Theme */
:global(.dark-mode) {
    --background: black;
    --text-color: white;
}

/* Light Theme */
:global(.light-mode) {
    --background: white;
    --text-color: black;
}
</style>

<div class={isDarkMode ? 'dark-mode main-container' : 'light-mode main-container'}>
    <div class="navbar">
        <a href="/" class="mr-auto font-bold">Noel "pogi" Mateo</a>
        <a href="/">Home</a>
        <a href="/portfolio">Portfolio</a>
        <a href="/about">About</a>
        <a href="/contact">Contact</a>

        <button 
            class="theme-toggle" 
            on:click={toggleTheme}
            aria-label="Toggle dark and light mode"
        >
            {#if isDarkMode}
                🌙
            {:else}
                ☀️
            {/if}
        </button>
    </div>

    <main class="main-content">
        <slot></slot>
    </main>
</div>
