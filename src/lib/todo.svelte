<style>
    .todo{
        display:grid;
        grid-template-columns: 2rem 1fr 2rem;
        grid-gap:0.5rem;
        align-items:center;
        margin:0 0 0.5rem 0;
        padding:0.5rem;
        background-color: #ff4322;
        border-radius: 10px;
        filter:drop-shadow(2px 4px 6px #262626);
        transform:translate(-1px, -1px);
        transition:filter 0.2s, transform 0.2s;

    }
    .todo button{
        width:2em;
        height:2em;
        border:none;
        background-color: transparent;
        background-position: 50% 50%;
        background-repeat: no-repeat;
        color:white;
    }
    .todo input{
        flex:1;
        padding: 0.5em 2em 0.5em 0.8em;
        border-radius: 10px;
        color:black;
    }
    .toggle{
        border: 1px solid black;
        border-radius:10px;
        box-sizing: border-box;
        background-size: 1em auto;
    }
    .text{
        position:relative;
        display:flex;
        align-items:center;
        flex:1;
    }
    .save{
        position:absolute;
        right:0;
        opacity:0;
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M48 96V416c0 8.8 7.2 16 16 16H384c8.8 0 16-7.2 16-16V170.5c0-4.2-1.7-8.3-4.7-11.3l33.9-33.9c12 12 18.7 28.3 18.7 45.3V416c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V96C0 60.7 28.7 32 64 32H309.5c17 0 33.3 6.7 45.3 18.7l74.5 74.5-33.9 33.9L320.8 84.7c-.3-.3-.5-.5-.8-.8V184c0 13.3-10.7 24-24 24H104c-13.3 0-24-10.7-24-24V80H64c-8.8 0-16 7.2-16 16zm80-16v80H272V80H128zm32 240a64 64 0 1 1 128 0 64 64 0 1 1 -128 0z"/></svg>'); 
    }
    .todo input:focus + .save,.save:focus{
        transition:0.4s;
        opacity: 1;
    }
    .delete{
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 448 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M135.2 17.7L128 32H32C14.3 32 0 46.3 0 64S14.3 96 32 96H416c17.7 0 32-14.3 32-32s-14.3-32-32-32H320l-7.2-14.3C307.4 6.8 296.3 0 284.2 0H163.8c-12.1 0-23.2 6.8-28.6 17.7zM416 128H32L53.2 467c1.6 25.3 22.6 45 47.9 45H346.9c25.3 0 46.3-19.7 47.9-45L416 128z"/></svg>');
        opacity:1;
    }

</style>

<div class="todo">
    <form action="" method="">
        <input type="hidden" name="done" value="" />
        <button aria-label="Mark as Done/Not Done" class="toggle">Done/Not Done</button>
    </form>

    <form action="" method="" class="text">
        <input type="text">
        <button aria-label="save your to-do" class="save"></button>
    </form>

    <form action="" method="">
        <button aria-label="Delete a to-do" class="delete"></button>

    </form>
</div>