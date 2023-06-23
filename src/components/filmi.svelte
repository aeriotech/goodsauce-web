<script>
    import levitrak from "../assets/levateste.png";
    import desnitrak from "../assets/DESNATEST.png";
    import Film1 from "../assets/newpic/NORMALsLIKA_1-min.png";
    import Film2 from "../assets/newpic/3-min.png";
    import Film3 from "../assets/newpic/2-min.png";
    import Film4 from "../assets/newpic/4-min.png";
    import Film5 from "../assets/newpic/5-min.png";
    import Film6 from "../assets/Slika6-min.png";
    import Film1mobi from "../assets/newpic/NORMALsLIKA_1-min.webp";
    import Film2mobi from "../assets/newpic/3-min.webp";
    import Film3mobi from "../assets/newpic/2-min.webp";
    import Film4mobi from "../assets/newpic/4-min.webp";
    import Film5mobi from "../assets/newpic/5-min.webp";
    import Film6mobi from "../assets/newpic/Slika6-1.webp";
    const TORERO = "https://cdn.magnadogsworldwide.com/thesauce/torero.mp4";
    const SUNLIGHT = "https://cdn.magnadogsworldwide.com/thesauce/sunlight.mp4";
    const LMK =
        "https://cdn.magnadogsworldwide.com/thesauce/2_GS_LMK_FINAL.mp4";
    const BYEBYE =
        "https://cdn.magnadogsworldwide.com/thesauce/4_GS_BYEBYE_FINAL.mp4";
    const SOARIN = "https://cdn.magnadogsworldwide.com/thesauce/5_SOARIN.mp4";

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
            <div class="slikepc">
                <VideoPlayer slika={Film2} video={LMK} />
            </div>
            <div class="slikepc">
                <VideoPlayer slika={Film3} video={SUNLIGHT} />
            </div>
            <div class="slikepc">
                <VideoPlayer slika={Film4} video={BYEBYE} />
            </div>
            <div class="slikepc">
                <VideoPlayer slika={Film5} video={SOARIN} />
            </div>

            <img class="slikafilm" src={Film6} alt="bb" loading="lazy" />

            <div class="slikemobi">
                <VideoPlayer slika={Film1mobi} video={TORERO} />
            </div>
            <div class="slikemobi">
                <VideoPlayer slika={Film2mobi} video={LMK} />
            </div>

            <div class="slikemobi">
                <VideoPlayer slika={Film3mobi} video={SUNLIGHT} />
            </div>

            <div class="slikemobi">
                <VideoPlayer slika={Film4mobi} video={BYEBYE} />
            </div>

            <div class="slikemobi">
                <VideoPlayer slika={Film5mobi} video={SOARIN} />
            </div>

            <img class="slikafilmobi" src={Film6mobi} alt="bb" loading="lazy" />
        </div>
    </div>

    <div class="space" style="background-image: url('{desnitrak}');">
        <div class="plac" />
    </div>
</div>

<style>
    .pad {
        width: 38px;
    }

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

    .slikepc {
        width: 100%;
        margin-top: 10px;
        margin-bottom: 10px;
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
        .slikepc {
            display: none;
        }
        .slikemobi {
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
