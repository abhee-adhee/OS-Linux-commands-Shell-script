Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="288" height="147" alt="image" src="https://github.com/user-attachments/assets/425656a2-2105-4496-a9ed-63ee01d6586d" />



cat < file2
## OUTPUT

<img width="304" height="180" alt="image" src="https://github.com/user-attachments/assets/325bcf50-4658-4ce7-b89e-38d0feef9dab" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="359" height="73" alt="image" src="https://github.com/user-attachments/assets/65f984c5-bed1-49f0-93af-b8fbe7dd9002" />

comm file1 file2
 ## OUTPUT
<img width="405" height="229" alt="image" src="https://github.com/user-attachments/assets/7f9eeeec-8e69-444b-a645-ffd1eec2ad2e" />

 
diff file1 file2
## OUTPUT
<img width="264" height="276" alt="image" src="https://github.com/user-attachments/assets/b43d7824-f982-403a-9e24-1b5c91b9c4fd" />

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="315" height="100" alt="image" src="https://github.com/user-attachments/assets/a4a290fa-28ac-4653-ac12-77aab58957a5" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="434" height="127" alt="image" src="https://github.com/user-attachments/assets/3ce8d6ae-3efd-40d4-b7e3-ff603ce99f74" />


cut -c1-3 file11
## OUTPUT




cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT
<img width="364" height="101" alt="image" src="https://github.com/user-attachments/assets/30492741-8376-46a6-b224-14ca0f0fa118" />


cat < newfile 
```
Hello world
hello world
^d
````
<img width="310" height="101" alt="image" src="https://github.com/user-attachments/assets/16f418eb-7d71-4956-bad1-869977a725ce" />

cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="398" height="82" alt="image" src="https://github.com/user-attachments/assets/e3f89789-d37c-499a-9744-7532ccba527a" />


grep hello newfile 
## OUTPUT

<img width="320" height="79" alt="image" src="https://github.com/user-attachments/assets/09cb4636-7d32-403e-a331-051fb33bcb3b" />



grep -v hello newfile 
## OUTPUT

<img width="320" height="84" alt="image" src="https://github.com/user-attachments/assets/aac7049b-4078-4c91-b693-9ec17e0d0ced" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="420" height="110" alt="image" src="https://github.com/user-attachments/assets/45a6e3cf-4c56-4a1f-b049-15320fa974fa" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="410" height="89" alt="image" src="https://github.com/user-attachments/assets/d62920e3-94b2-4863-a554-93ed62b6198f" />


grep -R ubuntu /etc
## OUTPUT

<img width="1368" height="550" alt="image" src="https://github.com/user-attachments/assets/c0d442cb-66a3-41a9-8b2a-46a951cb59c4" />

grep -w -n world newfile   
## OUTPUT

<img width="393" height="110" alt="image" src="https://github.com/user-attachments/assets/6a63a60f-cac0-491c-a7fd-22d259d5757b" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
<img width="326" height="150" alt="image" src="https://github.com/user-attachments/assets/f5d18062-6538-4f14-ab15-06eabf5f30ff" />

egrep -w 'Hello|hello' newfile 
## OUTPUT


<img width="465" height="109" alt="image" src="https://github.com/user-attachments/assets/057e80f5-8916-4578-905a-0aacf50d31cb" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="387" height="86" alt="image" src="https://github.com/user-attachments/assets/d0402c83-6cab-4dbd-9b37-287c228cf2d0" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="537" height="98" alt="image" src="https://github.com/user-attachments/assets/6518b312-7707-4592-98c1-0b2c8084d90e" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="430" height="78" alt="image" src="https://github.com/user-attachments/assets/e144c079-aca6-4194-ade0-0a2048e39e2f" />


egrep '(world$)' newfile 
## OUTPUT

<img width="391" height="97" alt="image" src="https://github.com/user-attachments/assets/322a76c2-06e4-4e04-a727-ba7437403f47" />


egrep '(World$)' newfile 
## OUTPUT

<img width="379" height="77" alt="image" src="https://github.com/user-attachments/assets/060c8b7d-eaf6-46b9-bab9-09878640df61" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="478" height="124" alt="image" src="https://github.com/user-attachments/assets/eb93be2b-57a5-4d61-a05d-d5f21ded2a08" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="391" height="79" alt="image" src="https://github.com/user-attachments/assets/8266257f-ba3e-4261-993d-b1d5d403f4a4" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="417" height="76" alt="image" src="https://github.com/user-attachments/assets/ea178dba-aaf7-4728-b73a-c65fb2bac34c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="471" height="70" alt="image" src="https://github.com/user-attachments/assets/2964236b-0712-44c2-ad1b-2c031275726e" />


egrep l{2} newfile
## OUTPUT
<img width="459" height="108" alt="image" src="https://github.com/user-attachments/assets/b27742c3-8a18-41cf-a7e7-a4e3a8dbc23c" />



egrep 's{1,2}' newfile
## OUTPUT 
cat<img width="423" height="81" alt="image" src="https://github.com/user-attachments/assets/e4a1035c-764e-44ef-87dc-a31479a6b2a9" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```
<img width="370" height="257" alt="image" src="https://github.com/user-attachments/assets/734c2c92-9e14-4df7-979c-2efc5979b5bc" />


