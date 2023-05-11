<script type="module">
    import Fa from 'svelte-fa/src/fa.svelte'
    import { faInstagram,faFacebook,faTwitter,faTiktok } from '@fortawesome/free-brands-svg-icons'
    export const Footer=()=>{}
    let year=new Date().getFullYear()
</script>
<main>
    <p>&copy; <span>{year}</span> Wyreweb OÜ</p>

    <ul class="social-links">
    <li><a href="https://instagram.com/wyreweb"><Fa icon={faInstagram} size="1.5x" /></a></li>
    <li><a href="https://twitter.com/wyreweb"><Fa icon={faTwitter} size="1.5x"/></a></li>
    <li><a href="https://www.tiktok.com/@wyreweb"><Fa icon={faTiktok} size="1.5x"/></a></li>
    <li><a href="https://facebook.com/wyreweb.ou"><Fa icon={faFacebook} size="1.5x"/></a></li>
</ul>
</main>
<style>
    main{
        position: absolute;
        bottom: 0;
        display: flex;
        justify-content: space-between;
        width: 96vw;
    }
    .social-links{
        list-style: none;
        display: flex;
        gap: 1rem;
    }
    a{
        color: white;
    }
</style>