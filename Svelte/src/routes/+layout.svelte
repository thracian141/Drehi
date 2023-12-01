<script>
    import Navbar from "./Navbar.svelte";
</script>

<div class="app">
    <Navbar />
    <main>
        <slot/>
    </main>
</div>

<style>
    * {
        font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }
    main {
        display: flex;
        width: 100%;
        height: 100%;
        flex-direction: column;
    }
    .app {
        display: flex;
        flex-direction: column;
        height:100vh;
        width:100vw;
        background-color: rgb(49,51,56);
        color:white;
    }
</style>