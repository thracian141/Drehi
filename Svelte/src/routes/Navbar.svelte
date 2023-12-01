<div class="topnav">
    <div style="display: flex; flex-direction:row; gap:2rem;">
        <a>Доставка до Овча Купел</a>
        <a>2-часов срок за връщане</a>
        <a>Връзка с Бойко Борисов</a>
    </div>


    <div style="display: flex; flex-direction:row; align-items:center; gap:0.3rem;">
        <img src="/envelope-at-fill.svg" />
        <p>vasiljavaskriptin@gov.ru</p>
    </div>
</div>
<nav>
    <img src="/logo.webp" alt="logo" id="logo"/>
    <h1 style="font-size: 2rem">рехи</h1>

    <input type="text" id="finder" placeholder="Търси Dрехи..."/>
</nav>

<style>
    #finder {
        border-radius: 0.5rem;
        background-color: rgb(30,31,34);
        width: 26rem;
        height:3rem;
        border: none;
        font-size: 1.1rem;
        padding: 0 0.6rem;
        color:white;
    }
    #finder::placeholder {
        color: rgb(127,133,141);
    }
    #logo {
        height:5rem;
    }
    p {
        color:white;
    }
    div > img {
        filter: brightness(0) saturate(100%) invert(99%) sepia(1%) saturate(6197%) hue-rotate(301deg) brightness(110%) contrast(101%);
        height: 1.2rem;
        width: 1.2rem;
    }
    .topnav {
        display: flex;
        flex-direction: row;
        color: rgb(128,132,142);
        line-height: 3rem;
        background-color: rgb(30,31,34);
        height: 3rem;
        padding: 0 2rem;
        align-items: center;
        justify-content: space-between;
    }
    .topnav > div > a {
        transition: color 0.1s ease-in-out;
        cursor:grab;
    }
    .topnav > div > a:hover {
        color: white;
    }
    nav {
        display: flex;
        flex-direction: row;
        height: 10rem;
        flex-grow: 1;
        background-color: rgb(43,45,49);
        align-items: center;
        padding: 0 0 0 2rem;
    }
</style>
