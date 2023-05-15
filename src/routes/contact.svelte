<script>
    import Fa from 'svelte-fa'
    import {faEnvelope} from '@fortawesome/free-solid-svg-icons'
    import {faWhatsapp} from '@fortawesome/free-brands-svg-icons'
</script>
<main>
    <h3>Reach Out</h3>
    <div class="content">
        <p> If you have any questions about our services or would like to schedule a consultation, please don't hesitate to contact us.</p>
        <ul class="contact-info">
            <li><a href="mailto:connect@wyreweb.com"><Fa icon={faEnvelope}/> connect@wyreweb.com</a></li>
            <li><a href="https://wa.me/201128533544"><Fa icon={faWhatsapp}/> +201128533544</a></li>
        </ul>
    </div>
</main>
<style>
    .content{
        display: grid;
        grid-template-columns: repeat(2,1fr);
        grid-gap: 30%;
        margin-left: 3rem;
    }
    main{
        background-color: rgba(255,255,255,0.25);
        backdrop-filter: blur(30px);
        border-radius: 10px;
        padding: 1rem;
        margin: 2.5vw auto;
        width: 80vw;
    }
    p,li{
        font-size: 1.25rem;
    }
    ul{
        list-style: none;
    }
    a{
        color: #80dd96;
        text-decoration: none;
    }
    p{
        font-size: clamp(1rem, -1.5rem + 8vw, 1.25rem);
    }
    @media (width<500px){
        main{
            height: fit-content;
            transform: translateX(-3vw);
        }
        .content{
            display: block;
            margin: 0;
        }
        .contact-info{
            width: 100%;
            padding-left: 1rem;
        }
    }
    @media (500px<width<999px){
        .content{
            grid-gap: 0;
        }
    }
</style>