<section id="slideshow">
    <div class="entire-content">
      <div class="content-carrousel">
        <figure class="shadow">
            <img src="src/lib/img/shoes.png" alt=" "/>
            <div class="figure-label-bg">
                <span>Thomas Jefferson</span>
                <span>Thomas Jefferson 1866's</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/specialki.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>Кърджалийки</span>
                <span>Кърджали "Специалки"</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/qke.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>Vasil Petrov</span>
                <span>Vasil "Versace"</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/hookah.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>Halal Albania</span>
                <span>Качествено албанско наргиле</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/clock.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>Fucking Clock</span>
                <span>Motherfuckin' CLOCK!!</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/arab.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>UAE Polo</span>
                <span>Halal</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/korset.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>Nike</span>
                <span>Мъжки Корсет Nike</span>
            </div>
        </figure>
        <figure class="shadow">
            <img src="src/lib/img/dyrva.jpg" alt=" "/>
            <div class="figure-label-bg">
                <span>Дърва</span>
                <span>за огрев</span>
            </div>
        </figure>
  </div>
</div>
</section>

<style>
    .figure-label-bg {
        position:absolute;
        width:100%;
        height:30%;
        background-color: #000000aa;
        z-index: 1;
        bottom:0;
        left:0;
        display: flex;
        flex-direction: column;
        padding: 0.5rem;
    }
    .figure-label-bg > span:first-child {
        color:#fff;
        font-size: 1.4rem;
    }
    .figure-label-bg > span:last-child {
        color:orange;
        font-size: 0.8rem;
    }

    * {
        margin: 0;
        padding: 0;
    }
    #slideshow {
        height: 100%;
        width: 100%;
        box-sizing: border-box;
        display: flex;
        justify-content: flex-start;
        align-items: center;
    }
    .entire-content {
        margin: auto; margin-top: 0;
        width: 18rem;
        perspective: 1000px;
        position: relative;
        padding-top: 80px;
    }
    .content-carrousel {
        width: 18rem;
        position: absolute;
        float: right;
        animation: rotar 25s infinite linear;
        transform-style: preserve-3d;
    }
    .content-carrousel:hover {
        animation-play-state:paused;
        cursor: pointer;
    }
    .content-carrousel figure {
        width: 18rem;
        height: 12rem;
        border-radius: 0.5rem;
        overflow: hidden;
        position: absolute;
    }
    .content-carrousel figure:nth-child(1) {
    transform: rotateY(0deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(2) {
    transform: rotateY(45deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(3) {
    transform: rotateY(90deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(4) {
    transform: rotateY(135deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(5) {
    transform: rotateY(180deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(6) {
    transform: rotateY(225deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(7) {
    transform: rotateY(270deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(8) {
    transform: rotateY(315deg) translateZ(26rem); 
    } .content-carrousel figure:nth-child(9) {
    transform: rotateY(360deg) translateZ(26rem); 
    } 

    .content-carrousel  figure {
        transition: transform 0.2s ease-in-out;
    }
    .content-carrousel figure:nth-child(1):hover {
    transform: rotateY(0deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(2):hover {
    transform: rotateY(45deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(3):hover {
    transform: rotateY(90deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(4):hover {
    transform: rotateY(135deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(5):hover {
    transform: rotateY(180deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(6):hover {
    transform: rotateY(225deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(7):hover {
    transform: rotateY(270deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(8):hover {
    transform: rotateY(315deg) translateZ(34rem); 
    } .content-carrousel figure:nth-child(9):hover {
    transform: rotateY(360deg) translateZ(34rem); 
    } 
    .content-carrousel img {
        image-rendering: auto;
        transition: all 300ms;
        width: 100%;
        height: 100%;
    }
    .content-carrousel img:hover {
        transform: scale(1.2);
        transition: all 300ms;
    }

    @keyframes rotar {
        from {
            transform: rotateY(360deg);
        } to {
            transform: rotateY(0deg);
        }
    }
</style>