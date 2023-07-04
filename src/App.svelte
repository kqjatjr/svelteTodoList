<svelte:head>

</svelte:head>

<script lang="ts">
  import Input from "./components/Input.svelte";
  import Todos from "./components/Todos.svelte";

  let todoValue = "";	
  let todoList = [];

  let lastId = 0;

  const addTodo = () => {
      if(todoValue) {
        const newTodo = {
          id: ++lastId,
          text: todoValue,
          completed: false
        }
        todoList = [...todoList, newTodo];
        todoValue = "";
      }
	}

  const removeTodo = (id: string) => {
    todoList = todoList.filter((prev) => prev.id !== id)
  }
	
	const handleKeyUp = e => {
		todoValue = e.target.value;
		if(e.keyCode === 13) {
			addTodo();
		}
	}
</script>

<main class="main-container">
  <div class="title">Todo List</div>
  <Input {todoValue} {addTodo} {handleKeyUp}/>
  <Todos {todoList} {removeTodo}/>
</main>

<style>
  .title {
    font-size: 30px;
  }
  .main-container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
</style>