<script>

    import Timer from "./Timer.svelte";
    import Howto from "./howto.svelte";
    import { Styles  } from 'sveltestrap';

</script>
<Styles />

<h1 class="p-5 text-center"> Handwashing App </h1>

<div class="container">
    <div class="row justify-content-md-center mx-auto">
      <div class="col-md-6">            
            <Timer/>
      </div>
    </div>
    <div class="row justify-content-md-center mx-auto">
        <div class="col-md-6">
          <Howto/>
        </div>
    </div>
</div>


