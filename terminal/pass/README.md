## Theory

Key-exchange is a method for generating a secret key along with another client without interchanging the key.

https://www.youtube.com/watch?v=pa4osob1XOk

Cryptography

https://www.youtube.com/watch?v=jhXCTbFnK8o

La encriptacion puede ser simetrica o asimetric, dependiendo de si se comparte o no el secret key.

## Requirements

In order to user pass, you must have a key created in your local computer which iwll be used for encryption.

https://www.passwordstore.org/

### Management of keys with `gpg`

[Guide](http://irtfweb.ifa.hawaii.edu/~lockhart/gpg/)

- List keys

`gpg --list-keys`

- Delete key

`gpg --delete-key key-ID`

#### Create a private key

```
gpg --full-generate-key
1
4096
0


pub   rsa4096 2021-12-25 [SC]
      851B42F5855E6D53EF6CC52459434BB9492BFCA3
uid                      francisco <email>
sub   rsa4096 2021-12-25 [E]
```

This will generate a private a public key, both identified with `851B42F5855E6D53EF6CC52459434BB9492BFCA3`.

### Importing

https://www.gnupg.org/gph/en/manual/x56.html

Trust public key after import

gpg --edit-key <KEY_ID>
gpg> trust

### Export

gpg --export-secret-keys 3D38A8734AE22785E5AE8604E1708C2E03E1E62A > file

gpg --export -a 3D38A8734AE22785E5AE8604E1708C2E03E1E62A > > file

### `pass`

```
brew install pass
pass init 851B42F5855E6D53EF6CC52459434BB9492BFCA3
```

### View `pass` in iPhone

https://mssun.github.io/passforios/

You need to use ssh as authentication. Type the exact URL that you cpy paste from github ssh option, and use `git` as the user in the app
