<script>
    import ozadjepage from "../assets/SPLETNA_GRAFIKA_OZADJE_brezgrafike.png";
    import spotify from "../assets/Spotify.png";
    import apple from "../assets/Apple Music.png";
    import tiktok from "../assets/TikTok.png";
    import youtube from "../assets/Youtube.png";
</script>

<div>
    <div class="space" style="background-image: url('{ozadjepage}');">
        <div>
            <p class="text">AVALIABLE ON ALL PLATFORMS</p>
            <div class="linki">
                <img class="slikalink" src={spotify} alt="bb" />
                <img class="slikalink" src={apple} alt="bb" />
                <img class="slikalink" src={tiktok} alt="bb" />
                <img class="slikalink" src={youtube} alt="bb" />
            </div>
        </div>
    </div>
</div>

<style>
    .linki{
        display: flex;
        
        justify-content: center;
    }
    .space {
        
        display: flex;
        justify-content: center;
        align-items: center;
        height: 531px;
    }
    .text {
        position: relative;
        align-items: center;
        justify-content: center;
        font-family: 'Mersad', sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 25px;
        line-height: 29px;
        /* identical to box height */

        text-align: center;
        letter-spacing: 0.2em;

        color: #f8c418;
    }
    @media only screen and (max-width: 600px) {
        .text {
        position: relative;
        align-items: center;
        justify-content: center;
        font-family: 'Mersad', sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 18px;
        line-height: 29px;
        /* identical to box height */

        text-align: center;
        letter-spacing: 0.2em;

        color: #f8c418;
    }
    .space {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 210px;
    }
    }
</style>
