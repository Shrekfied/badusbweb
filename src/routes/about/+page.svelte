<script>
    import titleStore from "$lib/stores/titleStore";

    titleStore.set("About");
</script>

<p>
    <b>Control Panel Version:</b> <span>{process.env.npm_package_version}</span>
    <br/>
    <b>API Location</b>: <span>https://usbpi</span>
</p>