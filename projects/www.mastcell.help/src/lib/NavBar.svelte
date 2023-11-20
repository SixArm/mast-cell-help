<script>
    import NavBarIntroduction from "$lib/NavBarIntroduction.svelte";
    import NavBarConditions from "$lib/NavBarConditions.svelte";
    import NavBarDiets from "$lib/NavBarDiets.svelte";
    import NavBarPrescriptions from "$lib/NavBarPrescriptions.svelte";
    import NavBarSupplements from "$lib/NavBarSupplements.svelte";
    import NavBarTherapies from "$lib/NavBarTherapies.svelte";
</script>

<style lang="postcss">
.collapse {
  @apply bg-base-200;
}
.collapse-title {
  @apply text-xl font-medium;
}
</style>

<div class="navbar bg-base-100">
    <div class="navbar-start">
      <div class="dropdown">
        <label tabindex="0" class="btn btn-ghost lg:hidden">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" /></svg>
        </label>
        <ul class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52">
          <div class="collapse">
            <input type="radio" name="my-accordion-1" checked="checked" /> 
            <div class="collapse-title">
              Introduction
            </div>
            <div class="collapse-content"> 
              <NavBarIntroduction />
            </div>
          </div>
          <div class="collapse">
            <input type="radio" name="my-accordion-1" /> 
            <div class="collapse-title">
              Conditions
            </div>
            <div class="collapse-content"> 
              <NavBarConditions />
            </div>
          </div>
        </ul>
      </div>
      <a class="btn btn-ghost text-xl">daisyUI</a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li>
            <details>
                <summary>Introduction</summary>
                <NavBarIntroduction />
            </details>
        </li>
        <li>
            <details>
                <summary>Conditions</summary>
                <NavBarConditions />
            </details>
        </li>
      </ul>
    </div>
    <div class="navbar-end">
      <a class="btn">Button</a>
    </div>
  </div>
