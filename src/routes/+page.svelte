<script>
  import Report from "$lib/report.svelte";
  import Member from "$lib/member.svelte";
  import Home from "$lib/home.svelte";
  import Policy from "$lib/policy.svelte";
  import Vision from "$lib/vision.svelte";
  import { Turnstile } from "svelte-turnstile";
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
  <Vision />
  <Policy />
  <Report />
  <Member />
</div>

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
    transform: translateY(-5px);
  }
</style>
