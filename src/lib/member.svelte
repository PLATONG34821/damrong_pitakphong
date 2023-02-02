<script>
    let Pitakphong = "logo-pitakphong.png";
    let Damrong = "logo-damrong.png";
</script>

<section id="member">
    <a href="#member">
        <h2>สมาชิกพรรค</h2>
    </a>
    <div class="member-list">
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/FHUN.jpg" alt="FHUN" />
            </div>
            <div class="member-name">
                <h2>FHUN</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/BEAUTY.jpeg" alt="BEAUTY" />
            </div>
            <div class="member-name">
                <h2>BEAUTY</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/BELL.jpeg" alt="BELL" />
            </div>
            <div class="member-name">
                <h2>MILD</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/FERN.jpeg" alt="FERN" />
            </div>
            <div class="member-name">
                <h2>FERN</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/FOLKSONG.jpeg" alt="FOLKSONG" />
            </div>
            <div class="member-name">
                <h2>FOLKSONG</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/FOURMOST.jpeg" alt="FOURMOST" />
            </div>
            <div class="member-name">
                <h2>FOURMOST</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/IK.jpeg" alt="IK" />
            </div>
            <div class="member-name">
                <h2>IK</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/JUNE.jpeg" alt="JUNE" />
            </div>
            <div class="member-name">
                <h2>JUNE</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/MILD.jpeg" alt="MILD" />
            </div>
            <div class="member-name">
                <h2>BELL</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/NAM.jpeg" alt="NAM" />
            </div>
            <div class="member-name">
                <h2>NAM</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/NEXT.jpeg" alt="NEXT" />
            </div>
            <div class="member-name">
                <h2>NEXT</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/OHM.jpeg" alt="OHM" />
            </div>
            <div class="member-name">
                <h2>OHM</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/STAMP.jpeg" alt="STAMP" />
            </div>
            <div class="member-name">
                <h2>STAMP</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/SUGUT.jpeg" alt="SUGUT" />
            </div>
            <div class="member-name">
                <h2>SUGUT</h2>
            </div>
        </div>
        <div class="member-box">
            <div class="member-img">
                <img src="member-img/TOPTAP.jpg" alt="TOPTAP" />
            </div>
            <div class="member-name">
                <h2>TOPTAP</h2>
            </div>
        </div>
    </div>
</section>

<style>
    #member > a {
        cursor: alias;
        text-decoration: none;
        transition: all 200ms;
    }
    #member > a:active {
        transform: translateY(-5px);
        opacity: 0.8;
    }
    #member {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: "Chonburi", cursive;
    }
    #member > a > h2 {
        margin: 5vh;
        color: #31344b;
        font-size: 10vmin;
    }
    .member-list {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
    }
    .member-box {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-width: 12.5vmax;
        max-width: 12.5vmax;
        min-height: 12.5vmax;
        max-height: 12.5vmax;
        margin: 10px;
        margin-inline: 25px;
        padding: 10px;
        background-color: hsla(233, 21%, 24%, 0.2);
        max-width: fit-content;
        border-radius: 2.5vh;
        overflow: hidden;
    }

    .member-img > img {
        border-radius: 50%;
        width: 10vmax;
        height: 10vmax;
        object-fit: cover;
        object-position: center;
    }

    .member-name {
        color: rgb(255, 255, 255);
        text-align: center;
    }

    .member-name > h2 {
        margin: 0;
        font-size: 2vh;
    }
</style>
