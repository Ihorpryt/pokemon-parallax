<script>
    import img from '$lib/img/Charizard_SS.webp';
    import img1 from '$lib/img/clouds.png';
    import img2 from '$lib/img/mountain-valley.png';
    import img3 from '$lib/img/cut-bottom.svg';
</script>


<div class="everything">

    <div class="dummy"></div>

    <div class="content">
        <img src={img1} class="clouds" alt="">
        <img src={img2} class="mountains" alt="">
        <img src={img3} class="cut" alt="" >


        <div class="text">
            <img src={img} class="cherizard" alt="">
            <div class="title">
            <h4>what is</h4>
            <h1>Pokémon</h1>
            </div>
            <p>The Star Wars universe spans countless planets and epochs, teeming with diverse alien species and cultures. A constant struggle burns between the light side of the Force, wielded by the Jedi Knights, and the dark side, embodied by the Sith. Droids, smugglers, bounty hunters, and iconic heroes like Luke Skywalker and Leia Organa navigate constant struggle for balance in the Force.</p>
            <p>Heroes rise from humble beginnings, wielding lightsabers and piloting starships in epic battles for freedom against tyrannical empires. It's a universe rich in adventure, mythology, and timeless themes of good versus evil.</p>
        </div>

    </div>

    <div class="dummy"></div>
    <div class="dummy"></div>


</div>


<style>
    /* .everything {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
    } */

    .content {
        /* max-width: 700px;
        display: flex;
        flex-direction: column;
        align-items: center; */

        display: grid;
        grid-template-areas: "stack";
        justify-items: center;
    }

    .content > * {
        grid-area: stack;
        animation: parallax linear;
        animation-timeline: scroll();
    }
    .clouds {
        width: 100%;
        --parallax-speed: -0.1;
    }
    .mountains {
        width: 100%;
        height: 948px;
        --parallax-speed: -1;
    }
    .cut {
        width: 100%;
        height: 65px;
        align-self:self-end;
        margin-bottom: -30px;
        --parallax-speed: -1;
    }
    .text {
        max-width: 700px;
        --parallax-speed: -3.2;
        position: absolute;
        margin-top: 300px;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .cherizard {
        width: 228px;
        height: 211px;
        margin-bottom: 55px;
        margin-top: 50px;
    }

    h1 {
        text-align: center;
        font-size: 50px;
        line-height: 50px;
        font-style: italic;
        font-weight: 900;
        letter-spacing: 1.25px;
        text-transform: uppercase;
        margin: 0;
        font-family: Kufam;
    }
    h4 {
        text-align: center;
        margin: 0;
        font-style: italic;
        font-weight: 600;
        font-size: 15px;
        line-height: 20px;
        letter-spacing: 3px;
        text-transform: uppercase;
        font-family: Kufam;
    }

    .title {
        display: flex;
        gap: 10px;
        flex-direction: column;
        margin-bottom: 10px;
    }
    p {
        text-align: center;
        font-family: Inter;
        font-size: 18px;
        font-weight: 500;
        line-height: 26px;
        margin-top: 0;
        margin-bottom: 20px;
    }

    @keyframes parallax {
        to {
            transform: translateY(calc(var(--parallax-speed) * 200px));
        }
    }

    .dummy {
        height: 200px;
        margin-top: 50px;
    }

</style>