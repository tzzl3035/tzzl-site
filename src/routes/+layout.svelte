<script>
  import { dark } from "$lib/stores/dark";
  let { children } = $props();
</script>

<div
  style="
  height: 100%;
"
  style:background={$dark ? "#222" : "white"}
  style:color={$dark ? "white" : "black"}
>
  <div
    style="height: 3.7em;
  border-bottom: 1px solid #ccc;
  "
  >
    <a href="/" style:color={$dark ? "white" : "#444"}>
      <img
        alt=""
        src="/favicon.png"
        style="
        width: 3.7em;
        position: absolute;
        left: 2em;
    "
      />
      <div
        style="
    margin: 0 0 0 3em;
    padding: 0.7em;
    font-size: 1.5em;
    display: inline-block;
  "
      >
        tzzl.site
      </div>
    </a>
    <button
      style="
    border: none;
    border-radius: 3px;
    height: 2.3em; width: 2.3em;
    position: absolute;
    right: 20%;
    top: 1em;
  "
      style:background={$dark ? "#4f4f4f" : "white"}
      style:box-shadow={$dark ? "0 1px 1px 0 white" : "1px 0 0 1px #777"}
      style:color={$dark ? "#e3e3e3" : "black"}
      onclick={() => ($dark = 1 - $dark)}>{$dark ? "W" : "D"}</button
    >
    <div
      style="
        display: inline-block;
        position: absolute;
        right: 4em;
        top:0.8em;
        font-size: 1.2em;
    "
    >
      <a
        href="https://github.com/tzzl3035/tzzl-site"
        style:color={$dark ? "#325fcd" : "#273e75"}
      >
        Github Repo ↗
      </a>
    </div>
  </div>

  {@render children()}
</div>

<style>
  div {
    font-family: "Georgia";
    transition: 0.1s;
  }
</style>
