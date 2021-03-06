# catacomb

Encrypts content using public keys from GitHub.
Encrypted files can then be decrypted using the matching `~/.ssh/id_rsa`.

## Installation

Using [fresh], run the following:

``` sh
fresh twe4ked/catacomb bin/catacomb --bin
```

Manually:

``` sh
mkdir ~/bin/
wget https://raw.github.com/twe4ked/catacomb/master/bin/catacomb ~/bin/catacomb
export PATH="$PATH:~/bin/"
# the PATH will need to be set in your shell config
```

## Usage

### Encrypting

``` sh
catacomb $recipients_github_username < file.txt > encrypted.txt
```

### Decrypting

``` sh
catacomb < encrypted.txt
```

## Notes

* Encrypts using the first key retrieved from GitHub
* Decrypts using `~/.ssh/id_rsa`

## Licence

MIT.

[fresh]: https://github.com/freshshell/fresh
