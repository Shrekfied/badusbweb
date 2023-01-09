<script>
    import titleStore from "$lib/stores/titleStore";

    titleStore.set("Ducky Script");
</script>

<textarea id="w3review" name="w3review" rows="20" cols="50">REM Insert DuckyScript Here</textarea>
<br>
<br>
<button class="submit-button">Run</button>
<button class="button">Run on Startup</button>

<style>
    textarea {
        font-size: 14px;
        font-family: Courier New;
    }
</style>
