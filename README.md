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

chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d

cat > file2

anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d

### Display the content of the files
cat < file1
## OUTPUT
![Screenshot from 2024-03-21 11-15-24](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/cea7dfc3-5a9f-4a38-be27-a22208676110)

cat < file2
## OUTPUT
![Screenshot from 2024-02-19 21-05-10](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/550f7f0c-2484-4ce6-a47e-469496fb09a3)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-03-21 11-01-15](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/90c99ef3-d190-4a38-b6cd-36d93d2f5379)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-03-21 11-02-13](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/d287cf28-c84c-4e42-8cc4-29716228243a)
 
diff file1 file2
## OUTPUT
![Screenshot from 2024-03-21 11-00-34](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/2899a28c-4143-4cf4-82b6-64dfba2c982b)

#Filters

### Create the following files file11, file22 as follows:

cat > file11

Hello world
This is my world
^d

cat > file22

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d



cut -c1-3 file11
## OUTPUT
![Screenshot from 2024-03-21 11-06-15](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/8d0a20d6-afef-4df3-be5e-25cf5d3302e9)

cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-03-21 11-12-34](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/aa0400f3-46fa-4f54-8810-fb5475cf52ac)

cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-03-21 11-14-23](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/f61d3f72-c6a3-4aab-b5d0-efaa4798b075)

cat < newfile 

Hello world
hello world
^d
`
cat > newfile 
Hello world
hello world
  
grep hello newfile 
## OUTPUT
![Screenshot from 2024-03-21 11-17-01](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/ee67d368-e49d-4e08-a01a-62457593f131)


grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-29-02](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/ad6cbabb-d974-4846-9de5-4484494a945f)

cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-03-25 15-31-12](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/4e3980fc-6583-4aa8-8df4-0a286aee0524)


grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-03-25 15-34-55](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/aa7ee5e4-dd93-4f15-a694-aee87967ef28)

cat < newfile 

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d


cat > newfile

Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 
![Screenshot from 2024-03-25 15-42-31](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/fbeedb06-eac3-4338-86c5-b7b843288230)

egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-44-44](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/f701d161-b6f7-4112-8710-2e7617373892)


egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-46-50](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/0186abfb-0a58-4d34-9835-410e301b2448)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-47-47](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/6d1e5b61-e3a7-45c9-ac29-b761fe0b0b40)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-48-13](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/e0535242-db6d-4978-bb0d-db40d2bc8e50)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-48-54](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/26412468-f099-4e24-92eb-37510b52f064)


egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-49-27](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/e9d0fffc-4efe-4e91-ad66-78c809d32890)

egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-50-35](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/78fe72a2-477f-46e3-be0f-74a68b19fa20)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-03-25 15-50-55](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/a8016fc0-1f6b-4f44-a2b7-7a75626aea39)



cat > file23

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d



sed -n -e '3p' file23
## OUTPUT
![Screenshot from 2024-03-25 15-56-26](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/1fbfc54f-f690-4bcb-af28-0eb1449aeb7f)


sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-03-25 15-56-53](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/46c125a0-7a98-4b57-ad19-24f906489a5e)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2024-03-26 08-18-19](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/9d61c833-49db-48b3-84fb-2abd4c2d5fe7)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-03-26 08-18-50](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/399d5cbc-153b-41a6-8aa6-9ed84137e2cb)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-03-26 08-19-30](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/cbfcfcbc-91b8-4f3b-968d-8cfa1eceeca2)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-03-26 08-20-06](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/3b398720-d569-443e-9e2a-42d5909c8e2d)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2024-03-26 08-20-42](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/b1743a7c-d803-4ef7-81a3-238bd2369a98)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-03-26 08-21-31](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/4c153ca2-6200-4a8f-9ed9-814eda6cf70c)



seq 10 
## OUTPUT
![Screenshot from 2024-03-26 08-21-46](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/54f8d127-13a8-4be8-b927-350f520a22d1)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-03-26 08-22-19](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/22cad363-02c5-4af1-9a77-b2a7bb7e6334)



seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2024-03-26 08-23-20](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/73b9508a-edd9-4bc2-bc69-c81ebabce313)


seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-03-26 08-25-53](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/a049eaf8-3be2-4178-9aba-bb43fc297bd3)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-03-26 08-26-36](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/2172476a-9496-4731-8a00-4aa66e508025)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-03-26 08-27-32](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/ffbab54b-04a3-46cf-a14d-6e660027986c)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-03-26 08-30-39](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/645048fc-c5a0-40e6-9c36-f8515f3deae8)


sed -n '2,4{s/$/*/;p}' file23
![Screenshot from 2024-03-26 08-28-35](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/45ffde7f-6740-4d97-88ea-b2e83e08e8b5)

#Sorting File content
cat > file21

1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
sort file21
## OUTPUT
![Screenshot from 2024-03-26 08-03-11](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/f33f9328-2fbc-4968-8fd7-b3da7f8d63f2)


cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
 
uniq file22
## OUTPUT

![Screenshot from 2024-03-26 08-03-54](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/19427389-b301-4520-8239-c0efeb8796bb)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot from 2024-03-26 08-04-45](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/19451415-e898-4173-95da-c82bd6864fbb)

cat < urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
^d
 
cat > urllist.txt

www. yahoo. com
www. google. com
www. mrcet.... com
 
cat urllist.txt | tr -d ' '
 ## OUTPUT

![Screenshot from 2024-03-26 08-07-52](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/caf922b2-acc6-4bb8-ab40-b1cc091bd36c)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2024-03-26 08-08-54](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/de9360d7-95a0-4c23-8cf6-020aaf6880c9)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-03-26 08-11-45](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/4e0dfc45-bf13-459d-a185-06a5b7a0da98)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2024-03-26 08-13-35](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/1dffd79f-9c88-4f95-a9e3-b57fa18cb586)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/96813167-e0d6-46b2-90db-29f21b5a176a)

gzip backup.tar

![Screenshot from 2024-03-26 09-00-14](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/99679687-a045-4561-b634-362f69a5dc94)

ls .gz
## OUTPUT
 ![image](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/2d0a06b9-eac5-4668-b186-c3396ccaabb1)
 
# Shell Script

echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2024-03-26 09-02-10](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/b46aa069-3262-43d7-bd01-651d123778c9)

 
cat << stop > herecheck.txt

hello in this world
i cant stop
for this non stop movement
stop


cat herecheck.txt
## OUTPUT

![Screenshot from 2024-03-26 09-02-59](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/cab070f9-34aa-43c1-a38b-f5f9ee3abdf3)

cat < scriptest.sh 
bash
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
 

cat scriptest.sh 
bash
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

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![Screenshot from 2024-03-26 09-03-57](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/65ae614d-035b-4c79-a761-b99c26c90c6c)

 
ls file1
## OUTPUT
![Screenshot from 2024-03-26 09-04-43](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/1f5e2aa4-0f43-44b7-a109-cfc900fb0846)

echo $?
## OUTPUT 
![Screenshot from 2024-03-26 09-05-05](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/9105f4d1-c554-45f0-9bf0-1f37feeb0c57)

./one
bash: ./one: Permission denied
 
 
# mis-using string comparisons

cat < strcomp.sh 
bash
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


cat strcomp.sh 
bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi

##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2024-03-26 09-05-27](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/ff2cbc1f-6ee5-4f32-aee8-0e2de3dbfd00)

# check file ownership
cat < psswdperm.sh 
bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d


cat psswdperm.sh 
bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 
./psswdperm.sh
## OUTPUT
![Screenshot from 2024-03-26 09-05-43](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/debdb3bb-8a1c-43fc-a31a-f2868563b850)


# check if with file location
cat>ifnested.sh 
bash
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

cat ifnested.sh 

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


./ifnested.sh 
## OUTPUT

![Screenshot from 2024-03-26 09-07-45](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/81168090-3d8c-491f-98de-fcbf0c1b453c)


# using numeric test comparisons
cat > iftest.sh 
bash
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



cat iftest.sh 
bash
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


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
bash
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


cat ifnested.sh 
bash
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


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![Screenshot from 2024-03-26 09-08-38](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/80023581-a998-40c4-8f65-926441c27f41)


# looking for a possible value using elif
cat elifcheck.sh 
bash
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


$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
bash
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

$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done

$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done

$ ./forin3.sh 

 ![Screenshot from 2024-03-26 08-58-16](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/7a1e5794-16b8-455e-b8ef-5d4ffa66a97b)

cat forin1.sh 
bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done

$ chmod 755 forin1.sh

## OUTPUT

cat forinfile.sh 
bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done

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
![Screenshot from 2024-03-26 08-57-18](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/14084d0c-373d-4702-9c26-4b3c1fea7b35)


cat forctype.sh 
bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
`
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![Screenshot from 2024-03-26 08-56-24](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/56693acd-71aa-4947-b4e3-bb584fa8f5d3)

