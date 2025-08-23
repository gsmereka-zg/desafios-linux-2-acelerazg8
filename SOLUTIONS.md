# Linux Command Line Challenges - Soluções

## Problema 1-b
Extract the "challenges.tar.gz" archive; you'll need its contents to
   solve some of the challenges.
```bash
tar -xzf challenges.tar.gz
```


## Problema 2-b
Change your working directory to the "challenges" directory that was
   created when you extracted "challenges.tar.gz"
```bash
cd challenges
```


## Problema 3-b
List the contents of the "challenges" directory.
```bash
ls .
```


## Problema 4-b
Create a new directory named "foo".
```bash
mkdir foo
```


## Problema 5-i
Create a new directory named "foo/bar/1/2/3"
```bash
mkdir -p foo/bar/1/2/3

```


## Problema 6-b
Remove the directory "foo" and all of its contents
```bash
rm -rf foo
```


## Problema 7-b
Print the text "Hello World".
```bash
echo "Hello World"
```


## Problema 8-b
Create a file named "hello.txt" that contains the text "Hello World".
```bash
echo "Hello World" > hello.txt
```


## Problema 9-b
Create an empty file named "empty.txt"
```bash
touch empty.txt
```


## Problema 10-b
Remove the file "empty.txt"
```bash
rm empty.txt
```


## Problema 11-i
Find a second way to solve challenge 9.
```bash
echo "" > empty.txt
```


## Problema 12-i
Find a third way to solve challenge 9.
```bash
> empty.txt
```


## Problema 13-b
Copy "hello.txt" and name the copy "goodbye.txt".
```bash
cat hello.txt > goodbye.txt
```


## Problema 14-b
Rename "goodby.txt" to "hello_copy.txt".
```bash
mv goodbye.txt hello_copy.txt
```


## Problema 15-i
Prove that the contents of "hello.txt" and "hello_copy.txt" are identical.
```bash
cmp hello.txt hello_copy.txt
```


## Problema 16-b
Concatenate the contents of "hello.txt" and "hello_copy.txt" and store the result in a file named "2_hellos.txt".
```bash
cat hello.txt hello_copy.txt > 2_hellos.txt
```

## Problema 17-b
Get the full path of your present working directory ("challenges").
```bash
pwd
```


## Problema 18-b
List the contents of the "challenges" directory (like challenge 3), but show the permissions for each file.

```bash
ls -l
```

## Problema 19-b
Append some text to the end of "restricted.txt". It's OK to do this in 2 steps.
```bash
chmod +w restricted.txt && echo 'some text' >> restricted.txt
```

## Problema 20-b
Run the "hello_executable" program.
```bash
./hello_executable
```


## Problema 21-b
Run the "challenge_20" program. It's OK to do this in 2 steps.
```bash
chmod +x ./hello_executable && ./hello_executable
```


## Problema 22-b
Compile and run "compile_me.c". It's OK to do this in 2 steps.
```bash
gcc compile_me.c -o compilei && ./compilei
```


## Problema 23-a
Run the "redirect" program and collect all of its output in a file named "output.txt".
```bash
./redirect 2>output.txt 1>>output.txt
```
> Alternativa: `./redirect &> output.txt`


## Problema 24-b
Get the current date and time.
```bash
date
```


## Problema 25-b
Show all of the running processes on your computer.
```bash
ps aux
```


## Problema 26-b
Show the number of processors/cores in your computer.
```bash
nproc
```
> Alternativa: `lscpu | grep '^CPU(s):'`


## Problema 27-b
Find out what version of the Linux kernel is currently running.
```bash
uname -r
```


## Problema 28-b
Find the file in the "bunch_of_files/" directory that contains the string: "You found the needle in the haystack!"
```bash
grep -rl "You found the needle in the haystack!" bunch_of_files/
```


## Problema 29-b
Print the first 25 lines of people.csv.
```bash
head -n 25 people.csv
```


## Problema 30-b
Print the last 25 lines of people.csv.
```bash
tail -n 25 people.csv
```


## Problema 31-i
Display just the differences between greeting1.txt and greeting2.txt
```bash
diff greeting1.txt greeting2.txt
```


## Problema 32-i
Print "Hello", then wait 5 seconds, then print "world!".
```bash
echo "Hello" && sleep 5 && echo "world!"
```


## Problema 33-i
Create a 1MB file full of zeros.
```bash
yes 0 | tr -d '
' | head -c 1M > zeros.txt
```
> Alternativa: `dd if=/dev/zero of=zeros.txt bs=1M count=1`

## Problema 34-i
Create a 2MB file full of random data.
```bash
dd if=/dev/urandom of=random2MB.bin bs=1M count=2
```


## Problema 35-i
Count the number of lines in README.txt.
```bash
wc -l ../CHALLENGE_README.txt
```


## Problema 36-b
Display the contents of README.txt in reverse (last line first).
```bash
tac ../CHALLENGE_README.txt
```


