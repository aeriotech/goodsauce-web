<script>
    import slikaozadnje from "../assets/SPLETNA_GRAFIKA_OZADJE_siroko 1.png";
    import magnanapis from "../assets/MAGNA_LOGO_PROFFESIONAL.png";
    import linkig from "../assets/iglink.png";
</script>

<div class="outline">
    <div class="container">
        <div class="papak" style="background-image: url('{slikaozadnje}'); ">
            <div class="header">
                <img class="magna" src={magnanapis} alt="bb" />
                <div class="spacer" />
                <a href="https://www.instagram.com/magnadogsworldwide/"
                    ><img class="iglink" src={linkig} alt="tt" /></a
                >
            </div>

            <div class="title">
                <span class="napis">The Sauce</span>
                <div id="crta" />
                <span class="napis">The Movie</span>
            </div>
        </div>
    </div>
</div>

<style>
    .space {
        width: 38px;
    }

    .title {
        display: flex;
        justify-content: center;
        gap: 18px;
    }
    #crta {
        border-left: #f8c418 4px;
        border-left-style: solid;
        color: #f8c418;
        margin-bottom: 1px;
        margin-top: 43px;
    }
    .napis {
        margin-top: 50px;
        font-family: "Mersad";
        font-style: SemiBold;
        font-weight: 600;
        font-size: 35px;
        line-height: 40px;

        color: #f8c418;
    }
    .header {
        display: flex;
        align-items: start;
    }
    .iglink {
        margin-top: 5px;
        margin-right: 5px;
    }
    .spacer {
        flex-grow: 1;
    }
    .outline {
        display: flex;
        justify-content: center;
        align-items: stretch;
    }
    .papak {
        flex-grow: 1;
        background-position: center;

        align-items: stretch;
        height: 100vh;
        background-size: cover;
    }

    .magna {
        margin-top: 5px;
        margin-left: 5px;
        z-index: 1;
        transition: 1s;
    }

    .container {
        flex-grow: 1;
        height: 100vh;
        background: #000000;
    }
    @media only screen and (max-width: 600px) {
        .magna {
            width: 140px;
        }
        #crta {
            border-left: #f8c418 3px;
            border-left-style: solid;
            color: #f8c418;
            margin-bottom: 1px;
            margin-top: 43px;
        }
        .napis {
            margin-top: 50px;
            font-family: "Mersad";
            font-style: SemiBold;
            font-weight: 600;
            font-size: 25px;
            line-height: 40px;

            color: #f8c418;
        }
        .title {
            display: flex;
            justify-content: center;
            gap: 12px;
        }
    }
</style>
