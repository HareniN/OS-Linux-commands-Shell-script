# OS-Linux-commands-Shell-scripting
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

![Screenshot from 2025-04-23 20-59-19](https://github.com/user-attachments/assets/49dbc380-ca90-4ed8-afb7-3804f9bea459)


cat < file2
## OUTPUT
![Screenshot from 2025-04-23 20-59-42](https://github.com/user-attachments/assets/a9164a01-f8e0-4123-8fdb-a747c193ba7e)


# Comparing File
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-04-23 21-00-12](https://github.com/user-attachments/assets/f8ad4eab-50e0-440c-b19a-5521fe1681bb)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-04-23 21-01-19](https://github.com/user-attachments/assets/137a97cb-8d8d-44b9-a327-2d9cd8af491b)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-04-23 21-02-03](https://github.com/user-attachments/assets/11672fbe-83cb-4e93-890b-6f65f18f6e0d)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

![Screenshot from 2025-04-23 21-04-02](https://github.com/user-attachments/assets/90fa7f1d-f034-4082-8b92-8caf589e29fe)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-04-23 21-04-54](https://github.com/user-attachments/assets/0b1684a1-13ea-4826-a948-84c186b8c05f)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-04-23 21-05-22](https://github.com/user-attachments/assets/f62f475a-5ad3-48d6-b1d5-70775d402fd6)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-07-13](https://github.com/user-attachments/assets/1fc86cf8-c484-4835-84bf-21d533843f3b)


grep hello newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-07-31](https://github.com/user-attachments/assets/985d7df9-3e56-4de2-ae13-293d9f7a01ad)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-08-13](https://github.com/user-attachments/assets/a8e7117a-bdf0-435e-8b1c-ca48b907f8dd)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-04-23 21-08-58](https://github.com/user-attachments/assets/cc9543f5-d837-4a65-b817-053e4ff8980a)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-04-23 21-09-45](https://github.com/user-attachments/assets/9ea32bf9-d088-468b-807c-451ac9a415f9)



grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-04-23 21-13-37](https://github.com/user-attachments/assets/bb1004f8-3f8e-465d-81b9-1553b257684d)


grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-04-23 21-15-15](https://github.com/user-attachments/assets/5552422b-fd2b-4930-8c55-e6fbdaffdbe4)

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
egrep -w 'Hello|hello' newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-17-11](https://github.com/user-attachments/assets/860a440a-d83d-441a-9176-e44fd79a3a38)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![Screenshot from 2025-04-23 21-18-06](https://github.com/user-attachments/assets/bcfdf81b-5ef0-4ebe-b88d-17a93e3abd7c)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-18-56](https://github.com/user-attachments/assets/304ee08a-9112-458a-a9ae-e480daf9360b)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-19-45](https://github.com/user-attachments/assets/93c7fc3b-f7c1-45bb-8154-33105456d668)


egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-20-25](https://github.com/user-attachments/assets/4fdcfd4a-06e2-4320-bc86-1ac393956996)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-20-47](https://github.com/user-attachments/assets/e00a9400-5066-4420-a45f-f6ba759ae5c7)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-21-31](https://github.com/user-attachments/assets/44eb0107-1a6b-41f2-9bbc-67058328f461)




egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-04-23 21-23-46](https://github.com/user-attachments/assets/245002b3-2360-42e6-9168-4080cd54e2c5)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-24-26](https://github.com/user-attachments/assets/68942ca3-f086-4230-b6e6-5843db478cc9)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-04-23 21-24-50](https://github.com/user-attachments/assets/3ad486dd-71d1-4d00-b322-2790a2fb171f)


egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-04-23 21-25-38](https://github.com/user-attachments/assets/90e110ae-cdbd-4b55-a46d-05f23859441d)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-23 21-26-17](https://github.com/user-attachments/assets/2c37355c-65e2-4258-b06a-63b5c32e3d03)


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


sed -n -e '3p' file23
## OUTPUT

![Screenshot from 2025-04-23 21-40-16](https://github.com/user-attachments/assets/1bcec11f-3e45-4410-97c1-a308518134e2)


sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-04-23 21-40-42](https://github.com/user-attachments/assets/66695d0b-1716-463f-9706-4af66482ff51)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-23 21-41-30](https://github.com/user-attachments/assets/39be5eaf-8daf-4a47-9db0-a4d9e5497422)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-04-23 21-41-52](https://github.com/user-attachments/assets/e19bbcdf-1bbc-4fdd-ac82-dc799a775210)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-04-23 21-42-32](https://github.com/user-attachments/assets/080ad526-4f46-4e11-8754-bbc5d0786e22)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-04-23 21-43-22](https://github.com/user-attachments/assets/ef6ff763-7116-4efc-90ed-8f6ed6e08065)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-23 21-43-57](https://github.com/user-attachments/assets/ae48533f-ad12-4255-9afb-a62420b5851a)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT

![Screenshot from 2025-04-23 21-45-23](https://github.com/user-attachments/assets/35c29b25-5a1f-431f-bb52-4accc3d16a66)


seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-04-23 21-46-24](https://github.com/user-attachments/assets/c5240fa7-4dc4-4ba0-ab6f-ba75951c1df9)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-04-23 21-47-55](https://github.com/user-attachments/assets/e5540581-4b85-4109-8048-5de8ff22f670)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-04-23 21-48-27](https://github.com/user-attachments/assets/e511c4a5-1410-4750-b6e2-a2f36a3af524)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-23 21-48-27 (copy)](https://github.com/user-attachments/assets/469b3704-88fb-49c0-8d27-601117cebff0)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-04-23 21-48-54](https://github.com/user-attachments/assets/3d7fbcd6-c0f7-464b-8fac-cfbb3e86d7f3)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-04-23 21-49-54](https://github.com/user-attachments/assets/7d7e7bf8-adbe-43d8-9b38-2dc609b3856c)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot from 2025-04-23 21-51-00](https://github.com/user-attachments/assets/3214f0a2-6809-4447-a039-18168277bd43)


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
![Screenshot from 2025-04-23 21-52-48](https://github.com/user-attachments/assets/f0474668-3152-497e-884e-ba9aa1f71719)



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
![Screenshot from 2025-04-23 21-53-29](https://github.com/user-attachments/assets/5d9e8da3-c284-45ab-90a9-53e47c4f3dca)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-04-23 21-54-09](https://github.com/user-attachments/assets/2eabf8bd-3583-4d71-8593-d730e2a43d37)

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
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2025-04-23 21-56-23](https://github.com/user-attachments/assets/663eca10-9491-4345-9281-50610e64cee6)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-04-23 21-56-56](https://github.com/user-attachments/assets/7f2582c6-c1e8-4f61-b898-1deae52a4899)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-04-23 22-16-23](https://github.com/user-attachments/assets/4e4f81fc-2e26-4092-ac7f-790a14b86c7e)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-04-23 22-19-17](https://github.com/user-attachments/assets/1b1b3b6f-c0c9-4ecf-9217-2fdb0ed75872)



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
![Screenshot from 2025-04-23 22-21-44](https://github.com/user-attachments/assets/0d472d17-0395-4444-9994-cc9f82fb09b6)

 
ls file1
## OUTPUT
![Screenshot from 2025-04-23 22-22-02](https://github.com/user-attachments/assets/91767aca-a8f1-4999-9e90-9a0060ef29fd)

echo $?
## OUTPUT 
![Screenshot from 2025-04-23 22-22-22](https://github.com/user-attachments/assets/2d4d07ba-a386-43d0-bc64-3e0aa4c557d4)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2025-04-23 22-27-53](https://github.com/user-attachments/assets/458bac92-c290-40f2-bd38-9fdf3ba97675)

 
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
![Screenshot from 2025-04-23 22-40-14](https://github.com/user-attachments/assets/61d32e9d-80a9-488b-8173-43d5bedc8654)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2025-04-23 22-41-13](https://github.com/user-attachments/assets/d83677b6-aa0a-4055-938e-3bc36d6001b7)



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
![Screenshot from 2025-04-23 22-43-04](https://github.com/user-attachments/assets/2107ddec-c71f-4763-bd1e-c94422fad733)

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

![Screenshot from 2025-04-23 22-44-07](https://github.com/user-attachments/assets/714e1d38-4e8f-4ebb-9903-66ec3264c272)


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

![Screenshot from 2025-04-23 22-46-07](https://github.com/user-attachments/assets/9605ac11-313e-4896-9599-5ffa1c333bab)

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
![Screenshot from 2025-04-23 22-47-26](https://github.com/user-attachments/assets/d57a9e25-5f35-465e-aa37-4aec97ecbde3)

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
![Screenshot from 2025-04-23 22-50-15](https://github.com/user-attachments/assets/4b3b42c8-e695-477e-9d69-82855d7be54c)


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
## OUTPUT
![Screenshot from 2025-04-23 22-53-30](https://github.com/user-attachments/assets/6c2ebd2a-4356-4a21-b193-1aaaeba6f151)

 
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
./untiltest.sh
## OUTPUT
![Screenshot from 2025-04-23 22-55-34](https://github.com/user-attachments/assets/9397819d-52c4-4c94-8fe8-e0bbd62a1ae1)

 
 
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
./forin1.sh
## OUTPUT 
![Screenshot from 2025-04-23 22-56-54](https://github.com/user-attachments/assets/5acbb6f6-4ec5-43a9-b89b-ff1783d2da72)

 
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
## OUTPUT
![Screenshot from 2025-04-23 22-58-25](https://github.com/user-attachments/assets/be023ebf-1cec-4635-ba80-a70d46fb13bf)

 
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
## OUTPUT 
![Screenshot from 2025-04-23 23-00-30](https://github.com/user-attachments/assets/abc75d43-09a3-477f-88ee-6d861b736a96)

 
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
./forin1.sh

## OUTPUT
![Screenshot from 2025-04-23 23-02-02](https://github.com/user-attachments/assets/3673e89e-3261-4623-8ca2-dec68078a56a)


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
![Screenshot from 2025-04-23 23-06-00](https://github.com/user-attachments/assets/654ed7b4-033f-4ed5-ac88-6e4fc425f346)


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
![Screenshot from 2025-04-23 23-07-31](https://github.com/user-attachments/assets/c796cbba-5bc1-460a-88e8-b3515c731735)

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
![Screenshot from 2025-04-23 23-08-18](https://github.com/user-attachments/assets/992404ed-170d-4045-baed-c33b712ab85e)

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

 ![Screenshot from 2025-04-23 23-09-43](https://github.com/user-attachments/assets/a37b0e6c-6c75-4733-be19-b2c2fa7e4606)

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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
![Screenshot from 2025-04-23 23-11-15](https://github.com/user-attachments/assets/99b110ca-539d-4259-999e-84d0f65e77c1)


 
cat forcontinue.sh 
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
 ![Screenshot from 2025-04-23 23-12-54](https://github.com/user-attachments/assets/29f7d5aa-65e1-4b49-a583-475e55571317)

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
![Screenshot from 2025-04-23 23-14-10](https://github.com/user-attachments/assets/b5c72e7c-b86e-4bbe-992f-6ee446a6680c)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

## OUTPUT

![Screenshot from 2025-04-23 23-15-55](https://github.com/user-attachments/assets/5298d076-46ac-4046-82e6-e71b024c2362)


 
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
![Screenshot from 2025-04-23 23-18-52](https://github.com/user-attachments/assets/392a499e-fc16-4628-bc17-b0891c195709)

 
 ./funcex.sh 1 2

 ![Screenshot from 2025-04-23 23-19-21](https://github.com/user-attachments/assets/a841ae01-6b61-46fa-a56e-5fa21c2d0892)

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
$ ./argshift.sh
![Screenshot from 2025-04-23 23-21-06](https://github.com/user-attachments/assets/76ab402d-ff8e-440c-9009-0a5873ec800a)
 1 2 3
 
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
 ![Screenshot from 2025-04-23 23-22-05](https://github.com/user-attachments/assets/fcd06c04-769e-4ca8-bd35-2e5fff29d314)

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
 ![Screenshot from 2025-04-23 23-24-18](https://github.com/user-attachments/assets/c3433932-0c87-419d-bd6f-735d40de335b)

 
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
 ![Screenshot from 2025-04-23 23-26-07](https://github.com/user-attachments/assets/ff5b7e83-f096-4c1d-a6f0-acb0b13bf85a)

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
![Screenshot from 2025-04-23 23-27-12](https://github.com/user-attachments/assets/30fb99ec-8fa4-430d-a221-9588dcaf6e2a)



# RESULT:
The Commands are executed successfully.
