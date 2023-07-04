<svelte:head>

</svelte:head>

<script lang="ts">
  import Input from "./components/Input.svelte";
</script>

<main class="main-container">
  <div class="title">Todo List</div>
  <Input />
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