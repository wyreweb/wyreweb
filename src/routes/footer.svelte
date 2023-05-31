<script type="module">
    import Fa from 'svelte-fa/src/fa.svelte'
    import { faInstagram,faFacebook,faTwitter,faTiktok } from '@fortawesome/free-brands-svg-icons'
    export const Footer=()=>{}
    let year=new Date().getFullYear()
</script>
<main>
    <p>&copy; <span>{year}</span> Wyreweb OÜ</p>
    <a href="https://koda.ee">
    <img src="/ecci logo.png" alt="image001.png">
</a>

    <ul class="social-links">
    <li><a href="https://instagram.com/wyreweb"><Fa icon={faInstagram} size="1.5x" /></a></li>
    <li><a href="https://twitter.com/wyreweb"><Fa icon={faTwitter} size="1.5x"/></a></li>
    <li><a href="https://www.tiktok.com/@wyreweb"><Fa icon={faTiktok} size="1.5x"/></a></li>
    <li><a href="https://facebook.com/wyreweb.ou"><Fa icon={faFacebook} size="1.5x"/></a></li>
</ul>
</main>
<style>
    main{
        display: flex;
        justify-content: space-between;
        backdrop-filter: blur(30px);
        border-radius: 10px 10px 0 0;
        width: 100%;

    }
    .social-links{
        list-style: none;
        display: flex;
        gap: 1rem;
        padding-right: 2rem;
    }
    p{
        margin-left: 2rem;
    }
    a{
        color: white;
    }
    img{
        width: 85%;
        margin-right: -10rem;

    }
    @media (width<500px){
        main{
            display: block;
            text-align: center;
        }
        .social-links{
            margin-left: 20vw;
        }
        img{
            width: 60%;
        }
        p{
            margin-left: -5vw;
        }
    }
    @media (500px<width<999px){
    p{
        font-size: 1rem;
        padding-right: 2rem;
    }
}
</style>