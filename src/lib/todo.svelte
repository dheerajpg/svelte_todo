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
    button.toggle{
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
        opacity:0.4;
        display: flex;
        align-items: center; 
        position: relative; 
    }

    .delete:hover,
    .delete:focus{
        transition: opacity 0.2s;
        opacity:1;
    }
    .done{
        transform: none;
        opacity:1;
        filter:drop-shadow(0px 0px 1px rgba(20, 20, 20, 0.1));
    }
     .done .toggle {
        border: none;
        display: flex;
        align-items: center; 
        position: relative; 
        top: 5px;
    }
    .svgtoggle{
        align-items: center; 
        position: relative; 
        top: 0.7rem;
        left:0.6rem;
    }

</style>

<div class="todo done">
    <form action="" method="">
        <input type="hidden" name="done" value="" />
        <svg class="svgtoggle" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M16.5001 8.99998C16.8906 9.3905 16.8906 10.0237 16.5001 10.4142L11.7072 15.2071C11.3167 15.5976 10.6835 15.5976 10.293 15.2071L8.0001 12.9142C7.60958 12.5237 7.60958 11.8905 8.0001 11.5C8.39063 11.1095 9.02379 11.1095 9.41432 11.5L11.0001 13.0858L15.0859 8.99998C15.1347 8.95116 15.1873 8.90845 15.2428 8.87184C15.6309 8.61556 16.1584 8.65827 16.5001 8.99998Z" fill="black"/>
            <path fill-rule="evenodd" clip-rule="evenodd" d="M22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12ZM20 12C20 16.4183 16.4183 20 12 20C7.58172 20 4 16.4183 4 12C4 7.58172 7.58172 4 12 4C16.4183 4 20 7.58172 20 12Z" fill="black"/>
            </svg>        
        <button aria-label="Mark as Done/Not Done"class="toggle"></button>    
    </form>

    <form action="" method="" class="text">
        <input type="text">
        <button aria-label="save your to-do" class="save"></button>
    </form>

    <form action="" method="">
        <button aria-label="Delete a to-do" class="delete"></button>

    </form>
</div>