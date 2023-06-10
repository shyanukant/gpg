## GPG (GNU Private Guard)/ PGP (Pretty Good Privacy)

1. Fork repo and open CodeSpace
2. Generate a GPG key
```bash
    gpg --gen-key
```
    `Enter you name, email and passphrase`
3. Find your key id
```bash
    gpg --list-secret-keys --keyid-format=long
```

4. Upload key to a key server
```bash
    gpg --send-keys <KEY ID>
```

5. Download my public key
```bash
    gpg --search-keys "rathishyanukant@gmail.com"
```
6. List all locally stored keys
```bash
    gpg --list-keys
```

### Sign Files using GPG

1. Create a `txt file` or any file and input anything and then sign your txt file
```bash
    gpg --sign --armor <YOUR.txt>
```

 Then enter the passphrae, it's generate `<YOUR.txt>.asc` file. This file sign your message of txt file.

2. To read the message, put the signed message into a file(.asc run) and run this command.

```bash
    gpg --decrypt <FILE NAME>.asc
```
We can read sign messages of anyone unless it is encrypted for a recipient
`Read my sign message, this for you`

### Encrypt/Decrypt Files using gpg
1. Encrypt your txt file for a specific recipient

```bash
    gpg --encrypt --armor \ --recipient <RECIPIENT'S EMIAL> <YOUR FILE>
```
Any Message for me😊
`Sent your Encrypt message in issue`
```bash
    gpg --encrypt --armor \ rathishyanukant@gmail.com <FILE NAME> 
```

2. The recipient(s) will be the only one who can decrypt the file
```bash
    gpg --decrypt <FILE NAME>
```

## Impersonate Another Github User

```bash
    GIT_COMMITTER_NAME="NAME" GIT_COMMITTER_EMAIL="EMAIL" \
    git commit --author="NAME <EMAIL>" -m "Your Commit Massage".
```