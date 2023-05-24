<script>
    import levitrak from "../assets/levateste.png";
    import desnitrak from "../assets/DESNATEST.png";
    import Film1 from "../assets/Slika1-min.png";
    import Film2 from "../assets/Slika2-min.png";
    import Film3 from "../assets/Slika3-min.png";
    import Film4 from "../assets/Slika4-min.png";
    import Film5 from "../assets/Slika5-min.png";
    import Film6 from "../assets/Slika6-min.png";
    import Film1mobi from "../assets/Slika1mobi.webp";
    import Film2mobi from "../assets/Slika2mobi.webp";
    import Film3mobi from "../assets/Slika3mobi.webp";
    import Film4mobi from "../assets/Slika4mobi.webp";
    import Film5mobi from "../assets/Slika5mobi.webp";
    import Film6mobi from "../assets/Slika6mobi.webp";
    import LIK from "../assets/Y2Mate.is - EZRA - Lik! (Official Video)-30UzCpFOdco-720p-1656378123642.mp4";

    import { onMount } from "svelte";
    //let video;

    let photoVisible = true;
    let videoVisible = false;
    /*
    function handleClick() {
        
        video.play();
    }*/

    function handleClick() {
        photoVisible = !photoVisible;
        videoVisible = !videoVisible;
    }

    onMount(() => {
        const video = document.getElementById("video");

        video.addEventListener("click", function (event) {
            event.stopPropagation();
        });
    });
</script>

<div class="outline">
    <div class="space" style="background-image: url('{levitrak}');">
        <div class="plac" />
    </div>
    <div class="box">
        <div class="container">
            <div class="filmkontejnr">
                {#if photoVisible}
                    <!-- svelte-ignore a11y-click-events-have-key-events -->
                    <img
                        class="slikafilm"
                        src={Film1}
                        alt="bb"
                        loading="lazy"
                        on:click={handleClick}
                    />
                {/if}

                {#if videoVisible}
                    <video class="film" src={LIK} id="video" controls />
                {/if}
            </div>

            <img class="slikafilm" src={Film2} alt="bb" loading="lazy" />
            <img class="slikafilm" src={Film3} alt="bb" loading="lazy" />
            <img class="slikafilm" src={Film4} alt="bb" loading="lazy" />
            <img class="slikafilm" src={Film5} alt="bb" loading="lazy" />
            <img class="slikafilm" src={Film6} alt="bb" loading="lazy" />

            <div class="slikafilmobi">
                {#if photoVisible}
                    
                    <img
                        class="slikafilmobi"
                        src={Film1mobi}
                        alt="bb"
                        loading="lazy"
                        on:click={handleClick}
                    />
                {/if}

                {#if videoVisible}
                    <video class="slikafilmobi" src={LIK} id="video" controls />
                {/if}
            </div>

            <img class="slikafilmobi" src={Film2mobi} alt="bb" loading="lazy" />
            <img class="slikafilmobi" src={Film3mobi} alt="bb" loading="lazy" />
            <img class="slikafilmobi" src={Film4mobi} alt="bb" loading="lazy" />
            <img class="slikafilmobi" src={Film5mobi} alt="bb" loading="lazy" />
            <img class="slikafilmobi" src={Film6mobi} alt="bb" loading="lazy" />
        </div>
    </div>
    <div class="space" style="background-image: url('{desnitrak}');" />
</div>

<style>
    .film {
        margin: 20px;
        width: 100%;
        height: 800px;
    }
    .filmkontejnr{
        max-width: 100%;
        justify-content: center;
        align-items: center;
        display: flex;
    }
    .slikafilmobi {
        display: none;
        max-width: 100%;
    }
    .slikafilm {
        width: 100%;
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
    @media (max-width: 768px) {
        .space {
            display: none;
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
