<script>
    import { onMount } from "svelte";
    //let video;
    export let slika;
    export let video;

    let photoVisible = true;
    let videoVisible = false;
    /*
    function handleClick() {
        
        video.play();
    }*/

    // Check if the device is mobile
    function isMobileDevice() {
        return /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
            navigator.userAgent
        );
    }

    // Lazy load photo function
    function lazyLoadPhoto(img) {
        const observer = new IntersectionObserver((entries, observer) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    const src = img.getAttribute("data-src");

                    if (src) {
                        img.setAttribute("src", src);
                        img.removeAttribute("data-src");
                        observer.unobserve(img);
                    }
                }
            });
        });

        observer.observe(img);
    }

    let images = [];

    function handleClick() {
        photoVisible = !photoVisible;
        videoVisible = !videoVisible;

        if (videoVisible) {
            //const video = document.getElementById("video");
            //video.play();
        }
    }

    onMount(() => {
        const video = document.getElementById("video");

        /*video.addEventListener("click", function (event) {
            event.stopPropagation();
        });*/
    });
</script>

<div class="filmkontejnr">
    {#if photoVisible}
        <div class="photo-wrapper">
            <img class="slikafilm" src={slika} alt="bb" />
            <div class="overlay">
                <!--<p class="play">PLAY</p>-->
                <button class="play-button" on:click={handleClick}>
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="64"
                        height="64"
                        viewBox="0 0 64 64"
                    >
                        <path d="M22 14l28 18-28 18z" fill="#fff" />
                    </svg>
                </button>
                <button class="play-button-mobile" on:click={handleClick}>
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="64"
                        height="64"
                        viewBox="0 0 64 64"
                    >
                        <path d="M22 14l28 18-28 18z" fill="#292222" />
                    </svg>
                </button>
            </div>
        </div>
    {/if}

    {#if videoVisible}
        <div class="video-wrapper">
            <video class="film" src={video} id="video" controls autoplay />
            <button class="exit-button" on:click={handleClick}>
                <span class="exit-icon" />
            </button>
        </div>
    {/if}
</div>

<style>
    .play-button-mobile {
        display: none;
        justify-content: center;
        align-items: center;
        width: 80px;
        height: 80px;
        border: none;
        background: none;
        color: #292222;
        font-size: 32px;
        opacity: 0.5;
        cursor: pointer;
    }
    .play {
        display: none;
    }
    .overlay {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        opacity: 0;
        transition: opacity 0.3s ease;
        justify-content: center;
        align-items: center;
    }

    .play-button {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 80px;
        height: 80px;
        border: none;
        background: none;
        color: #fff;
        font-size: 32px;
        opacity: 1;
        cursor: pointer;

        transition: 300ms linear all;
    }
    .slikafilm {
        width: 100%;
        opacity: 1;
        transition: opacity 0.4s ease;
    }

    .slikafilm:hover {
        opacity: 0.7;
        transition: opacity 0.3s ease;
    }

    .photo-wrapper {
        position: relative;
        width: 100%;
        overflow: hidden;
        opacity: 1;
        transition: opacity 1s ease;
    }

    .photo-wrapper:hover .slikafilm {
        opacity: 0.7;
        transition: opacity 0.7s ease;
    }

    .photo-wrapper:hover .overlay {
        opacity: 1;
    }

    .filmkontejnr {
        width: 100%;

        justify-content: center;
        align-items: center;
        display: flex;
        
        overflow: hidden;
    }

    .film {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    .video-wrapper {
        position: relative;
        width: 100%;
    }

    .exit-icon {
        width: 16px;
        height: 16px;

        transform: rotate(45deg);
    }

    .exit-icon::before,
    .exit-icon::after {
        content: "";
        position: absolute;
        background-color: #fff;
    }

    .exit-icon::before {
        width: 2px;
        height: 20px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .exit-icon::after {
        width: 20px;
        height: 2px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    .exit-button {
        position: absolute;
        top: 20px;
        left: 20px;
        width: 40px;
        height: 40px;
        background-color: rgba(0, 0, 0, 0);
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        opacity: 0.4;
        transition: 300ms linear all;
    }
    .exit-button:hover {
        opacity: 1;
        background-color: black;
        transform: rotate(90deg);
        transition: 300ms linear all;
    }
    @media (max-width: 768px) {
        .play-button {
            display: none;
            justify-content: center;
            align-items: center;
            width: 80px;
            height: 80px;
            border: none;
            background: none;
            color: #fff;
            font-size: 32px;
            opacity: 1;
            cursor: pointer;

            transition: 300ms linear all;
        }
        .photo-wrapper .slikafilm {
            opacity: 1;
            max-width: 100%;
        }
        .film {
            width: 100%;
        }
        .video-wrapper {
            position: relative;
            width: 100%;
        }

        .photo-wrapper .overlay {
            opacity: 1;
        }
        .exit-button {
            position: absolute;
            top: 2px;
            left: 2px;
            width: 32px;
            height: 32px;
            background-color: rgba(0, 0, 0, 0);
            border: none;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0.4;
            transition: 300ms linear all;
        }
        .exit-icon {
            width: 12px;
            height: 12px;

            transform: rotate(45deg);
        }

        .exit-icon::before,
        .exit-icon::after {
            content: "";
            position: absolute;
            background-color: #fff;
        }

        .exit-icon::before {
            width: 1px;
            height: 12px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .exit-icon::after {
            width: 12px;
            height: 1px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        .overlay {
            display: flex;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            opacity: 1;
            justify-content: center;
            align-items: center;
        }
        .play-button-mobile {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 80px;
            height: 80px;
            border: none;
            background: none;
            color: #292222;
            font-size: 32px;
            opacity: 0.5;
            cursor: pointer;
        }
        .play {
            font-size: 4px;
            font-family: "Mersad", sans-serif;
            font-style: normal;
            font-weight: 800;
            color: #ffffff;
            position: absolute;
            display: flex;
            z-index: 1;
            justify-content: center;
            align-items: center;
        }
    }
</style>
