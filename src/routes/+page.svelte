<script>
	import Todo from "$lib/todo.svelte";
</script>

<svelte:head>
    <title>To-Do</title>
</svelte:head>

<h1>To-Do</h1>
<form action ="" method="">
    <input type="text" name="text" aria-label="add a todo" placeholder = "+Add a todo"/>
</form>

<Todo />