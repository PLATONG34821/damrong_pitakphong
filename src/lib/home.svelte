<div class="home" id="home">
    <div class="logo">
        <svg
            viewBox="0 0 450 285"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
        >
            <path
                d="M90.5 75.6507C90.5 73.7254 91.6054 71.9712 93.3422 71.1403L238.505 1.6938C240.057 0.950988 241.883 1.05902 243.337 1.97977L422.675 115.528C424.122 116.444 425 118.039 425 119.752V154.537C425 157.804 421.918 160.193 418.755 159.379L165.761 94.31C164.934 94.0973 164.066 94.0999 163.241 94.3177L96.775 111.845C93.6039 112.681 90.5 110.29 90.5 107.011V75.6507Z"
                fill="#313653"
            />
            <path
                d="M0.5 160.916C0.5 158.642 2.03502 156.654 4.2355 156.079L163.686 114.399C164.546 114.174 165.451 114.182 166.307 114.424L388.357 177.028C390.512 177.635 392 179.601 392 181.84V201.974C392 204.952 389.413 207.27 386.453 206.944L165.785 182.642C165.265 182.584 164.739 182.609 164.226 182.715L6.51204 215.312C3.40928 215.954 0.5 213.584 0.5 210.416V160.916Z"
                fill="#3E495B"
            />
            <path
                d="M86.5 239.565C86.5 236.979 88.4713 234.82 91.0462 234.586L277.925 217.552C278.307 217.518 278.692 217.527 279.072 217.58L445.693 240.897C448.163 241.243 450 243.355 450 245.849V279.43C450 282.219 447.719 284.468 444.931 284.43L269.5 282H91.5C88.7386 282 86.5 279.761 86.5 277V239.565Z"
                fill="#121D2F"
            />
        </svg>
    </div>
    <div class="title">
        <span>PITAKPHONG<br />CHIANGMAN</span>
    </div>
    <div class="sub-title">
        <span>ทุกข์ภัยใช่</span>
        <span>ไร้ทางแก้</span>
        <span>พิทักษ์พงษ์นี้แน่</span>
        <span>ไม่แม้แพ้ยอมใคร</span>
    </div>
</div>

<style>
    .logo {
        margin-top: 7.5vh;
        margin-bottom: 5vh;
    }

    .home { 
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        animation: forwards cubic-bezier(0, 0.77, 1, 0.4);
    }

    .title {
        display: flex;
        flex-direction: column;
        align-items: center;
        font-family: "Yeseva One", cursive;
        font-size: 12.5vmin;
        color: white;
    }

    .title > span {
        text-align: center;
    }

    .sub-title {
        color: #31344b;
        font-family: "Chonburi", cursive;
        font-size: 3vmin;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }

    .sub-title > span {
        margin-right: 1vh;
    }

    .home > .logo > svg {
        width: 50vmin;
    }

    * {
        filter: blur(3px);
    }

    *:nth-child(1) {
        animation: fade-in 0.8s 0.5s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    *:nth-child(2) {
        animation: fade-in 0.8s 0.9s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    *:nth-child(3) {
        animation: fade-in 0.8s 1.2s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    *:nth-child(4) {
        animation: fade-in 0.8s 1.5s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    @keyframes fade-in {
        100% {
            opacity: 1;
            filter: blur(0);
        }
    }
</style>
