<script>
    import levitrak from "../assets/levateste.png";
    import desnitrak from "../assets/DESNATEST.png";
    import Film1 from "../assets/Slika1.png";
    import Film2 from "../assets/Slika2.png";
    import Film3 from "../assets/Slika3.png";
    import Film4 from "../assets/Slika4.png";
    import Film5 from "../assets/Slika5.png";
    import Film6 from "../assets/Slika6.png";
    import Film1mobi from "../assets/Slika1mobi.png";
    import Film2mobi from "../assets/Slika2mobi.png";
    import Film3mobi from "../assets/Slika3mobi.png";
    import Film4mobi from "../assets/Slika4mobi.png";
    import Film5mobi from "../assets/Slika5mobi.png";
    import Film6mobi from "../assets/Slika6mobi.png";
</script>

<div class="outline">
    <div class="space" style="background-image: url('{levitrak}');">
        <div class="plac" />
    </div>
    <div class="box">
        <div class="container">
            <img class="slikafilm" src={Film1} alt="bb" />
            <img class="slikafilm" src={Film2} alt="bb" />
            <img class="slikafilm" src={Film3} alt="bb" />
            <img class="slikafilm" src={Film4} alt="bb" />
            <img class="slikafilm" src={Film5} alt="bb" />
            <img class="slikafilm" src={Film6} alt="bb" />

            <img class="slikafilmobi" src={Film1mobi} alt="bb" />
            <img class="slikafilmobi" src={Film2mobi} alt="bb" />
            <img class="slikafilmobi" src={Film3mobi} alt="bb" />
            <img class="slikafilmobi" src={Film4mobi} alt="bb" />
            <img class="slikafilmobi" src={Film5mobi} alt="bb" />
            <img class="slikafilmobi" src={Film6mobi} alt="bb" />
        </div>
    </div>
    <div class="space" style="background-image: url('{desnitrak}');" />
</div>

<style>
    .slikafilmobi {
        display: none;
        max-width: 100%;
    }
    .slikafilm {
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
