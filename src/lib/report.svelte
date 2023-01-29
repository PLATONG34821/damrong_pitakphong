<script>
    // @ts-nocheck

    import supabase from "$lib/db";
    import { onMount } from "svelte";
    import Marquee from "svelte-fast-marquee";

    /**
     * @type {any[] | null}
     */
    let issues = [];
    let issues_count = 0;
    let newRealname = "";
    let newIssue = "";
    let play = true;

    const addIssue = async (
        /** @type {string} */ issue,
        /** @type {any} */ realname
    ) => {
        if (issue != "") {
            if (realname == "") {
                let realname = "ไม่ต้องการระบุชื่อ";
                try {
                    const { data, error } = await supabase
                        .from("issue")
                        .insert([{ issue: issue, realname: realname }]);
                } catch (err) {
                    console.log(err);
                }
            } else {
                try {
                    const { data, error } = await supabase
                        .from("issue")
                        .insert([{ issue: issue, realname: realname }]);
                } catch (err) {
                    console.log(err);
                }
            }
            await getIssue();
        } else {
            alert("จำเป็นต้องกรอกปัญหา!");
        }
    };

    onMount(async () => {
        await getIssue();
    });

    const getIssue = async () => {
        try {
            let { data, error } = await supabase.from("issue").select("*");
            // @ts-ignore
            issues = data;
        } catch (err) {
            console.log(err);
        }
    };
</script>

<div class="issue" id="report">
    <a href="#report">
        <h2>แจ้งปัญหา</h2>
    </a>
    <div class="add-issue">
        <input
            placeholder="ชื่อ-นามสกุล (ไม่จำเป็น)"
            type="text"
            bind:value={newRealname}
        />
        <input placeholder="ปัญหาที่พบ" type="text" bind:value={newIssue} />
        <button on:click={() => addIssue(newIssue, newRealname)}
            >ส่งปัญหา</button
        >
    </div>
    <div class="show-issue" id="show-issue">
        <Marquee pauseOnClick={true} speed={200} {play}>
            {#each issues as issue}
                <div class="issue-box">
                    <h3>{issue.realname}</h3>
                    <p>{issue.issue}</p>
                </div>
            {:else}
                <p />
            {/each}
        </Marquee>
    </div>
</div>

<style>
    #report > a {
        text-decoration: none;
        transition: all 200ms;
    }
    #report > a:hover {
        cursor: alias;
        transform: translateY(-5px);
        opacity: 0.8;
    }
    .add-issue > input {
        width: 30vh;
        font-family: "Chonburi", cursive;
        margin: 0.75vh;
        text-decoration: none;
        display: inline-block;
        outline: 0;
        border: 0;
        border-radius: 8px;
        padding: 14px 24px 16px;
        font-size: 15px;
        font-weight: 700;
        line-height: 1;
        transition: transform 200ms, background 200ms;
        background: #fff;
        color: #31344b;
    }

    .add-issue > input::placeholder {
        color: #31344b;
    }

    .add-issue > button {
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
        transition: transform 200ms;
        background: transparent;
        color: #fff;
        box-shadow: 0 0 0 3px #fff inset;
    }

    .add-issue > button:hover {
        transform: translateY(-5px);
    }

    .issue > a > h2 {
        font-size: 10vmin;
        color: #31344b;
    }

    .show-issue {
        width: 100vw;
        display: flex;
        justify-content: right;
        flex-direction: row;
    }
    .issue {
        margin-bottom: 20vmin;
        color: #fff;
        font-family: "Chonburi", cursive;
        flex-direction: column;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: nowrap;
    }

    .add-issue {
        padding: 1.5vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-color: #31344b;
        width: fit-content;
        margin-bottom: 1.5vh;
        border-radius: 2.5vh;
    }

    .issue-box {
        padding: 1.5vh;
        justify-content: center;
        align-items: center;
        display: flex;
        flex-wrap: none;
        flex-direction: column;
        background-color: #31344b;
        width: fit-content;
        max-width: 30vmax;
        margin: 1.5vh;
        border-radius: 2.5vh;
        cursor: -webkit-grab;
        cursor: grab;
    }

    .issue-box:active {
        cursor: -webkit-grabbing;
        cursor: grabbing;
    }

    .issue-box > h3 {
        background-color: hsla(0, 0%, 0%, 0.25);
        padding: 1.5vmin;
        border-radius: 2.5vh;
        white-space: nowrap;
    }
</style>
