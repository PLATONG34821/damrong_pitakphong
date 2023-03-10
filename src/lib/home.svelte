<div class="home" id="home">
    <div class="logo">
        <img src="logo-council.png" height="575" alt="LOGO">
    </div>
    <div class="title">
        <span>STUDENT COUNCIL</span>
    </div>
    <div class="sub-title">
        <span>ลูกดำรง</span>
        <span>รักศักด์ศรี</span>
        <span>กริยาวาจาดี</span>
        <span>มีน้ำใจ</span>
        <span>ไหว้งดงาม</span>
    </div>
</div>

<style>
    .logo {
        margin-top: 7.5vh;
        margin-bottom: 5vh;
    }

    .logo > img {
        height: 25vmax;
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
        color: #d9d477;
        font-family: "Chonburi", cursive;
        font-size: 3vmin;
        display: flex;
        flex-direction: row;
        justify-content: center;
    }

    .sub-title > span {
        margin-right: 1vh;
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

    *:nth-child(5) {
        animation: fade-in 0.8s 1.5s forwards cubic-bezier(0.11, 0, 0.5, 0);
    }

    @keyframes fade-in {
        100% {
            opacity: 1;
            filter: blur(0);
        }
    }
</style>
