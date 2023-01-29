<script>
  import Report from "$lib/report.svelte";
  import Member from "$lib/member.svelte";
  import Home from "$lib/home.svelte";
  import Policy from "$lib/policy.svelte";
  import Vision from "$lib/vision.svelte";
  import { Turnstile } from 'svelte-turnstile';
</script>

<div class="hide">
<Turnstile siteKey="0x4AAAAAAABzM8RBMKZycgnJ" retry="auto" />
</div>
<div class="container">
  <Home />
  <div class="menu">
    <a href="#vision">วิสัยทัศน์พรรค</a>
    <a href="#policy">นโยบายพรรค</a>
    <a href="#report">แจ้งปัญหา</a>
    <a href="#member">สมาชิกพรรค</a>
</div>
  <Vision/>
  <Policy />
  <Report />
  <Member />
</div>

<a href="#home" class="top"
  ><svg
      fill="#fff"
      version="1.1"
      id="Layer_1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 0 330 330"
      xml:space="preserve"
  >
      <path
          id="XMLID_224_"
          d="M325.606,229.393l-150.004-150C172.79,76.58,168.974,75,164.996,75c-3.979,0-7.794,1.581-10.607,4.394
 l-149.996,150c-5.858,5.858-5.858,15.355,0,21.213c5.857,5.857,15.355,5.858,21.213,0l139.39-139.393l139.397,139.393
 C307.322,253.536,311.161,255,315,255c3.839,0,7.678-1.464,10.607-4.394C331.464,244.748,331.464,235.251,325.606,229.393z"
      />
  </svg>
</a>
<svg id="filters">
  <defs>
      <filter id="threshold">
          <feColorMatrix
              in="SourceGraphic"
              type="matrix"
              values="1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 255 -140"
          />
      </filter>
  </defs>
</svg>

<style>
  .hide {
    display: none;
  }
  .menu {
        margin-top: 7.5vh;
        margin-bottom: 10vh;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
    }

    .menu > a {
        text-align: center;
        width: 17vh;
        font-family: "Chonburi", cursive;
        margin: 0.75vh;
        text-decoration: none;
        display: inline-block;
        outline: 0;
        border: 0;
        cursor: pointer;
        border-radius: 8px;
        padding: 14px 24px 16px;
        font-size: 18px;
        font-weight: 700;
        line-height: 1;
        transition: transform 200ms, background 200ms;
        background: transparent;
        color: #fff;
        box-shadow: 0 0 0 3px #fff inset;
    }

    .menu > a:nth-child(3) {
        box-shadow: 0 0 0 3px #31344b inset;
        display: inline-block;
        outline: 0;
        border: 0;
        cursor: pointer;
        background: #31344b;
        color: #fff;
        border-radius: 8px;
        padding: 14px 24px 16px;
        font-size: 18px;
        font-weight: 700;
        line-height: 1;
        transition: transform 200ms, background 200ms;
    }

    .menu > a:hover {
        transform: translateY(-3px);
    }
  .top {
      --offset: 50px;
      text-decoration: none;
      white-space: nowrap;
      background-color: #31344b;
      padding: 1.5vh;
      width: 2.5vh;
      height: 2.5vh;
      border-radius: 50%;
      transition: transform 200ms, background 200ms;
      position: sticky;
      bottom: 20px;
      margin-left: 10px;
      place-self: end;
      margin-top: calc(100vh + var(--offset));
  }

  .top:hover {
      opacity: 0.7;
  }

  .top > svg {
      width: 2vh;
      height: 1.75vh;
  }
</style>
