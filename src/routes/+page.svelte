<script>
    import Footer from "./footer.svelte";
    import Fa from 'svelte-fa/src/fa.svelte'
    import {faArrowCircleLeft,faArrowCircleRight} from '@fortawesome/free-solid-svg-icons'
  import About from "./about.svelte";
  import Services from "./services.svelte";
  import Contact from "./contact.svelte";
//   import {panGesture} from 'svelte-gestures'
  let distance=0
  const goRight=()=>{
    distance -= 100;
    let leftBTN = document.querySelector('.left');
    let rightBTN=document.querySelector('.right')
    let cards = document.querySelector('.cards');
    cards.style.transform = `translateX(${distance}vw)`;
    if (distance === 0) {
      leftBTN.style.display = "none";
    }
    if (distance === -200) {
      rightBTN.style.display = "none";
    } else {
        rightBTN.style.display="block"
    }
    leftBTN.style.display = "block";
  }
  const goLeft=()=>{
    distance += 100;
    let leftBTN = document.querySelector('.left');
    let rightBTN=document.querySelector('.right')
    let cards = document.querySelector('.cards');
    cards.style.transform = `translateX(${distance}vw)`;
    if (distance === 0) {
      leftBTN.style.display = "none";
    }
    if (distance === -200) {
      rightBTN.style.display = "none";
    } else {
        rightBTN.style.display="block"
    }
  }
  const handlePanMove=(event)=>{
    const deltaX = event.detail.delta.x;
    const deltaY = event.detail.delta.y;
    distance += deltaX;
    distance = Math.max(Math.min(positionX, 100), -100);
  }
</script>
<main>
    <div class="navbar">
    <div class="identity">
    <img src="/logo.svg" alt="Wyreweb logo">
    <h1>Wyreweb</h1>
</div>
        <button class="blog">Check out the blog</button>
</div>
<div class="cards">
    <About/>
    <Services/>
    <Contact/>
</div>
<div class="buttons">
    <button class="left"on:click={goLeft}><Fa icon={faArrowCircleLeft} size="5x"/></button>
    <button class="right" on:click={goRight}><Fa icon={faArrowCircleRight} size="5x"/></button>

</div>
    <Footer/>
</main>
<style>
    @font-face {
    font-family: 'digitalt';
    font-style: normal;
    src: url('https://fonts.cdnfonts.com/css/digitalt'); /* IE9 Compat Modes */
    src: local(''), url('/digitalt-font/Digitalt-nGZM.otf') format('embedded-opentype'),
        /* Modern Browsers */ url('/digitalt-font/Digitalt-04no.ttf') format('truetype')
    }
    *{
        overflow-x: hidden;
    }
    .navbar{
        color: white;
        display: flex;
        gap: 1rem;
        justify-content: space-between;
    }
    img{
        width: clamp(6rem, -1.5rem + 8vw, 15rem);
    }
    .identity{
        display: flex;
        gap: 1rem;
    }
    h1{
        font-family: 'digitalt';
        font-size: clamp(3rem, -1.5rem + 8vw, 2.5rem);
    }
    button{
        background: transparent;
        border: none;
        color: #937fdb;
        position: fixed;
        top: 20vw;
        z-index: 10;
    }
    .left{
        left: 1rem;
        display: none;
    }
    .right{
        left: 94vw;
    }
    .cards{
        display: flex;
        justify-content: space-between;
        gap: 1rem;
        width: 300vw;
        transition: all 0.3s;
    }
    .blog{
        color: white;
        background: transparent;
        top: 2rem;
        right: 1rem;
        border-radius: 10px;
        border: solid white 1px;
        font-size: 1.25rem;
        padding: 0.5rem;
        cursor: pointer;
    }
    .blog::after{
        content: 'soon';
        color: red;
        position: absolute;
        top: -55%;
        right: -5%;
    }
    @media (width<500px){
        .buttons{
            display: none;
        }
        .navbar{
            flex-wrap: wrap;
        }
        .blog{
            font-size: 1rem;
            top: 7.5rem;
        }
        .cards{
            margin: 15vw auto;
        }
    }
</style>