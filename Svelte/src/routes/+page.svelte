<script lang="ts">
    let thomas = "src/lib/img/thomas.png";
</script>

<div class="wrapper" style="overflow: hidden;">
  <a href="/" class="specialoffer">
    <div class="textbg">
      <div class="selected"></div>
      <span>СПЕЦИАЛНА ОФЕРТА!</span>
      <span style="color: orange; font-size:1.1rem;">Оферта №1</span>
    </div>
  </a>
  <div class="container">
    <div class="carousel">
      <a href="/" class="carousel__face"><span>Thomas Jefferson 1876's</span></a>
      <a href="/" class="carousel__face"><span>Кърджали "Специалки"</span></a>
      <a href="/" class="carousel__face"><span>Vasil Versace</span></a>
      <a href="/" class="carousel__face"><span>Дърва за огрев</span></a>
      <a href="/" class="carousel__face"><span>UAE Polo</span></a>
      <a href="/" class="carousel__face"><span>Албанско Наргиле</span></a>
      <a href="/" class="carousel__face"><span>Мъжки Nike Корсет</span></a>
      <a href="/" class="carousel__face"><span>Водолазен костюм Calvin Klein</span></a>
      <a href="/" class="carousel__face"><span>Motherfuckin' CLOCK</span></a>
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
    display: flex;
    flex-direction: row;
    width:100%;
    height:100%;
  }
  .specialoffer {
    background-image: url("src/lib/img/offer1.jpg");
    height: auto;
    width: 15%;
    background-repeat: no-repeat;
    background-size: cover;
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
  .container {
    position: relative;
    width: 300px;
    margin: 5% auto 0 auto;
    perspective: 1600px;
  }

  .carousel {
    position: absolute;
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    animation: rotate360 20s infinite forwards linear;
  }
  .carousel__face { 
    position: absolute;
    width: 300px;
    height: 187px;
    top: 20px;
    left: 10px;
    right: 10px;
    background-size: cover;
    box-shadow:inset 0 0 0 2000px rgba(0,0,0,0.5);
    display: flex;
    transition:box-shadow 0.1s ease-in-out;
    border-radius: 0.5rem;
  }
  .carousel__face, .carousel__face:visited {
      color: white;
      text-decoration: none;
  }
  .carousel__face:hover {
      box-shadow: inset 0 0 0 2000px rgba(0,0,0,0.1);
  }

  span {
    margin: auto;
    font-size: 2rem;
  }

  .carousel__face:nth-child(1) {
    background-image: url("src/lib/img/shoes.png");
    transform: rotateY(  0deg) translateZ(430px); }
  .carousel__face:nth-child(2) { 
      background-image: url("src/lib/img/specialki.jpg");
      transform: rotateY( 40deg) translateZ(430px); }
  .carousel__face:nth-child(3) {
      background-image: url("src/lib/img/qke.jpg");
    transform: rotateY( 80deg) translateZ(430px); }
  .carousel__face:nth-child(4) {
      background-image: url("src/lib/img/dyrva.jpg");
    transform: rotateY(120deg) translateZ(430px); }
  .carousel__face:nth-child(5) { 
      background-image: url("src/lib/img/arab.jpg");
  transform: rotateY(160deg) translateZ(430px); }
  .carousel__face:nth-child(6) { 
      background-image: url("src/lib/img/hookah.jpg");
  transform: rotateY(200deg) translateZ(430px); }
  .carousel__face:nth-child(7) { 
      background-image: url("src/lib/img/korset.jpg");
  transform: rotateY(240deg) translateZ(430px); }
  .carousel__face:nth-child(8) {
      background-image: url("src/lib/img/vodolazi.jpg");
    transform: rotateY(280deg) translateZ(430px); }
  .carousel__face:nth-child(9) {
      background-image: url("src/lib/img/clock.jpg");
    transform: rotateY(320deg) translateZ(430px); }



  @keyframes rotate360 {
    from {
      transform: rotateY(0deg);
    }
    to {
      transform: rotateY(-360deg);
    }
  }
</style>
