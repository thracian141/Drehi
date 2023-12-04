<script lang="ts">
    let thomas = 'src/lib/img/thomas.png';
</script>

<div class="carousel">
    <a style="filter:invert(100%); height:12rem;" href="/"><img src="/buttonicons/chevron-left.svg" alt=""></a>
    <button>right</button>
    <div class="current-image">
        <img src={thomas} alt="" />
        <span><b>ТЕСТОВО СЪОБЩЕНИЕ</b></span>
    </div>
</div>

<style>
    .carousel {
        background-color: rgb(49,51,56);
        background-color: red;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        width: 80rem;
        height:32rem;

    }
    .current-image {
        display: flex;
        flex-direction: column;
        height:100%;
        position: relative;
    }
    .current-image > img {
        height:100%;
        width:auto;
        z-index: 1;
    }
    .current-image > span {
        position: absolute;
        bottom:0%;
        left:50%;
        transform: translateX(-50%);
        width:100%;
        height:20%;
        background-color: rgba(0,0,0,0.4);
        backdrop-filter: blur(4px);
        text-align: center;
        font-size: 2.4rem;
        line-height: 6rem;
        z-index: 2;
    }
</style>