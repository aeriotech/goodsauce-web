<script>
    import levitrak from "../assets/levateste.png";
    import desnitrak from "../assets/DESNATEST.png";
    import Film1 from "../assets/newpic/NORMALsLIKA_1-min.png";
    import Film2 from "../assets/Slika2-min.png";
    import Film3 from "../assets/Slika3-min.png";
    import Film4 from "../assets/Slika4-min.png";
    import Film5 from "../assets/Slika5-min.png";
    import Film6 from "../assets/Slika6-min.png";
    import Film1mobi from "../assets/newpic/NORMALsLIKA_1-min.webp";
    import Film2mobi from "../assets/newpic/Slika2-2.webp";
    import Film3mobi from "../assets/newpic/Slika3-2.webp";
    import Film4mobi from "../assets/newpic/Slika4-1.webp";
    import Film5mobi from "../assets/newpic/Slika5-1.webp";
    import Film6mobi from "../assets/newpic/Slika6-1.webp";

    import LIK from "../assets/Y2Mate.is - EZRA - Lik! (Official Video)-30UzCpFOdco-720p-1656378123642.mp4";
    import TREJLR from "../assets/Y2Mate.is - EZRA - GOOD SAUCE (OFFICIAL TRAILER)-r5InmsO96TY-1080p-1655860415849.mp4";
    import TORERO from "../assets/newpic/1_GS_TORERO_FINAL.mp4"
    
    
    
    import VideoPlayer from "./video/videowraper.svelte";
</script>

<div class="outline">
    <div class="space" style="background-image: url('{levitrak}');">
        <div class="plac" />
    </div>
    <div class="box">
        <div class="container">
            <div class="slikepc">
                <VideoPlayer slika={Film1} video={TORERO} />
                
            </div>
            <img class="slikafilm" src={Film2} alt="bb" />
            <img class="slikafilm" src={Film3} alt="bb" />
            <img class="slikafilm" src={Film4} alt="bb" />
            <img class="slikafilm" src={Film5} alt="bb" loading="lazy" />
            <img class="slikafilm" src={Film6} alt="bb" loading="lazy" />

            <div class="slikemobi">
                <VideoPlayer slika={Film1mobi} video={TORERO} />
                
            </div>
            
            <img class="slikafilmobi" src={Film2mobi} alt="bb" />
            <img class="slikafilmobi" src={Film3mobi} alt="bb" />
            <img class="slikafilmobi" src={Film4mobi} alt="bb" />
            <img class="slikafilmobi" src={Film5mobi} alt="bb" loading="lazy" />
            <img class="slikafilmobi" src={Film6mobi} alt="bb" loading="lazy" />
        </div>
    </div>
    <div class="space" style="background-image: url('{desnitrak}');" />
</div>

<style>
    .slikemobi {
        display: none;
    }
    .slikafilmobi {
        display: none;
        max-width: 100%;
    }
    .plac {
        width: 20px;
    }
    .space {
        width: 38px;
    }
    .outline {
        display: flex;
        justify-content: center;
        align-items: stretch;
        background-size: cover;
    }
    .container {
        display: flex;
        flex-direction: column;

        justify-content: center;
        background-size: cover;
        overflow: hidden;
    }
    .box {
        flex-grow: 1;
    }

    .slikafilm {
        width: 100%;
        opacity: 1;
        transition: opacity 0.3s ease;
    }
    @media (max-width: 768px) {
        .space {
            display: none;
        }
        .slikepc{
            display: none;
        }
        .slikemobi{
            display: block;
        }
        .slikafilmobi {
            max-width: 100%;
            display: block;
        }
        .slikafilm {
            display: none;
            max-width: 100%;
        }
    }
</style>
