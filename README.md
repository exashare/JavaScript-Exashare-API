# JavaScript-Exashare-API
A Web Service for the Exashare API

Account Info
------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.AccountInfo(
        {
            key: 'your_key'
        },
        function(result){
            console.log(result.login);
            console.log(result.money);
        }
    );
</script>

```

Add URL upload
--------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.UploadURL(
        {
            key: 'your_key',
            url: 'http://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4',
            folder: 'name_your_folder'
        },
        function(result){
            console.log(result.queue_id);
        }
    );
</script>

```

Check URL Upload
----------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.CheckUploadURL(
        {
            key: 'your_key',
            id: 'queue_id'
        },
        function(result){
            console.log(result.status);
            console.log(result.url);
            console.log(result.file_code);
        }
    );
</script>

```
