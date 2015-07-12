

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

