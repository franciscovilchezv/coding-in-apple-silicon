## Theory

### Key-exchange

Key-exchange is a method for generating a secret key along with another client without interchanging the key.

https://www.youtube.com/watch?v=pa4osob1XOk

### Cryptography

https://www.youtube.com/watch?v=jhXCTbFnK8o

La encriptacion puede ser simetrica o asimetric, dependiendo de si se comparte o no el secret key.

### Public key

Utilizado para la encriptación.

### Secret key

Utilizado para la desencriptación.

## Requirements

In order to user pass, you must have a key created in your local computer which will be used for encryption.

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

#### Secret key

Binary file:

`gpg --export-secret-keys 3D38A8734AE22785E5AE8604E1708C2E03E1E62A > file`

Armored ASCII file

`gpg --export-secret-keys -a 3D38A8734AE22785E5AE8604E1708C2E03E1E62A > file`

#### Public key

`gpg --export -a 3D38A8734AE22785E5AE8604E1708C2E03E1E62A > file`

### Change your passphrase it

https://help.ubuntu.com/community/GnuPrivacyGuardHowto#Changing_your_Passphrase

### `pass` usage

```
brew install pass
pass init 851B42F5855E6D53EF6CC52459434BB9492BFCA3
```

### View `pass` in iPhone

https://mssun.github.io/passforios/

You need to use ssh as authentication. 

Type the URL that you copy paste from github ssh option in the following format:

`ssh://git@github.com/repo_owner/repo_name.git`

You need to use `git` a.sthe username.

You will need to provide the `ssh key` which is usually located in ~/.ssh. 

In case you don't, set up an shh key:

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh
