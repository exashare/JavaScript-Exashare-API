# JavaScript Exashare API
A Web Service for the Exashare API

## VERSION API
0.01

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
            if(!result.error){
                console.log(result.login);
                console.log(result.money);
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```

Add URL Upload
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
            if(!result.error){
                console.log(result.queue_id);
            }else{
                console.log(result.error);
            }
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
            if(!result.error){
                console.log(result.status);
                console.log(result.url);
                console.log(result.file_code);
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```

Upload Server Request
---------------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.GetUploadServer(
        {
            key: 'your_key'
        },
        function(result){
            if(!result.error){
                console.log(result.url);
                console.log(result.srv_id);
                console.log(result.disk_id);
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```

Check Files
-----------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.CheckFiles(
        {
            key: 'your_key',
            files: [
                1a1a1a1a1a1a,
                1b1b1b1b1b1b,
                2c2c2c2c2c2c
            ]
        },
        function(result){
            if(!result.error){
                for(var row in result){
                    console.log(result[row].file_code);
                }
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```

Renew File code
---------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.RenewFile(
        {
            key: 'your_key',
            file_code: '1a1a1a1a1a1a'
        },
        function(result){
            if(!result.error){
                console.log(result.file_code);
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```

Clone File code
---------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.CloneFile(
        {
            key: 'your_key',
            file_code: '1a1a1a1a1a1a',
            folder: 'name_your_folder',
            new_title: 'new_title_to_file_cloned'
        },
        function(result){
            if(!result.error){
                console.log(result.file_code);
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```

Check Files DMCA
----------------

```

<script src="ExashareAPI.js"></script>
<script>
    ExashareAPI.CheckFilesDMCA(
        {
            key: 'your_key',
            date: 'YYYY-MM-DD',
            order: 'down'
        },
        function(result){
            if(!result.error){
                for(var row in result){
                    console.log(result[row].file_code);
                    console.log(result[row].dmca_created);
                    console.log(result[row].dmca_expire);
                }
            }else{
                console.log(result.error);
            }
        }
    );
</script>

```
