<script>
import {onMount} from 'svelte'
import Icon from 'svelte-awesome'
import {code,shoppingBag,paintBrush,addressBookO,table} from 'svelte-awesome/icons'
    let show = false;

onMount(() => {
  show = true;
});
</script>
<main style="opacity: {show ? 1 : 0}; transition: opacity 500ms ease; transition-delay:0.5s">
    <h3>Services</h3>
    <ul class="cards-grid">
        <li><Icon data={code} label="Source Code" scale={3}/><h4>Website Development</h4> <p>Make a website that suits your needs, reflects your brand identity, and enhances your online presence.</p></li>
        <li><Icon data={shoppingBag} label="e-commerce" scale={3}/><h4>E-commerce Website Building</h4> <p>Cultivate your online business with an e-commerce business to make your products and service easily accessible to your target audience and customers. We can help you increase sales, build customer trust, and establish brand loyalty.</p></li>
        <li><Icon data={paintBrush} label="branding" scale={3}/><h4>Digital Marketing & Branding</h4> <p>Establish your online presence and increase your online reach through digital marketing and social media marketing strategies tailored specifically to your. We can help you create personalized digital marketing strategies including SEO and PPC services as well as social media marketing calendars.</p></li>
        <li><Icon data={addressBookO} label="web portfolio" scale={3}/><h4>Web Portfolio</h4> <p>Showcase your work with a web portfolio that displays your work. Whether you’re a traditional or digital artist, photographer, designer, or even dancer we can help you showcase your talent and attract new customers by displaying your expertise.</p></li>
        <li><Icon data={table} label="restaurant menu" scale={3}/><h4>Digitizing Menus</h4> <p>Digitize your restaurant menu to achieve better visual representation and easier access to your menu items and provide additional information. We can help you create digital menus that are cost effective and enhance your customer experience and are easily updated.</p></li>
    </ul>
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
    }
    .cards-grid{
        list-style: none;
        display: grid;
        grid-template-columns: repeat(3,1fr);
        gap: 1rem;
        text-align: center;
    }
    li{
        font-size: 1.25rem;
    }
    @media (width<500px){
        main{
            height: fit-content;
        }
        .cards-grid{
            display: block;
        }
        li{
            margin-top: 3rem;
            width: 90%;
        }
    }
    @media (250px<width<1000px){
        p{
            font-size: 1rem;
        }
    }
    @media(500px<width<1000px){
        .cards-grid{
        grid-template-columns: repeat(2,1fr);
    }
    }
</style>