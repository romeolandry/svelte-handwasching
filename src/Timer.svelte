<script>
    import { Progress } from "sveltestrap";
    import { createEventDispatcher, SvelteComponentTyped } from 'svelte';
    import ProgressBar from "./ProgressBar.svelte"
    const totalSeconds= 20;
    let secondleft =  totalSeconds;
    let activeClick = '';

    $: progressvalue = ((totalSeconds - secondleft) / totalSeconds)*100;

    const dispatch = createEventDispatcher();
     
    function startTimer(){
        activeClick = 'disabled';
        const timer = setInterval(() => {
            secondleft -=1;
            if(secondleft<0){
                dispatch('end');
                clearInterval(timer);
                activeClick = '';
                secondleft = totalSeconds;
            }
        }, 100);
    };
</script>

<style>
    .btn-outline-secondary{
        background-color: rgb(154, 73, 73);
        border: 1px;
    }
</style>

<div>
    <h2>Seconf Left: {secondleft}</h2>
</div>

<div>
    <ProgressBar bind:progress={progressvalue} />
</div>

<button class="btn btn-outline-secondary w-100 rounded-0 mb-3 {activeClick} " on:click="{startTimer}"> Start </button>