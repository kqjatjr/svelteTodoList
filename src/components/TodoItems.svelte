<script>
  export let todo;
  export let removeTodo;
</script>

<div>
  <div>{todo.text}</div>
  <button on:click={removeTodo(todo.id)}>삭제</button>
</div>