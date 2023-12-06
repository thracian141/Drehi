<div class="wrapper">
    <div style="display: flex; flex-direction:row;">
        <img style="width:5rem; margin-right: 1rem;" src="/buttonicons/heart-box.svg" alt=" "/>
        <h1 style="font-size: 4rem;">ХАРЕСАНИ АРТИКУЛИ</h1>
        <img style="width:5rem; margin-left: 1rem;" src="/buttonicons/archive-fill.svg" alt=" "/>
    </div>
    <div style="width:100%; height:2px; background-color:rgb(66, 69, 73); margin-top:1rem;"></div>
    <ul class="list">
        <li class="liked-item">
            <p>3x</p>
            <img class="itemimg" src='src/lib/img/obuvki.png' alt=" "/>
            <h1>Калцони</h1>
            <span style="color:#ff8888">Няма налична промоция!</span>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>1x</p>
            <img class="itemimg" src='src/lib/img/shirt.webp' alt=" "/>
            <h1>Използвана риза</h1>
            <span style="color:#ff8888">Няма налична промоция!</span>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>7x</p>
            <img class="itemimg" src='src/lib/img/clock.jpg' alt=" "/>
            <h1>motherfuckin' clock</h1>
            <span style="color:#ff8888">Няма налична промоция!</span>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>1x</p>
            <img class="itemimg" src='src/lib/img/qke.jpg' alt=" "/>
            <h1>qke :)</h1>
            <span style="color:#88ff88">Има налична промоция!</span>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <li class="liked-item">
            <p>1x</p>
            <img class="itemimg" src='src/lib/img/arab.jpg' alt=" "/>
            <h1>UAE Polo "Halal Arab"</h1>
            <span style="color:#88ff88">Има налична промоция!</span>
            <img src='/buttonicons/trash-fill.svg' alt=" " class="trash"/>
        </li>
        <h2 style="margin-left: auto;">Имате 5 харесани артикула</h2>
    </ul>
</div>

<style>
    span {
        margin-left: auto;
    }
    .trash {
        filter: brightness(0) saturate(100%) invert(72%) sepia(55%) saturate(5701%) hue-rotate(323deg) brightness(96%) contrast(80%) !important;
        width: 1.6rem; height:1.6rem;
        margin-left: 7.5rem;
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
        height:100%;
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