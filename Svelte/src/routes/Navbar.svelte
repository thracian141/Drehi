<script lang="ts">
    import { fade, slide } from "svelte/transition";
    import DropdownProducts from "./DropdownProducts.svelte";
    import { writable } from "svelte/store";

    let categoryHovered = "";
    let lastHoveredIndex = -1;

    const dropdownOpen = writable(false);
    let hovered = [false, false, false, false, false, false, false];
    let inCurrentButton = false;
    let hasEnteredDropdown = false;

    function handleMouseEnter(index : number) {
        inCurrentButton = true;
        hovered[index] = true;
        dropdownOpen.set(true);
        lastHoveredIndex = index;
    }

    function handleMouseLeave(index : number) {
        inCurrentButton = false;
        hovered[index] = false;
        setTimeout(() => {
            if (!hasEnteredDropdown && !inCurrentButton) {
                dropdownOpen.set(false);
            }
        }, 300);
    }

    function handleDropdownMouseEnter() {
        inCurrentButton = true;
        hasEnteredDropdown = true;
        dropdownOpen.set(true);
        if (lastHoveredIndex !== -1) {
            hovered[lastHoveredIndex] = true;
        }
    }

    function handleDropdownMouseLeave() {
        inCurrentButton = false;
        hasEnteredDropdown = false;
        dropdownOpen.set(false);
        hovered = hovered.map(() => false);
        if (lastHoveredIndex !== -1) {
            hovered[lastHoveredIndex] = false;
        }
    }
</script>

<div class="topnav">
    <div style="display: flex; flex-direction:row; gap:2rem;">
        <a>Доставка до Овча Купел</a>
        <a>2-часов срок за връщане</a>
        <a href="https://www.facebook.com/boyko.borissov.7/?locale=bg_BG"
            >Връзка с Бойко Борисов</a
        >
    </div>
    <div
        style="display:flex; flex-direction:row; align-items:center; gap:0.3rem;">
        <img
            src="/buttonicons/envelope-at-fill.svg"
            alt="contact"
            style="width:1.2rem; height:1.2rem; filter: brightness(0) saturate(100%) invert(99%) sepia(1%) saturate(6197%) hue-rotate(301deg) brightness(110%) contrast(101%);"/>
        <p>vasiljavaskriptin@gov.ru</p>
    </div>
</div>
<nav>
    <a href="/" style="display: flex; flex-direction:row; align-items:center; width:17.5rem; position:relative;">
        <img src="/logo.webp" alt="logo" style="max-height: 7.2rem; position:absolute; left:0%;"/>
        <img src="/rehi.PNG" alt=" " style="max-height: 4.5rem; margin-top:1.5rem; position:absolute; right:0%; z-index:1; "/>
    </a>

    <div
        style="display: flex; flex-direction:row; background-color:#5663F7; align-items:center; border-radius:0.6rem; width:41.5rem;">
        <input type="text" id="finder" placeholder="Търси Dрехи..." />
        <img src="/buttonicons/search.svg" alt="search" id="finderico" />
    </div>

    <div style="display:flex;flex-direction:row; gap:1.2rem;">
        <a href="/liked" class="navbutton">
            <img src="/buttonicons/heart-half.svg" alt="liked items" />
            <p style="margin:0; padding:0;">ХАРЕСАНИ</p>
            <div class="circle">2</div>
        </a>
        <a href="/cart" class="navbutton">
            <img src="/buttonicons/cart-fill.svg" alt="liked items" />
            <p style="margin:0; padding:0;">КОЛИЧКА</p>
        </a>
        <a href="/" class="navbutton">
            <img src="/buttonicons/person.svg" alt="liked items" />
            <p style="margin:0; padding:0;">ПРОФИЛ</p>
        </a>
    </div>
