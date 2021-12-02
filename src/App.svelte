<!-- https://svelte.dev/tutorial/event-modifiers -->
<!-- https://streamchaser.tv/ -->
<!-- https://simonwep.github.io/pickr/ -->
<!-- https://simeydotme.github.io/svelte-range-slider-pips/?ref=madewithsvelte.com -->


<script>
  import "./Tailwind.style.svelte"
  import AddList from "./components/AddList.svelte";
  import { todoList } from './store/Todo';
</script>


<div class="todolist-wrapper">
  <AddList/>

  {#if $todoList.
  length > 0}
    {#each $todoList as todo (todo.id)}
      <p>{todo.title}</p> 
    {/each}
  {/if}
</div>


<style lang="postcss">

  .todolist-wrapper{
    @apply w-full py-10 ;
  }

</style>