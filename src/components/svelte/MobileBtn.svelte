<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
  function toggleNav() {
    dispatch("toggleNav");
  }
  export let navIsOpen;
</script>

<button class="nav-bar-btn" class:navIsOpen on:click={toggleNav}>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    fill="none"
    viewBox="0 0 24 24"
    stroke-width="1.5"
    stroke="currentColor"
    class="icon-sm"
  >
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
    />
  </svg>
</button>

<style>
  button {
    display: flex;
    align-items: center;
    padding: 0;
    margin: 0;
    border: none;
    background: transparent;
    cursor: pointer;
    color: white;
  }
  .navIsOpen {
    display: none;
  }
</style>
