<script>
  import titleStore from "$lib/stores/titleStore";

  titleStore.set("Terminal");
</script>

<div class="terminal">
  <pre>
   <span style="color:#8AE234;"><b>pi@raspberrypi</b></span>:<span style="font-weight: bold; color:#729FCF"> <b>~/test</b></span> $ ls
   <span>file  file1</span>
   <span style="color:#8AE234;"><b>pi@raspberrypi</b></span>:<span style="font-weight: bold; color:#729FCF"> <b>~/test</b></span> $ _
  </pre>
</div>

<style>
  .terminal {
    background: black;
    color: white;
    padding: 10px;
    height:  500px;
    overflow: hidden;
    font-weight:bolder;
  }
</style>