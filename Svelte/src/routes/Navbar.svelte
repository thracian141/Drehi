<div class="topnav">
    <div style="display: flex; flex-direction:row; gap:2rem;">
        <a>Доставка до Овча Купел</a>
        <a>2-часов срок за връщане</a>
        <a>Връзка с Бойко Борисов</a>
    </div>
    <div style="display:flex; flex-direction:row; align-items:center; gap:0.3rem;">
        <img src="/buttonicons/envelope-at-fill.svg" alt="contact" style="width:1.2rem; height:1.2rem; filter: brightness(0) saturate(100%) invert(99%) sepia(1%) saturate(6197%) hue-rotate(301deg) brightness(110%) contrast(101%);" />
        <p>vasiljavaskriptin@gov.ru</p>
    </div>
</div>
<nav>
    <div id="logodiv">
        <img src="/logo.webp" alt="logo" id="logo"/>
        <h1 style="font-size: 3rem; position:absolute; right:0%;">рехи</h1>
    </div>

    <div style="display: flex; flex-direction:row; background-color:#5663F7; align-items:center; border-radius:0.6rem; width:41.5rem;">
        <input type="text" id="finder" placeholder="Търси Dрехи..." />
        <img src="/buttonicons/search.svg" alt="search" id="finderico"/>
    </div>    

    <div style="display:flex;flex-direction:row; gap:1.2rem;">
        <a href="/" class="navbutton">
            <img src="/buttonicons/heart-half.svg" alt="liked items"/>
            <p style="margin:0; padding:0;">ХАРЕСАНИ</p>
        </a>
        <a href="/" class="navbutton">
            <img src="/buttonicons/cart-fill.svg" alt="liked items"/>
            <p style="margin:0; padding:0;">КОЛИЧКА</p>
        </a>
        <a href="/" class="navbutton">
            <img src="/buttonicons/person.svg" alt="liked items"/>
            <p style="margin:0; padding:0;">ПРОФИЛ</p>
        </a>
    </div>
</nav>

<style>
    #finder {
        border-radius: 0.5rem;
        background-color: rgb(30,31,34);
        width: 36rem;
        height:4rem;
        border: none;
        font-size: 1.4rem;
        padding: 0 0.6rem;
        color:white;
        transition: filter 0.2s ease-in-out;
    }
    #finder:focus {
        outline: none;
        filter:drop-shadow(0px 0px 4px rgba(255, 255, 255, 0.5));
    }
    #finder::placeholder {
        color: rgb(127,133,141);
    }
    #finderico {
        margin-left: 1rem;
        height: 2rem;
        width: auto;
        filter: brightness(0) saturate(100%) invert(100%) sepia(100%) saturate(38%) hue-rotate(321deg) brightness(110%) contrast(110%);
        transition: filter 0.1s ease-in-out;
    }
    #finderico:hover {
        cursor: pointer;
        filter: brightness(0) saturate(100%) invert(100%) sepia(100%) saturate(38%) hue-rotate(321deg) brightness(110%) contrast(110%) drop-shadow(0px 0px 4px rgba(255, 255, 255, 0.8));
    }
    .navbutton {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap:0.3rem;
        text-decoration: none;
        transition: filter 0.1s ease-in-out;
        filter: brightness(0) saturate(100%) invert(78%) sepia(12%) saturate(362%) hue-rotate(160deg) brightness(85%) contrast(87%);
    }
    .navbutton > p {
        font-size: 1.2rem;
    }
    .navbutton > img {
        height: 1.7rem;
        width:auto;
    }
    .navbutton:hover {
        filter: brightness(0) saturate(100%) invert(100%) sepia(100%) saturate(38%) hue-rotate(321deg) brightness(110%) contrast(110%) drop-shadow(0px 0px 3px rgba(255, 255, 255, 0.65));;
    }
    #logodiv {
        display: flex;
        flex-direction: row;
        align-items: center;
        position: relative;
        width: 12.3rem;
    }
    #logo {
        height:6.5rem;
        width: auto;
        margin:0;
        position: absolute;
        left: 0;
    }
    p {
        color:white;
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
        box-shadow: rgba(0, 0, 0, 0.4) 0px 0px 4px 1px;
        z-index: 999;
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
        justify-content: space-between;
        align-items: center;
        padding: 0 2rem;
        border-bottom:1px solid #424549dd;
    }
</style>
