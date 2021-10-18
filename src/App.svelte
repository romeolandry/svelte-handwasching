<script>

    import Timer from "./Timer.svelte";
    import Howto from "./Howto.svelte";
    import { Styles  } from 'sveltestrap';
   
    let audio;

    function TimerEnds(event){
      audio.play();
    }
</script>
<Styles />

<!-- <h1 class="p-5 text-center"> Handwashing App </h1> -->

<div class="container">
    <div class="row justify-content-md-center mx-auto">
      <div class="col-md-6">            
            <Timer on:end={TimerEnds} />
      </div>
    </div>
    <div class="row justify-content-md-center mx-auto">
        <div class="col-md-6">
          <Howto/>
        </div>
    </div>
</div>


<audio bind:this="{audio}" src="sound.wav"></audio>
