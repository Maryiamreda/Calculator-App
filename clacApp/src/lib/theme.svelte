<script>
    function changetheme(e) {
        if (e == 2) {
            document.body.classList.remove("thirdtheme");

            document.body.classList.add("scndtheme");
        } else if (e == 3) {
            document.body.classList.remove("scndtheme");
            document.body.classList.add("thirdtheme");
        } else {
            document.body.classList.remove("scndtheme", "thirdtheme");
        }
    }
</script>

<main>
    <div class="themes">
        <button
            class="st"
            on:click={() => {
                changetheme(1);
            }}>1</button
        >
        <button
            on:click={() => {
                changetheme(2);
            }}
        >
            2
        </button>
        <button
            class="rd"
            on:click={() => {
                changetheme(3);
            }}>3</button
        >
    </div>
    <input type="radio" />
    <label> </label>
</main>

<style>
    button {
        padding: 10px;
        border: none;
        outline: none;
        background: none;
        color: var(--maintheme-color);
        background-color: transparent;
    }
    button:focus {
        outline: none;
    }

    div {
        display: inline-flex;
    }
    .themes {
        font-size: 30px;
        padding-left: 407px;
    }

    label {
        width: 120px;
        height: 50px;
        position: relative;
        left: 75%;
        display: block;
        background: var(--keypad-background);
        border-radius: 200px;

        cursor: pointer;
    }
    label:after {
        content: "";
        width: 33px;
        height: 33px;
        position: absolute;
        top: 10px;
        left: 10px;
        background-color: var(--maintheme-equalbutton);
        /* background: linear-gradient(180deg, #ffcc89, #d8860b); */
        border-radius: 180px;
        box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2);
    }

    :global(.scndtheme label:after) {
        transform: translateX(90%);
    }
    :global(.thirdtheme label:after) {
        transform: translateX(170%);
    }
    input {
        width: 0;
        height: 0;
        visibility: hidden;
    }
    /* 
    input:checked + label {
        background: #242424;
    }
    input:checked + label:after {
        left: 490px;
        transform: translateX(-100%);
        background: linear-gradient(180deg, #777, #3a3a3a);
    }
    label,
    label:after {
        transition: 0.3s;
    } */
</style>
