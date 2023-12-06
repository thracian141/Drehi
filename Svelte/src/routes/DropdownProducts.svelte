<script>
    export let categoryHovered = '';
</script>

<div class="wrapper">
    {#if categoryHovered}
        <div class="category">
            <h3>Якета</h3>
            <p>хубави</p>
            <p>грозни</p>
            <p>красиви</p>
            <p>прекрасни</p>
        </div>
        <div class="category">
            <h3>Панталони</h3>
            <p>1 крачол</p>
            <p>2 крачол</p>
            <p>3 крачол</p>
            <p>4 крачол</p>
        </div>
        <div class="category">
            <h3>Ризи</h3>
            <p>хубави</p>
            <p>грозни</p>
            <p>красиви</p>
            <p>прекрасни</p>
        </div>
        <div class="category">
            <h3>Блузи</h3>
            <p>хубави</p>
            <p>грозни</p>
            <p>красиви</p>
            <p>прекрасни</p>
        </div>
        <div class="category">
            <h3>Копчета</h3>
            <p>големи</p>
            <p>огромни брат</p>
            <p>малки</p>
            <p>рандом</p>
        </div>
    {/if}
</div>

<style>
    h3 {
        align-self: center;
        font-size: 2rem;
        font-weight: 600;
    }
    p {
        font-size: 1.2rem;
        font-weight: 400;
    }
    .category {
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        gap: 0.5rem;
        margin-bottom: 1rem;
    }
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .wrapper {
        display: flex;
        flex-flow: row;
        overflow: hidden;
        flex-wrap: wrap;
        justify-content:space-between;
        align-items: flex-start;
        width:100%;
        height: 100%;
        max-height: 26rem;
        padding: 1rem;
    }
</style>