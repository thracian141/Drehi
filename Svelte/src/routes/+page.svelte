<script lang="ts">
    let thomas = "src/lib/img/thomas.png";
</script>

<div class="container">
    <div class="carousel">
      <a href="/" class="carousel__face"><span>Thomas Jefferson 1876's</span></a>
      <a href="/" class="carousel__face"><span>Кърджали "Специалки"</span></a>
      <a href="/" class="carousel__face"><span>Vasil Versace</span></a>
      <a href="/" class="carousel__face"><span>Дърва за огрев</span></a>
      <a href="/" class="carousel__face"><span>UAE Polo</span></a>
      <a href="/" class="carousel__face"><span>Hamburger</span></a>
      <a href="/" class="carousel__face"><span>Мъжки Nike Корсет</span></a>
      <a href="/" class="carousel__face"><span>Водолазен костюм Calvin Klein</span></a>
      <a href="/" class="carousel__face"><span>Motherfuckin' CLOCK</span></a>
    </div>
  </div>

<style>
.container {
  position: relative;
  width: 320px;
  margin: 1rem auto 0 auto;
  perspective: 1100px;
}

.carousel {
  position: absolute;
  width: 100%;
  height: 100%;
  transform-style: preserve-3d; 
  animation: rotate360 40s infinite forwards linear;
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
}
.carousel__face, .carousel__face:visited {
    color: white;
    text-decoration: none;
}
.carousel__face:hover {
    box-shadow: inset 0 0 0 2000px rgba(0,0,0,0.2);
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
    background-image: url("src/lib/img/hamburg.webp");
 transform: rotateY(200deg) translateZ(430px); }
.carousel__face:nth-child(7) { 
    background-image: url("src/lib/img/corset.avif");
 transform: rotateY(240deg) translateZ(430px); }
.carousel__face:nth-child(8) {
    background-image: url("src/lib/img/shoes.png");
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
