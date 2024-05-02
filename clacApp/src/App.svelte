<script>
  import { fly } from "svelte/transition";
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";
  import Ans from "./lib/ans.svelte";
  import Numb from "./lib/buttons.svelte";
  import theme from "./lib/theme.svelte";
  import Theme from "./lib/theme.svelte";
</script>

<main>
  <Theme></Theme>
  <div class="calc">calc</div>
  <Ans></Ans>
  <Numb></Numb>
  <div class="attribution">
    Challenge by <a
      href="https://www.frontendmentor.io?ref=challenge"
      target="_blank">Frontend Mentor</a
    >. Coded by <a href="#">Maryiam Reda</a>.
  </div>
</main>

<style>
  .calc {
    width: 17%;
    color: var(--maintheme-color);
    margin-bottom: 20px;
    font-weight: 700;
    font-size: 50px;
  }

  .attribution {
    font-size: 11px;
    text-align: center;
  }
  .attribution a {
    color: hsl(228, 45%, 44%);
  }
</style>
