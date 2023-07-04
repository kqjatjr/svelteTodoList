<!-- <input class="todo-input" placeholder="할일을 입력하세요"/>
<button class="todo-add-button">추가</button> -->

<script>
  export let todoValue;
  export let addTodo;
  export let handleKeyUp;
</script>


<div>
  <input class="todo-input" placeholder="할일을 입력하세요" bind:value={todoValue} on:keyup={e => handleKeyUp(e)}/>
  <button class="todo-button" on:click={addTodo}>추가</button>
</div>

<style>
  .todo-input {
    width: 300px;
    height: 50px;
    box-sizing: border-box;
    border-radius: 25px;
    padding-left: 10px;
  }

  .todo-button {
    height: 50px;
    width: 80px;
    box-sizing: border-box;
    border-radius: 25px;
    font-size: 20px;
  }
</style>