sed -n -e '3p' file23
## OUTPUT


<img width="331" height="83" alt="image" src="https://github.com/user-attachments/assets/1d3236a2-60c0-4564-970c-a780319f1224" />


sed -n -e '$p' file23
## OUTPUT

<img width="331" height="74" alt="image" src="https://github.com/user-attachments/assets/5edeb4d7-65b9-4084-ad37-a884e31e4008" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="463" height="256" alt="image" src="https://github.com/user-attachments/assets/3c1e37a1-611d-4589-9eb8-cf192e5748f9" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="432" height="253" alt="image" src="https://github.com/user-attachments/assets/bff1fb32-dd63-45eb-a6e0-20a43c251d68" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="478" height="251" alt="image" src="https://github.com/user-attachments/assets/d8d8fce9-8950-4a9e-a22c-dac67decef55" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="371" height="170" alt="image" src="https://github.com/user-attachments/assets/571f0198-7dde-4716-b66b-1dd751888592" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="410" height="122" alt="image" src="https://github.com/user-attachments/assets/5e2e19bd-2481-4838-b11f-017dea36fef1" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="410" height="103" alt="image" src="https://github.com/user-attachments/assets/71092390-ea23-4afc-8a7d-dd8a607ac9e6" />


seq 10 
## OUTPUT

<img width="443" height="296" alt="image" src="https://github.com/user-attachments/assets/929cccba-0a2c-481a-a5ab-364204c5bba6" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="365" height="120" alt="image" src="https://github.com/user-attachments/assets/e7f55ead-a22b-4178-a25c-1718e0e72796" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="399" height="134" alt="image" src="https://github.com/user-attachments/assets/b894ae86-7fad-4c0c-a5b7-c82bbb3f71ae" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="353" height="81" alt="image" src="https://github.com/user-attachments/assets/5f46fd5f-5f83-4c46-9e4c-408b936e1d71" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="352" height="132" alt="image" src="https://github.com/user-attachments/assets/f10ea581-be0b-45ec-be90-dce6a97ab358" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="431" height="123" alt="image" src="https://github.com/user-attachments/assets/a6c82ce3-95e7-416e-a24e-e4b9c7074f02" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="454" height="136" alt="image" src="https://github.com/user-attachments/assets/52118fac-e3d4-4c80-b8a1-93d04d8d4735" />


sed -n '2,4{s/$/*/;p}' file23
<img width="422" height="126" alt="image" src="https://github.com/user-attachments/assets/e5e20964-635a-4173-ad31-6ca0bd08d9a8" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="452" height="172" alt="image" src="https://github.com/user-attachments/assets/f17717fb-f455-48c1-9869-e3f53e70a150" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="405" height="176" alt="image" src="https://github.com/user-attachments/assets/bf97fd14-f585-44a0-84b8-a85f25f73370" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="452" height="245" alt="image" src="https://github.com/user-attachments/assets/a8e11966-a8db-47ec-9a2b-fbb5c4c2cf86" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urlist.txt | tr -d ' '
 ## OUTPUT

<img width="426" height="124" alt="image" src="https://github.com/user-attachments/assets/af1e210b-288d-4d93-b35e-f9a263f554e8" />

 
cat urlist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="509" height="130" alt="image" src="https://github.com/user-attachments/assets/f8cfbe67-77d1-4216-b4d2-8805a3d6e14f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="615" height="682" alt="image" src="https://github.com/user-attachments/assets/b1657bd5-e131-49c4-a0c7-2769971d8fca" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1072" height="636" alt="image" src="https://github.com/user-attachments/assets/05aac75b-4e49-4d46-bc22-b93337f7f770" />

tar -xvf backup.tar
## OUTPUT
<img width="523" height="629" alt="image" src="https://github.com/user-attachments/assets/bf85011e-675a-45e1-9b27-a393bcb0e2c0" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="456" height="81" alt="image" src="https://github.com/user-attachments/assets/6b20c69c-37be-4839-be48-58e7d153f406" />

gunzip backup.tar.gz
## OUTPUT
<img width="415" height="45" alt="image" src="https://github.com/user-attachments/assets/edb930bb-2994-4028-b4d6-8c0f6f0d982a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
