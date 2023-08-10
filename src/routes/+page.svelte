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
    .Tododiv h1{
        align-items: center;
    }
    .new{
        margin: 0 0 0.5rem 0;
    }
    .new input{
        font-size:28px;
        width:100%;
        padding: 0.5em 0em 0.4em 0em;
    }
    .Tododiv :global(input){
        text-align: center;
        border: 1px solid transparent;
        border-radius: 10rem;
    }
</style>

<svelte:head>
    <title>To-Do</title>
</svelte:head>
<div class = "Tododiv">
<h1>To-Do</h1>
<form action ="" method="" class="new">
    <input type="text" name="text" aria-label="add a todo" placeholder = "+Add a todo"/>
</form>

<Todo />
<Todo />
<Todo />
</div>