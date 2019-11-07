# backup-reader

## Create credentials

After deploy, log in `backup-reader-nginx` running container and run the following commands, replacing `${USER}` value with desired usernames (one each time):

```
$ apk add openssl
$ export USER="user1"
$ echo "${USER}:$(openssl passwd)" > /htpasswd/${USER}
```

You will be prompted to enter password twice for each user, and then they will be able to login.
