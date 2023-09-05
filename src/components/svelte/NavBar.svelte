<script>
    import MobileBtn from "./MobileBtn.svelte";
    import CloseBtn from "./CloseBtn.svelte";
    let isOpen = true;

    function toggleNav(){
        isOpen = !isOpen;
    }

</script>

<MobileBtn navIsOpen={isOpen} on:toggleNav={toggleNav} />
<CloseBtn  navIsOpen={isOpen} on:toggleNav={toggleNav}/>
<nav class="full-width" class:isOpen >
    <ul
        class="flex flex-col full-width items-center gap text-sm p-block"
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
    }
    .isOpen {
        background: blueviolet;
        display: block;
    }
</style>