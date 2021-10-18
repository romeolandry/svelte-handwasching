<script>
    export let progress = 0;


</script>

<style>
    .progress{
        margin: 20px ,0;
        border: solid rgb(194,194,194) 1px;
    }
    .progress-bar{
        background-color: rgb(77,199,55);
    }
</style>

<div class="progress rounded-0 mb-3">
    <div class="progress-bar" role="progressbar" style="width:{progress}%;" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100">{progress}%</div>
</div>