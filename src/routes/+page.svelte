<script>
    import Footer from "./footer.svelte";
  import About from "./about.svelte";
  import Services from "./services.svelte";
  import Contact from "./contact.svelte";
</script>
<main>
    <div class="navbar">
    <div class="identity">
    <img src="/logo.svg" alt="Wyreweb logo">
    <h1>Wyreweb</h1>
</div>
<a href="https://wyreweb.com/blog"><button class="blog">Check out the blog</button></a>
    </div>
<div class="cards">
    <About/>
    <Services/>
    <Contact/>
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
        z-index: 10;
    }
    .cards{
        position: relative;
        gap: 1rem;
        transition: all 0.3s;
    }
    .blog{
        color: white;
        background: transparent;
        border-radius: 10px;
        border: solid white 1px;
        font-size: 1.25rem;
        padding: 0.5rem;
        cursor: pointer;
        height: 3rem;
        margin-right: 1rem;
        margin-top: 2rem;
        position: relative;
    }
    @media (width<500px){
        .navbar{
            display: block;
        }
        .blog{
            font-size: 1rem;
            margin-left:30vw;
        }
        .cards{
            margin: 15vw auto;
        }
    }
</style>