<script>
    let ph = " ";
    let signvalue = " ";
    let frst;
    let secnd;
    let operator;
    const a = ["+", "/", "-", "*"];
    let result;

    function clear() {
        ph = " ";
    }
    function filterdlist(e) {
        signvalue = " ";
        ph += e;
    }
    function op(sign) {
        frst = Number(ph);
        operator = sign;
        ph = " ";
        signvalue = sign;
    }

    function res() {
        secnd = Number(ph);

        if (operator === "+") {
            result = frst + secnd;
            ph = result.toString();
        } else if (operator === "/") {
            result = frst / secnd;
            ph = result.toString();
        } else if (operator === "*") {
            result = frst * secnd;
            ph = result.toString();
        } else {
            result = frst - secnd;
            ph = result.toString();
        }
    }
</script>

<main>
    <p>{ph} {signvalue}</p>
    <div class="container">
        <div class="btn">
            <button
                on:click={() => {
                    filterdlist(7);
                }}>7</button
            >
            <button
                on:click={() => {
                    filterdlist(8);
                }}>8</button
            >
            <button
                on:click={() => {
                    filterdlist(9);
                }}>9</button
            >
            <button class="delbtn">DEL</button>
        </div>
        <div class="btn">
            <button
                on:click={() => {
                    filterdlist(4);
                }}>4</button
            >
            <button
                on:click={() => {
                    filterdlist(5);
                }}>5</button
            >
            <button
                on:click={() => {
                    filterdlist(6);
                }}>6</button
            >
            <button
                on:click={() => {
                    op(a[0]);
                }}>+</button
            >
        </div>
        <div class="btn">
            <button
                on:click={() => {
                    filterdlist(1);
                }}>1</button
            >
            <button
                on:click={() => {
                    filterdlist(2);
                }}>2</button
            >
            <button
                on:click={() => {
                    filterdlist(3);
                }}>3</button
            >
            <button
                on:click={() => {
                    op(a[2]);
                }}>-</button
            >
        </div>
        <div class=" btn">
            <button
                on:click={() => {
                    filterdlist(".");
                }}>.</button
            >
            <button
                on:click={() => {
                    filterdlist(0);
                }}>0</button
            >
            <button
                on:click={() => {
                    op(a[1]);
                }}>/</button
            >
            <button
                on:click={() => {
                    op(a[3]);
                }}>*</button
            >
        </div>

        <div class="buttom">
            <button on:click={clear} class="reset">Reset</button>
            <button
                on:click={() => {
                    res();
                }}
                class="equal"
            >
                =
            </button>
        </div>
    </div>
</main>

<style>
    main {
        width: 540px;
    }
    p {
        width: 100%;
        height: 100px;
        border-radius: 10px;
        background-color: var(--screen-background);
        margin-bottom: 20px;
        font-size: 30px;
        color: var(--maintheme-color);
    }
    .btn {
        display: flex;
        justify-content: space-between;

        margin-bottom: 35px;
        font-size: 30px;
    }
    botton {
        color: hsl(221, 14%, 31%);
    }
    button {
        width: 94px;
        background-color: var(--mainrtheme-button);
        padding: 13px;
        text-align: center;
        box-shadow: 0px 3px 0px 0px var(--key-shadow);
    }
    .container {
        border-radius: 6px;
        padding: 40px;
        width: 100%;
        background-color: var(--keypad-background);
    }
    .buttom button {
        width: 49%;

        font-size: 28px;

        color: white;
        height: 58px;
    }
    .delbtn,
    .reset {
        background-color: var(--maintheme-resetbutton);
    }
    .equal {
        background-color: var(--maintheme-equalbutton);
        box-shadow: 0px 3px 0px 0px var(--equalkey-shadow);
    }
</style>
