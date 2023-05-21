<script>
    import bimagna from "../assets/MAGNAWEBTEST.png";
    //import parnerji from "../assets/sponsorji1 1.png";
    import parnerjiw from "../assets/sponsorji1white.png";
</script>

<div>
    <div class="space">
        <div>
            <img class="bigmagna" src={bimagna} alt="bb" />
        </div>
    </div>
    <div class="sponzorji">
        <p class="collab">In collaboration with:</p>
    </div>
    <div class="parnerji">
        <img class="slikasponzor" src={parnerjiw} alt="bb" />
    </div>
</div>

<style>
    .bigmagna {
        width: 372px;
    }
    .slikasponzor {
        width: 1144px;
    }
    .parnerji {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #101010;
        height: 260px;
    }
    .collab {
        font-family: "Mersad", sans-serif;
        font-style: normal;
        font-weight: 800;
        font-size: 15px;
        line-height: 17px;
        text-align: center;
        letter-spacing: 0.125em;
        text-transform: uppercase;

        color: #f8c418;
        font-display: swap;
    }
    .sponzorji {
        display: flex;
        background-color: #101010;
        justify-content: center;
        align-items: center;
    }
    .space {
        display: flex;
        background-color: #101010;
        justify-content: center;
        align-items: center;
    }
    @media only screen and (max-width: 600px) {
        .parnerji {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #101010;
        height: 129px;

    }
        .bigmagna {
            width: 220px;
        }
        .slikasponzor {
            width: 369px;
        }
    }
</style>
