<script>
    import bimagna from "../assets/MAGNAWEBTEST.png";
</script>

<div>
    <div class="space">
        <div>
            <img class="bigmagna" src={bimagna} alt="bb" />
        </div>
    </div>
    <div class="sponzorji">
        <p class="collab"> In collaboration with:</p>
    </div>
</div>

<style>
    .collab {
        font-family: "Mersad";
        font-style: normal;
        font-weight: 800;
        font-size: 15px; 
        line-height: 17px;
        text-align: center;
        letter-spacing: 0.125em;
        text-transform: uppercase;

        color: #f8c418;
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
        .bigmagna {
            width: 372px;
        }
    }
</style>
