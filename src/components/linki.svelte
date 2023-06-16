<script>
    
    import ozadjepagecomp from "../assets/SPLETNA_GRAFIKA_OZADJE_brezgrafike - Copy-min.webp";
    import spotify from "../assets/Spotify.png";
    import apple from "../assets/Apple Music.png";
    import tiktok from "../assets/TikTok.png";
    import youtube from "../assets/Youtube.png";
    import deezer from "../assets/newpic/DEEZER.png";
    
</script>

<div>
    <div class="space" style="background-image: url('{ozadjepagecomp}');">
        <div class="kontejnr">
            <p class="text">AVALIABLE ON ALL PLATFORMS</p>
            <div class="linki">
                <a
                    href="https://open.spotify.com/album/1Iu1NEi9uaNJUbh3oi8QmG?si=hlrL5YxYQ_CLjYIn3JctWw"
                    ><img class="slikalink" src={spotify} alt="bb" /></a
                >
                <a
                    href="https://music.apple.com/si/album/good-sauce-ep/1692316478"
                    ><img class="slikalink" src={apple} alt="bb" /></a
                >
                <a
                    href="https://www.tiktok.com/@magnadogsworldwide"
                    ><img class="slikalink" src={tiktok} alt="bb" /></a
                >

                <a href="https://www.youtube.com/@worldwidezra/videos"
                    ><img class="slikalink" src={youtube} alt="bb" /></a
                >

                <a href="https://deezer.page.link/8zYtgxwZx7TDrvKx9"
                    ><img class="slikalink" src={deezer} alt="bb" /></a
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