</nav>
<div class="bottomnav">
    <button class:bottom-nav-button-hover={hovered[0]}
        on:mouseenter={() => {handleMouseEnter(0); categoryHovered = "Мъжки"}}
        on:mouseleave={() => handleMouseLeave(0)}
        class="bottom-nav-button">
        МЪЖКИ
        <div class="bottomhider"></div>
    </button>
    <button class:bottom-nav-button-hover={hovered[1]}
        on:mouseenter={() => {handleMouseEnter(1); categoryHovered = "Дамски"}}
        on:mouseleave={() => handleMouseLeave(1)}
        class="bottom-nav-button"
    >
        ДАМСКИ
        <div class="bottomhider"></div>
    </button>
    <button class:bottom-nav-button-hover={hovered[2]}
        on:mouseenter={() => {handleMouseEnter(2); categoryHovered = "Детски"}}
        on:mouseleave={() => handleMouseLeave(2)}
        class="bottom-nav-button"
    >
        ДЕТСКИ
        <div class="bottomhider"></div>
    </button>
    <button class:bottom-nav-button-hover={hovered[3]}
        on:mouseenter={() => {handleMouseEnter(3); categoryHovered = "Аксесоари"}}
        on:mouseleave={() => handleMouseLeave(3)}
        class="bottom-nav-button"
    >
        АКСЕСОАРИ
        <div class="bottomhider"></div>
    </button>
    <button class:bottom-nav-button-hover={hovered[4]}
        on:mouseenter={() => {handleMouseEnter(4); categoryHovered = "Мерч"}}
        on:mouseleave={() => handleMouseLeave(4)}
        class="bottom-nav-button">
        MERCH
        <div class="bottomhider"></div>
    </button>
    <button class:bottom-nav-button-hover={hovered[5]}
        on:mouseenter={() => {handleMouseEnter(5); categoryHovered = "Марки"}}
        on:mouseleave={() => handleMouseLeave(5)}
        class="bottom-nav-button">
        МАРКИ
        <div class="bottomhider"></div>
    </button>
    <button class:bottom-nav-button-hover={hovered[6]}
        on:mouseenter={() => {handleMouseEnter(6); categoryHovered = "Други"}}
        on:mouseleave={() => handleMouseLeave(6)}
        class="bottom-nav-button">
        ДРУГИ
        <div class="bottomhider"></div>
    </button>
    {#if $dropdownOpen}
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <div in:slide={{ duration: 800 }} out:slide={{ duration: 400 }}
        class="bottomnav-dropdown" on:mouseenter={handleDropdownMouseEnter} on:mouseleave={handleDropdownMouseLeave}>
            <DropdownProducts {categoryHovered}/>
        </div>
    {/if}
</div>

<style>
    #logodiv {
        transition: filter 0.1s ease-in-out;
    }
    #logodiv:hover {
        cursor: pointer;
        filter: drop-shadow(0px 0px 4px rgba(255, 255, 255, 0.8));
    }
    .circle {
        background-color: #ff8888 !important;
        border-radius: 100%;
        color: white !important;
        font-size: 1rem;
        width: 1.4rem;
        height: 1.4rem;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        top:-15%; right:20%;
        font-weight: bolder;
        filter:none !important;
    }
    .bottomnav-dropdown {
        position: absolute;
        top: 100%;
        background-color: rgb(43, 45, 49);
        width:60%;
        max-height: 26rem;
        display: flex;
        flex-direction: row;
        outline: #5663f7 solid 3px;
        border-radius: 0 0 0.3rem 0.3rem;
        z-index: 500;
    }
    .bottomhider {
        opacity: 0;
        display: flex;
        background-color: rgb(43, 45, 49);
        height: 7px;
        width: 100%;
        position: absolute;
        bottom: -3px;
        left: 0;
        z-index: 999;
    }
    .bottom-nav-button {
        display: flex;
        flex-direction: column;
        height: 100%;
        flex-grow: 1;
        border-radius: 0.3rem;
        background-color: rgb(30, 31, 34);
        border: none;
        transition: filter 0.1s ease-in-out;
        align-items: center;
        justify-content: center;
        color: rgb(128, 132, 142);
        font-size: 1.4rem;
        font-weight: bold;
        position: relative;
    }
    .bottom-nav-button-hover {
        z-index: 888;
        background-color: rgb(43, 45, 49);
        cursor: pointer;
        outline: #5663f7 solid 3px;
    }
    .bottom-nav-button-hover > .bottomhider {
        opacity: 1;
    }
    .bottomnav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        background-color: rgb(30, 31, 34);
        flex-grow: 1;
        height: 6rem;
        padding-left: 20%; padding-right: 20%;
        box-shadow: rgba(0, 0, 0, 0.2) 0px -2px 3px 0.5px;
        border-bottom: 1px solid #424549dd;
        position: relative;
    }
    #finder {
        border-radius: 0.5rem;
        background-color: rgb(30, 31, 34);
        width: 36rem;
        height: 4rem;
        border: none;
        font-size: 1.4rem;
        padding: 0 0.6rem;
        color: white;
        transition: filter 0.2s ease-in-out;
    }
    #finder:focus {
        outline: none;
        filter: drop-shadow(0px 0px 4px rgba(255, 255, 255, 0.5));
    }
    #finder::placeholder {
        color: rgb(127, 133, 141);
    }
    #finderico {
        margin-left: 1rem;
        height: 2rem;
        width: auto;
        filter: brightness(0) saturate(100%) invert(100%) sepia(100%)
            saturate(38%) hue-rotate(321deg) brightness(110%) contrast(110%);
        transition: filter 0.1s ease-in-out;
    }
    #finderico:hover {
        cursor: pointer;
        filter: brightness(0) saturate(100%) invert(100%) sepia(100%)
            saturate(38%) hue-rotate(321deg) brightness(110%) contrast(110%)
            drop-shadow(0px 0px 4px rgba(255, 255, 255, 0.8));
    }
    .navbutton {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 0.3rem;
        text-decoration: none;
        position: relative;
        transition: filter 0.1s ease-in-out;
    }
    .navbutton > p {
        font-size: 1.2rem;
        filter: brightness(0) saturate(100%) invert(78%) sepia(12%)
            saturate(362%) hue-rotate(160deg) brightness(85%) contrast(87%);
    }
    .navbutton > img:first-child {
        height: 1.7rem;
        width: auto;
        filter: brightness(0) saturate(100%) invert(78%) sepia(12%)
            saturate(362%) hue-rotate(160deg) brightness(85%) contrast(87%);
    }
    .navbutton:hover {
        filter: brightness(0) saturate(100%) invert(100%) sepia(100%)
            saturate(38%) hue-rotate(321deg) brightness(110%) contrast(110%)
            drop-shadow(0px 0px 3px rgba(255, 255, 255, 0.65));
    }
    #logodiv {
        display: flex;
        flex-direction: row;
        align-items: center;
        position: relative;
        width: 11.5rem;
    }
    #logo {
        height: 5.5rem;
        width: auto;
        margin: 0;
        position: absolute;
        left: 0;
    }
    p {
        color: white;
    }
    .topnav {
        display: flex;
        flex-direction: row;
        color: rgb(128, 132, 142);
        line-height: 3rem;
        background-color: rgb(30, 31, 34);
        height: 2.6rem;
        padding: 0 2rem;
        align-items: center;
        justify-content: space-between;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 0px 4px 1px;
        z-index: 999;
        border-bottom: 1px solid #424549dd;
    }
    .topnav > div > a {
        color: rgb(128, 132, 142);
        transition: color 0.1s ease-in-out;
        cursor: grab;
        text-decoration: none !important;
    }
    .topnav > div > a:hover {
        color: white !important;
    }
    .topnav > div > a:visited {
        color: rgb(128, 132, 142);
        text-decoration: none !important;
    }
    .topnav > div > a:visited:hover {
        color: white;
    }
    nav {
        display: flex;
        flex-direction: row;
        height: 10rem;
        flex-grow: 1;
        background-color: rgb(43, 45, 49);
        justify-content: space-between;
        align-items: center;
        padding: 0 2rem;
        border-bottom: 1px solid #424549dd;
    }
</style>
