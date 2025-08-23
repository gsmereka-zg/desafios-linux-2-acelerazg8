

1. (B)
tar -xzf challenges.tar.gz 

2. (B)
cd challenges

3. (B)
ls . (ls --help for more options)
## Problema 4-b
```bash
mkdir foo
```


## Problema 5-i
```bash
mkdir -p foo/bar/1/2/3

```


## Problema 6-b
```bash
rm -rf foo
```


## Problema 7-b
```bash
echo "Hello World"
```


## Problema 8-b
```bash
echo "Hello World" > hello.txt
```


## Problema 9-b
```bash
touch empty.txt
```


## Problema 10-b
```bash
rm empty.txt
```


## Problema 11-i
```bash
echo "" > empty.txt
```


## Problema 12-i
```bash
> empty.txt
```


## Problema 13-b
```bash
cat hello.txt > goodbye.txt
```


## Problema 14-b
```bash
mv goodbye.txt hello_copy.txt
```


## Problema 15-i
```bash
cmp hello.txt hello_copy.txt
```


## Problema 16-b
```bash
cat hello.txt hello_copy.txt > 2_hellos.txt
```

## Problema 17-b
```bash
pwd
```


## Problema 18-b
```bash
ls -l
```

## Problema 19-b
```bash
chmod +w restricted.txt && echo 'some text' >> restricted.txt
```

## Problema 20-b
```bash
./hello_executable
```


## Problema 21-b
```bash
chmod +x ./hello_executable && ./hello_executable
```


## Problema 22-b
```bash
gcc compile_me.c -o compilei && ./compilei
```


## Problema 23-a
```bash
./redirect 2>output.txt 1>>output.txt
```


## Problema 24-b
```bash
date
```


## Problema 25-b
```bash
ps aux
```


## Problema 26-b
```bash
nproc
```

