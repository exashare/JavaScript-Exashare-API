# JavaScript-Exashare-API
A Web Service for the Exashare API

Account info
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
