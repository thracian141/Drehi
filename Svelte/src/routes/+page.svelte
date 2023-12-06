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
            <h1 style="writing-mode: vertical-rl; text-orientation: upright; letter-spacing:-10px;">ПРОМО!</h1>
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
    .centerbottom {
        display: flex;
        flex-direction: row;
        background-color: #00000044;
        height:25%;
        width:100%;
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
    background-image: url("src/lib/img/offer1.jpg");
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
    background-image: url("src/lib/img/offer2.jpg");
    }
    .specialoffer:hover {
    box-shadow: inset 0 0 0 2000px rgba(0,0,0,0);
    }
    .specialoffer:hover > .textbg > .selected {
    width:80%;
    }
</style>
