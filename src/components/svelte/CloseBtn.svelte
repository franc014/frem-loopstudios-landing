<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
  function toggleNav() {
    dispatch("toggleNav");
  }
  export let navIsOpen;
</script>

<button class:navIsOpen on:click={toggleNav}>
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
      d="M9.75 9.75l4.5 4.5m0-4.5l-4.5 4.5M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
    />
  </svg>
</button>

<style>
  button {
    display: none;
    align-items: center;
    padding: 0;
    border: none;
    cursor: pointer;
    background: transparent;
    color: white;
  }

  .navIsOpen {
    display: flex;
  }
</style>
