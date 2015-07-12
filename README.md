## Help
Most of the time, `man <command-name>` will give you the documentation on the command usage.

```
man ls
```

## Char Escaping

`\` escapes `"` chars.

```
echo "\"Hello World\""
```

This prints out `"Hello World"`.

## Executing a Script Inside a File
When you save a file named `hw` under the current directory and try to excecute it by running `hw`, 
it will not run the file as it will try to find it as a global command. You can run `./hw` to run the command 
file `hw` under the current directory.

However, you also need to give the file execute permission. Otherwise, you will get the following error:

> bash: ./hw: Permission denied 

First, let's list the permissions on the file:

```
ls -l hw
```

This got me the following output:

> -rw-rw-r-- 1 tugberk tugberk 20 Jul 12 02:29 hw

The first part, `rw` means that I have read and write permission on the file. The `-` after the `rw` means that 
I don't have executeble permission on the file. To give executable permission, we can use Change Mode command (`chmod`).

```
chmod u+x hw
```

The `u` part of the `u+x` here means that it is a user permission and it will give the permission for the user who owns this 
file. `+x` part here means that I want to add executable permission. After running this command, you can see the 
executable permission added by running `ls -l hw`:

> -rwxrw-r-- 1 tugberk tugberk 20 Jul 12 02:29 hw

You can revoke the executable permission by using the `-` instead of `+`:

```
chmod u-x hw
```