cat forctype1.sh 
bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done

$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![Screenshot from 2024-03-26 08-55-35](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/8899c703-62dd-4c51-aa84-ea21297d24a1)


cat fornested1.sh 
bash
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

$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![Screenshot from 2024-03-26 08-54-44](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/34d755eb-cd75-4ef2-8f7c-1cc2d6171e75)

 
cat forbreak.sh 
bash
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

## OUTPUT
![Screenshot from 2024-03-26 08-53-54](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/56576de7-bb31-482f-8367-6695f4492afd)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
bash
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


 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT

 
cat exread.sh 
bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![Screenshot from 2024-03-26 08-53-00](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/6af845d8-7abd-4511-86a7-7e3d502a29eb)


 cat exread1.sh
bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot from 2024-03-26 08-52-14](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/5f68dc6e-d782-4755-ae4d-2779817a8a49)


$ ./exread1.sh 
 
cat funcex.sh
bash
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

## OUTPUT
![Screenshot from 2024-03-26 08-51-30](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/595ee82c-49fd-46fe-8357-26901ec8e2ea)

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done

$ chmod 777 argshift.sh

## OUTPUT
![Screenshot from 2024-03-26 08-49-20](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/de17793b-6c93-4235-87aa-a09b2ff46662)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
bash
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

$ chmod 777 argshift.sh
## OUTPUT
![Screenshot from 2024-03-26 08-48-27](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/e74fbcc7-e92e-4774-bced-7b2fae5e3617)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x

## OUTPUT
![Screenshot from 2024-03-26 08-47-48](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/07bf82e6-0425-444a-a0ae-61d9c92d9a4e)

 ./argshift.sh 1 2 3
 
 
cat > nc.awk
bash
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
 
cat>data.dat
bash
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

awk -f nc.awk data.dat
## OUTPUT 
![Screenshot from 2024-03-26 08-46-57](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/ca198f8b-6ece-47ac-b236-bf8b4db1f2bb)

 
cat > palindrome.sh
bash
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

## OUTPUT 
![image](https://github.com/aswethaashok/OS-Linux-commands-Shell-script/assets/149987410/ad48f573-4392-4d47-8cb8-927e77bd8199)


# RESULT:
The Commands are executed successfully.
