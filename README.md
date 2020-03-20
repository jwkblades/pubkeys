# Pubkeys

These are my public keys to various things, primarily programming related. In
the `gpg2` directory, you can find GPG signing keys, which I will be using to
sign my commits over time. They may be subject to change given time, and it is
possible that some may expire (depending on how paranoid I am about them).  

## Trusting My Keys

For those of you not familiar with signing keys, or how to add them to your
local (Linux) machine's trust, here are some quick instructions on how to do
that. If you are using a Mac, or Windows machine, I am sorry but you are on your
own there.  

### Importing the Key

```
$ gpg2 --import ./gpg2/keyName.gpg
```

The next step is to trust the public keys in the master branch of this
repository. That can be done via the following commands:  
```
$ gpg2 --edit-key keyName.gpg
gpg> trust
gpg> save
$ gpg2 --lsign-key keyName.gpg
```

I would suggest _not_ going above a trust level of 4 for anyone's keys that you
aren't exchanging in person, but the choice is completely yours.  

The `--lsign-key` makes it so the key can no longer be exported from your local
machine.  

Run through this process for each of the keys in this directory you want to add.  
