<script>
    import {onMount} from 'svelte'
    let show = false;

onMount(() => {
  show = true;
});
</script>
<main style="opacity: {show ? 1 : 0}; transition: opacity 500ms ease;">
    <h2>Welcome to Wyreweb!</h2>
    <p>
        At Wyreweb, you're not just a client, you're also a collaborative member in our web development team. We believe in the client's vision and do our best to make that vision an applicable reality. We work closely with our clients to best understand their vision and work tirelessly to make perfectly unique solutions that suit each client's requirements with no issues or delays. No matter the size of your business or your goals, we can help you.
    </p>
    <p>
        We aim at Wyreweb to not only create sleek websites, but also make them fast, functional, and easy to maintain.
    </p>
  </main>
<style>
    main{
        background-color: rgba(255,255,255,0.25);
        backdrop-filter: blur(30px);
        -webkit-backdrop-filter: blur(30px);
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