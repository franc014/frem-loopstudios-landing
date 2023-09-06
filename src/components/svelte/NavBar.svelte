<script>
  import MobileBtn from "./MobileBtn.svelte";
  import CloseBtn from "./CloseBtn.svelte";
  let isOpen = false;

  function toggleNav() {
    isOpen = !isOpen;
  }
</script>

<div class="mobile-buttons">
  <MobileBtn navIsOpen={isOpen} on:toggleNav={toggleNav} />
  <CloseBtn navIsOpen={isOpen} on:toggleNav={toggleNav} />
</div>

<nav class="full-width" class:isOpen>
  <ul
    class="flex flex-col full-width gap items-center justify-center text-sm"
    style="--gap-size: 1rem; "
  >
    <li>About</li>
    <li>Careers</li>
    <li>Events</li>
    <li>Products</li>
    <li>Support</li>
  </ul>
</nav>

<style>
  nav {
    display: none;
    color: white;
    border: 1px solid hsl(var(--crl-white));
  }

  ul li {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 1rem 0;
    background-color: transparent;
    color: hsl(var(--crl-white));
  }

  .isOpen {
    display: block;
  }

  @media screen and (min-width: 850px) {
    nav {
      display: block;
    }
    .mobile-buttons {
      display: none;
    }
    ul {
      flex-direction: row;
      justify-content: flex-end;
    }
    ul li {
      width: auto;
      background-color: none;
    }

    nav {
      border: 1px solid hsl(var(--crl-white));
      margin-left: auto;
      width: auto;
      border: none;
    }
  }
</style>
