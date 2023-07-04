<script>
  import TodoItems from "./TodoItems.svelte";
  export let todoList;
  export let removeTodo;
</script>

<div>  
{#if todoList && todoList.length > 0}
  {#each todoList as todo }
  <TodoItems {todo} {removeTodo}/>
{/each}
{:else}
  <p></p>
{/if}
</div>