

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


## Problema 27-b
```bash
uname -r
```


## Problema 28-b
```bash
grep -rl "You found the needle in the haystack!" bunch_of_files/
```


## Problema 29-b
```bash
head -n 25 people.csv
```


## Problema 30-b
```bash
tail -n 25 people.csv
```


## Problema 31-i
```bash
diff greeting1.txt greeting2.txt
```


## Problema 32-i
```bash
echo "Hello" && sleep 5 && echo "world!"
```


## Problema 33-i
```bash
yes 0 | tr -d '
' | head -c 1M > zeros.txt
```


## Problema 34-i
```bash
dd if=/dev/urandom of=random2MB.bin bs=1M count=2
```


## Problema 35-i
```bash
wc -l ../CHALLENGE_README.txt
```


## Problema 36-b
```bash
tac ../CHALLENGE_README.txt
```


## Problema 37-i
```bash
cut -d',' -f2 people.csv
```


## Problema 38-a
```bash
cut -d',' -f2 people.csv              | sort | uniq | wc -l
```


## Problema 39-a
```bash
cut -d',' -f2 people.csv | tail -n +2 | sort | uniq | wc -l
```


## Problema 40-a
```bash
cut -d',' -f2 people.csv | sed 1d | sort | uniq | wc -l
```


## Problema 41-a
```bash
time
```


## Problema 42-a
```bash
cat people.csv | cut -d',' -f4 | grep -c 'Josiah'
```


## Problema 43-i
```bash
find . -type f | wc -l
```


## Problema 44-i
```bash
find . -type d | wc -l
```


## Problema 45-i
```bash
find . -type f -name "*deleteme*" -delete
```


## Problema 46-i
```bash
grep -rl 'You found the needle in the haystack!' bunch_of_files/ | xargs sed -i 's/You found the needle in the haystack!/The needle has been removed./'
```


## Problema 47-a
```bash
cat people.csv | tr ',' '|' > people_pipe.csv
```


## Problema 48-A
```bash
fdupes bunch_of_files/
```


## Problema 49-a
```bash
install -D /dev/null f/supercalifragilisticexpialidocious.txt && rm f/*
```


## Problema 50-a
```bash
touch {a..c}-{1..3}.txt
```

