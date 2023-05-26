<script>
    //import ozadjepage from "../assets/SPLETNA_GRAFIKA_OZADJE_brezgrafike.png";
    import ozadjepagecomp from "../assets/SPLETNA_GRAFIKA_OZADJE_brezgrafike - Copy-min.webp";
    import spotify from "../assets/Spotify.png";
    import apple from "../assets/Apple Music.png";
    import tiktok from "../assets/TikTok.png";
    import youtube from "../assets/Youtube.png";
    import deezer from "../assets/newpic/DEEZER.png";
    import tidle from "../assets/newpic/TIDLE.png";
</script>

<div>
    <div class="space" style="background-image: url('{ozadjepagecomp}');">
        <div class="kontejnr">
            <p class="text">AVALIABLE ON ALL PLATFORMS</p>
            <div class="linki">
                <a
                    href="https://open.spotify.com/track/4Nym0pHaQ8RM28lA9Q1suJ?si=9fc1397c507f4aba"
                    ><img class="slikalink" src={spotify} alt="bb" /></a
                >
                <a
                    href="https://music.apple.com/si/album/torero/1688238226?i=1688238239"
                    ><img class="slikalink" src={apple} alt="bb" /></a
                >
                <a
                    href="https://www.tiktok.com/music/Torero-7236270306096252930?is_from_webapp=1&sender_device=pc"
                    ><img class="slikalink" src={tiktok} alt="bb" /></a
                >

                <img class="slikalink" src={youtube} alt="bb" />

                <a href="https://deezer.page.link/KBTXJiR49CZ4SGi96"
                    ><img class="slikalink" src={deezer} alt="bb" /></a
                >

                <a href=""
                    ><img class="slikalink" src={tidle} alt="bb" /></a
                >
            </div>
        </div>
    </div>
</div>

<style>
    .slikalink {
        margin: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .linki {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .space {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 303px;
    }
    .text {
        display: flex;
        position: relative;
        align-items: center;
        justify-content: center;
        font-family: "Mersad", sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 25px;
        line-height: 29px;
        /* identical to box height */

        text-align: center;
        letter-spacing: 0.2em;

        color: #f8c418;
        font-display: swap;
    }
    @media only screen and (max-width: 600px) {
        .slikalink {
            margin: 5px;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .text {
            position: relative;
            align-items: center;
            justify-content: center;
            font-family: "Mersad", sans-serif;
            font-style: normal;
            font-weight: 600;
            font-size: 18px;
            line-height: 29px;
            /* identical to box height */

            text-align: center;
            letter-spacing: 0.2em;

            color: #f8c418;
            font-display: swap;
        }
        .space {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 210px;
        }
    }
</style>
