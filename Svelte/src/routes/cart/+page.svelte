<div class="wrapper">
    <div style="display: flex; flex-direction:row;">
        <img style="width:5rem; margin-right: 1rem;" src="/buttonicons/cart-fill.svg" alt=" "/>
        <h1 style="font-size: 4rem;">КОЛИЧКА</h1>
    </div>
    <div style="width:100%; height:2px; background-color:rgb(66, 69, 73); margin-top:1rem;"></div>
    <ul class="list">
        <li class="liked-item">
            <p>1x</p>
            <img class="itemimg" src='/img/shirt.webp' alt=" "/>
            <h1>Използвана риза</h1>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>7x</p>
            <img class="itemimg" src='/img/clock.jpg' alt=" "/>
            <h1>motherfuckin' clock</h1>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>1x</p>
            <img class="itemimg" src='/img/qke.jpg' alt=" "/>
            <h1>qke :)</h1>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>1x</p>
            <img class="itemimg" src='/img/arab.jpg' alt=" "/>
            <h1>UAE Polo "Halal Arab"</h1>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <a href="/order" class="button">
            <p>ПОРЪЧКА</p>
        </a>
    </ul>
</div>

<style>
    .button:hover {
        background-color: #4a53cd;
        color: #f0f0f0;
    }
    .button {
        margin-left: auto; margin-right: auto;
        background-color: #5560F5;
        width:20rem;
        height:5rem;
        border-radius: 0.5rem;
        font-size: 1.8rem;
        display: flex;
        justify-content: center;
        font-weight: bold;
        align-items: center;
        flex-flow: row;
        text-decoration: none !important;
        color: white;
        transition: color 0.1s ease-in-out, background-color 0.1s ease-in-out;
    }
    .trash {
        filter: brightness(0) saturate(100%) invert(72%) sepia(55%) saturate(5701%) hue-rotate(323deg) brightness(96%) contrast(80%) !important;
        width: 1.6rem; height:1.6rem;
        margin-left: auto;
        cursor: pointer;
        transition: filter 0.1s ease-in-out;
    }
    .trash:hover {
        filter: brightness(0) saturate(100%) invert(72%) sepia(55%) saturate(5701%) hue-rotate(323deg) brightness(96%) contrast(80%) drop-shadow(0 0 3px #ff444488) !important;
    }
    .liked-item > h1 {
        margin-left:2rem;
        font-size: 1.2rem;
    }
    .liked-item > .itemimg {
        filter: none !important;
        height:4.5rem;
        width: 4.5rem;
        object-fit: cover;
        border-radius: 0.5rem;
        margin-left: 2rem;
        transition: height 0.3s ease-in-out, width 0.3s ease-in-out;
    }
    .liked-item > .itemimg:hover {
        height: 10rem;
        width:10rem;
        z-index: 999;
    }
    .liked-item {
        display: flex;
        flex-direction: row;
        width:100%;
        height: 5rem;
        background-color: rgb(49, 51, 56);
        border-radius: 10px;
        align-items: center;
        padding: 2rem;
    }
    .list {
        margin-top: 2rem;
        width:75%;
        height:auto;
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
    }
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .wrapper {
        padding:2rem;
        background-color: rgb(43, 45, 49);
        border: solid 2px rgb(30, 31, 34);
        border-radius: 1rem;
        width: 65%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .wrapper img {
        filter: brightness(0) saturate(100%) invert(28%) sepia(80%) saturate(1257%) hue-rotate(216deg) brightness(113%) contrast(98%);
    }
</style>