<script>
  import {todoList} from "../store/Todo";

  let value="";
  const addTodo = () =>{
    todoList.update(n=>n.concat({title : value, id : Math.random()}))
    value = ""
  }
</script>


<div class="flex w-full justify-center items-center">
  <form class="flex justify-center" on:submit|preventDefault={addTodo}>
    <input placeholder="Type Todo" class=" px-2 border border-black" bind:value={value} type="text">
    <button class="ml-2 bg-red-500 px-3 py-2" type="submit">Add Todo</button>
  </form>
</div>
