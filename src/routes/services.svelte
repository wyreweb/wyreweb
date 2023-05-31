<script>
     import {onMount} from 'svelte'
    let show = false;

onMount(() => {
  show = true;
});
</script>
<main style="opacity: {show ? 1 : 0}; transition: opacity 500ms ease; transition-delay:0.5s">
    <h3>Services</h3>
    <ul class="cards-grid">
        <li>Website Development</li>
        <li>E-commerce Website Building</li>
        <li>Digital Marketing & Branding</li>
        <li>Digitizing Menus</li>
    </ul>
</main>
<style>
    main{
        background-color: rgba(255,255,255,0.25);
        backdrop-filter: blur(30px);
        border-radius: 10px;
        padding: 1rem;
        margin: 2.5vw auto;
        width: 80vw;
    }
    li{
        font-size: 1.25rem;
    }
    @media (width<500px){
        main{
            height: fit-content;
        }
    }
</style>