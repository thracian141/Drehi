<script lang="ts">
    import Carousel from "./Carousel.svelte";   
</script>

<div class="wrapper" style="overflow: hidden;">
    <a href="/" class="specialoffer">
        <div class="textbg">
            <div class="selected"></div>
            <span>СПЕЦИАЛНА ОФЕРТА!</span>
            <span style="color: orange; font-size:1.1rem;">Оферта №1</span>
        </div>
    </a>
    <div style="display: flex; flex-direction:column; width:70%; height:100%;">
        <div class="central">
            <Carousel />
        </div>
        <div class="centerbottom">
            <h1 style="writing-mode: vertical-rl; text-orientation: upright; letter-spacing:-10px;">ПРОМО</h1>
            <!-- svelte-ignore a11y-missing-attribute -->
            <a class="promo">
                <h1>-15%</h1>
                <p>на всички терлици</p>
            </a>
            <!-- svelte-ignore a11y-missing-attribute -->
            <a class="promo">
                <h1>-20%</h1>
                <p>на Vasil Versace</p>
            </a>
            <!-- svelte-ignore a11y-missing-attribute -->
            <a class="promo">
                <h1>-30%</h1>
                <p>комплект 3 броя обувки</p>
            </a>
            <h1 style="writing-mode: vertical-rl; text-orientation: upright; letter-spacing:-10px;">ПРОМО</h1>
        </div>
    </div>
        <a href="/" class="specialoffer">
        <div class="textbg">
            <div class="selected"></div>
            <span>СПЕЦИАЛНА ОФЕРТА!</span>
            <span style="color: orange; font-size:1.1rem;">Оферта №2</span>
        </div>
    </a>
</div>


<style>
    .promo {
        display: flex;
        flex-direction: column;
        color:white;
        border: solid white;
        border-width: 0 1px 0 1px;
        height:90%;
        width: 20%;
        justify-content: center;
        align-items: center;
        font-size: 1.4rem;
        cursor: pointer;
        transition: background-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
    }
    .promo > h1 {
        margin: 0;
        padding: 0;
    }
    .promo:hover {
        background-color: #ffffff22;
        box-shadow: 0 0 12px 5px #ffffff22;
    }
    .centerbottom {
        display: flex;
        flex-direction: row;
        background-color: #00000044;
        color:orange;
        height:30%;
        width:100%;
        font-size: 1rem;
        justify-content: space-between;
        align-items: center;
    }
    .central {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width:100%;
        height:75%;
    }
    .selected {
        display: flex;
        background-color: orange;
        width:15%;
        height:0.3rem;
        z-index: 888;
        transition: width 0.4s ease-in-out;
        margin-bottom: 0.5rem;
        margin-left: 0.5rem;
        margin-top: 1rem;
    }
    .textbg > span {
    font-size:auto;
    margin: 0;
    padding: 0;
    font-size: 1.35rem;
    line-break:normal;
    padding-left: 0.5rem; padding-right: 1rem;
    }
    .textbg {
    position: absolute;
    background-color: #000000aa;
    width:100%;
    height:30%;
    display: flex;
    flex-direction: column;
    bottom: 0%;
    }
    .wrapper {
    display:flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;
    flex-direction: row;
    width:100%;
    height:100%;
    }
    .specialoffer {
    background-image: url("/img/offer1.jpg");
    height: 100%;
    width: 15%;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    color:white;
    text-decoration: none;
    box-shadow:inset 0 0 0 2000px rgba(0,0,0,0.5);
    transition: box-shadow 0.2s ease-in-out;
    display: flex;
    flex-direction: column;
    text-align: left;
    position: relative;
    overflow: hidden;
    }
    .specialoffer:last-child {
    background-image: url("/img/offer2.jpg");
    }
    .specialoffer:hover {
    box-shadow: inset 0 0 0 2000px rgba(0,0,0,0);
    }
    .specialoffer:hover > .textbg > .selected {
    width:80%;
    }
</style>
