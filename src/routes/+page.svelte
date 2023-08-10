<script>
    import "/src/app.css"
	import Todo from "$lib/todo.svelte";
</script>

<style>
    .Tododiv{
        width:100%;
        max-width: 42rem;
        margin: 4rem auto 0rem auto;
    }

</style>

<svelte:head>
    <title>To-Do</title>
</svelte:head>
<div class = "Tododiv">
<h1>To-Do</h1>
<form action ="" method="">
    <input type="text" name="text" aria-label="add a todo" placeholder = "+Add a todo"/>
</form>

<Todo />
<Todo />
<Todo />
</div>