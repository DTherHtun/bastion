```
$ kubect create -f bastion.yaml
$ kubectl -n development port-forward pod/bastion 1234:22
$ ssh -p 1234 root@localhost -L 5432:postgres:5432
$ nc -vvv localhost 5432 #or use postgres with localhost:5432
$ kubect delete -f bastion.yaml # must be delete for security reason.
```