## Problema 37-i
Display all of the last names in people.csv.
```bash
cut -d',' -f2 people.csv
```
> Alternativa: `awk -F',' '{print $2}' people.csv`


## Problema 38-a
Count the number of unique last names in people.csv.
```bash
cut -d',' -f2 people.csv | sort | uniq | wc -l
```


## Problema 39-a
Count the number of unique last names in people.csv.
```bash
cut -d',' -f2 people.csv | tail -n +2 | sort | uniq | wc -l
```


## Problema 40-a
There's a second way to exclude the CSV header from your count. Find it.
```bash
cut -d',' -f2 people.csv | sed 1d | sort | uniq | wc -l
```


## Problema 41-a
Now that you've found two ways to correctly count the number of unique last names in people.csv, can you prove whether or not one is more efficient (faster) than the other?
```bash
time
```
> Nota: comparar eficiência de métodos usando `time` com cada comando alternativo


## Problema 42-a
Count the number of people with the first name "Josiah" in people.csv.
```bash
cat people.csv | cut -d',' -f4 | grep -c 'Josiah'
```


## Problema 43-i
Count the number of files (not directories) in the "challenges" directory .
```bash
find . -type f | wc -l
```


## Problema 44-i
Count the number of subdirectories in the "challenges" directory.
```bash
find . -type d | wc -l
```
> Alternativa: `ls -l | grep ^d | wc -l`


## Problema 45-i
Remove all files with "deleteme" in the name.
```bash
find . -type f -name "*deleteme*" -delete
```
> Alternativa: `rm *deleteme*`


## Problema 46-i
In challenge 28 you found a file. Replace the string "You found the needle in the haystack!" with "The needle has been removed."
```bash
grep -rl 'You found the needle in the haystack!' bunch_of_files/ | xargs sed -i 's/You found the needle in the haystack!/The needle has been removed./'
```


## Problema 47-a
Transform people.csv from ',' delimited to '|' delimited and save the result in people_pipe.csv.
```bash
cat people.csv | tr ',' '|' > people_pipe.csv
```


## Problema 48-A
Find all of the files in "bunch_of_files/" that are duplicates of "file001.rand".
```bash
fdupes bunch_of_files/
```
> Alternativa: `md5sum bunch_of_files/* | sort | uniq -w32 -d`


## Problema 49-a
Execute this challenge in exactly 2 steps:
1) (B) Create an empty file named "supercalifragilisticexpialidocious.txt".
2) (A) Remove "supercalifragilisticexpialidocious.txt". Your command may     only use a maximum 5 total characters (no wildcards or globs).
```bash
install -D /dev/null f/supercalifragilisticexpialidocious.txt && rm f/*
```
> Nota: usa menos 5 caracteres no comando para remover o arquivo.


## Problema 50-a
Create a set of empty files. Each file has a name in the form "L-N.txt" where L is a letter and N is a number. Valid letters are a,b,c, while valid numbers are 1,2,3. Create all permutations (total of 9 files). Make your command as short as possible. I can do it in 25 characters, can you do better?
```bash
touch {a..c}-{1..3}.txt
```

# Significado das Flags dos Comandos

- **tar -xzf**
  - `-x`: extrair arquivos do arquivo tar
  - `-z`: descompactar gzip
  - `-f`: especifica o arquivo a ser extraído

- **ls -l**
  - `-l`: lista detalhada, mostrando permissões, proprietário, tamanho e data

- **chmod +w**
  - `+w`: adiciona permissão de escrita

- **grep -rl**
  - `-r`: busca recursivamente em subdiretórios
  - `-l`: mostra apenas os nomes dos arquivos correspondentes

- **head -n 25**
  - `-n 25`: mostra as primeiras 25 linhas

- **tail -n 25**
  - `-n 25`: mostra as últimas 25 linhas
  - `-n +2`: inicia na segunda linha (pula a primeira)

- **cut -d',' -f2**
  - `-d','`: define o delimitador de campo
  - `-f2`: seleciona o segundo campo

- **sort**
  - Sem flags básicas, ordena linhas alfabeticamente

- **uniq**
  - Sem flags básicas, remove linhas duplicadas consecutivas

- **wc -l**
  - `-l`: conta linhas

- **sed 1d**
  - `1d`: deleta a primeira linha

- **time**
  - Mede o tempo de execução de um comando

- **grep -c**
  - `-c`: conta quantas linhas correspondem ao padrão

- **find . -type f**
  - `-type f`: encontra apenas arquivos

- **find . -type d**
  - `-type d`: encontra apenas diretórios

- **find . -name "*pattern*" -delete**
  - `-name`: busca pelo nome do arquivo
  - `-delete`: remove os arquivos encontrados

- **sed -i**
  - `-i`: edita arquivos no lugar

- **tr ',' '|'**
  - Sem flags; substitui todos os caracteres `,` por `|`

- **fdupes**
  - Sem flags; lista arquivos duplicados

- **install -D**
  - `-D`: cria o arquivo e todos os diretórios necessários

- **touch**
  - Sem flags; cria arquivos vazios