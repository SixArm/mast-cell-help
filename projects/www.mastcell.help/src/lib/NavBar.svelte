<script>
    import ListIntroduction from "$lib/ListIntroduction.svelte";
    import ListConditions from "$lib/ListConditions.svelte";
    import ListDiets from "$lib/ListDiets.svelte";
    import ListPrescriptions from "$lib/ListPrescriptions.svelte";
    import ListSupplements from "$lib/ListSupplements.svelte";
    import ListTherapies from "$lib/ListTherapies.svelte";
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
            <div class="collapse-title">Introduction</div>
            <div class="collapse-content"><ListIntroduction /></div>
          </div>
          <div class="collapse">
            <input type="radio" name="my-accordion-1" />
            <div class="collapse-title">Conditions</div>
            <div class="collapse-content"><ListConditions /></div>
          </div>
          <div class="collapse">
            <input type="radio" name="my-accordion-1" /> 
            <div class="collapse-title">Supplements</div>
            <div class="collapse-content"><ListSupplements /></div>
          </div>
          <div class="collapse">
            <input type="radio" name="my-accordion-1" /> 
            <div class="collapse-title">Diets</div>
            <div class="collapse-content"><ListDiets /></div>
          </div>
        </ul>
      </div>
      <a class="btn btn-ghost text-xl" href="/">MastCell.Help</a>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1">
        <li>
            <details>
                <summary>Introduction</summary>
                <ListIntroduction />
            </details>
        </li>
        <li>
            <details>
                <summary>Conditions</summary>
                <ListConditions />
            </details>
        </li>
        <li>
          <details>
              <summary>Supplements</summary>
              <ListSupplements />
          </details>
        </li>
        <li>
          <details>
              <summary>Diets</summary>
              <ListDiets />
          </details>
        </li>
      </ul>
    </div>
    <div class="navbar-end">
      <a class="btn">Button</a>
    </div>
  </div>
