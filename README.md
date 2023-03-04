# Example of bug in transcrypt

Link to the issue: [smudge context=default' failed 1](https://github.com/elasticdog/transcrypt/issues/158)


# transcrypt cipher and password

Output of `transcrypt --display`:
```
The current repository was configured using transcrypt version 2.2.2
and has the following configuration:

  GIT_WORK_TREE:  /tmp/testing2
  GIT_DIR:        /tmp/testing2/.git
  GIT_ATTRIBUTES: /tmp/testing2/.gitattributes

  CIPHER:   aes-256-cbc
  PASSWORD: qLdF5e0xkI6WP+zlzDczNOqHALotjfD/EwLsvKol

Copy and paste the following command to initialize a cloned repository:

  transcrypt -c aes-256-cbc -p 'qLdF5e0xkI6WP+zlzDczNOqHALotjfD/EwLsvKol'
```


# Steps to replicate

```
git clone https://github.com/AtomicFS/transcrypt_bug.git
```
```
transcrypt --cipher=aes-256-cbc --password="qLdF5e0xkI6WP+zlzDczNOqHALotjfD/EwLsvKol"
```

