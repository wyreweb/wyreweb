<script>
    import {onMount} from 'svelte'
    let show = false;

onMount(() => {
  show = true;
});
</script>
<main style="opacity: {show ? 1 : 0}; transition: opacity 500ms ease;">
    <h2>Welcome to Wyreweb!</h2>
    <p>We offer web and IT services to help businesses of all sizes succeed online.</p>
  
    <p>Our team of experts has a wealth of experience in web development, digital marketing, and IT services such as network infrastructure, security, and cloud computing. We are committed to delivering high-quality solutions that are tailored to our clients' specific needs and building long-lasting relationships with them.</p>
        
    <p>Contact us today to find out how we can help you achieve your business goals.</p>
  </main>
<style>
    main{
        background-color: rgba(255,255,255,0.25);
        backdrop-filter: blur(30px);
        border-radius: 10px;
        padding: 1rem;
        margin: 2.5vw auto;
        width: 80vw;
        opacity: 0;
    }
    p{
        font-size: clamp(0.9rem, -1.5rem + 8vw, 1.25rem);
    }
</style>