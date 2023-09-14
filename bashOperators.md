# 20 BASH SCRIPT OPERATORS AND THEIR USAGE

## 1)** Integer Operator
‘**’ operator is used to calculate the xy. ‘**’ is used to print the value of 53 in the following command.

$ echo $((5 ** 3)) 125

## 2)/ Integer Operator
‘/’ is an arithmetic operator to divide two numeric values in bash. The following commands show the division of two integer numbers by using `let` command.

$ let n=30/6 <br>
$ echo $n 5

## 3) ++ (Pre) Increment Operator
‘++` operator is used to increment the value of a variable by 1. When the operator is used before the variable then it will act as a pre-increment operator that means the value of the variable will be incremented first and will do other operation later. The value of $i will be incremented before adding with the number 10 in the following example.

$ i=39 <br>
$  echo $((++i+10)) 50

## 4) %Integer Operator
‘%’ operator is used to calculate the remainder of the division of two numbers. The remainder value of 89/5 will be printed after executing the following command.

$ echo `expr 89 % 5` 4

## 5) (Post) ++ Increment Operator
When ‘++’ operator is used after the variable then it will act as post-increment operator and it increments the value of the variable by 1 after doing another task. In this example, the current value of $i will be printed first and incremented by 1 in the second command that is 10. The last command will print the value of $i , which is 11.$ i=10

$ i=10 <br>
$ echo $((i++)) <br>
$ echo $i 

## 6) – – (Pre) Decrement Operator
‘–` operator is used to decrement the value of a variable by 1. When the operator is used before the variable then it will act as a pre-decrement operator that means the value of the variable will be decremented first and the other operation will be done later. The value of $i will be decremented before adding with the number 15 in the following example.

$ i=36 <br>
$ echo $((--i+15)) 50

## 7) && Logical Operator
‘&&’ is a comparison operator that is used for creating Boolean AND logic. When all conditions are true the then AND logic return true. Two conditions are checked by using ‘&&’ operator in the following example.

if [[ $1 = "fahmida" && $2 = "abcd" ]] <br>
then <br>
  echo "Valid user" <br>
else <br>
  echo "Invalid user" <br>
fi

## 8) || Logical Operator
‘||’ operator is used to create two or more conditions with OR logic which returns true when any one of the condition returns true. The following script shows the use of this operator.

if [[ $1 = 101 || $1 = 780 ]] <br>
then <br>
  echo "You have won the ticket" <br>
else <br>
  echo "Try again" <br>
fi

## 9) & Bitwise Operator
‘&’ operator is used to perform bitwise AND operation that works on binary data.  The following command shows the use of this operator.

$ echo $((3 & 6)) 2

## 10) -eq Integer operator
‘-eq’ operator is used to check two values are equal or not. If the values are equal then it returns true otherwise returns false.

n=50 <br>
if [ $n -eq 80 ] <br>
then <br>
  echo "The number is equal to 80" <br>
else <br>
  echo "The number is not equal to 80" <br>
fi

## 11) -ne Integer operator
‘-ne’ operator is used to check two numbers are not equal or equal. If the values are not equal then it returns true otherwise returns false.

n=50 <br>
if [ $n -ne 100 ] <br>
then <br>
  echo "The number is not equal to 100" <br>
else <br>
  echo "The number is equal to 100" <br>
fi

## 12) -gt Integer operator
‘-gt’ operator is used to compare two numbers and it returns true if any number is greater than the other number. The following script shows the use of this operator.

n=50 <br>
if [ $n -gt 50 ] <br>
then <br>
  echo "The number is greater than 50 " <br>
else <br>
  echo "The number is less than or equal to 50" <br>
fi

## 13) -ge Integer operator
‘-ge’ operator is used to compare two numbers and it returns true if any number is greater than or equal to the other number. The following script shows the use of this operator.

n=50 <br>
if [ $n -ge 50 ] <br>
then <br>
  echo "The number is greater than or equal to 50" <br>
else <br>
  echo "The number is less than 50" <br>
fi

## 14) -lt Integer operator
‘-lt’ operator is used to compare two numbers and it returns true if any number is less than the other number. The following script shows the use of this operator.

n=50 <br>
if [ $n -lt 50 ] <br>
then <br>
  echo "The number is less than 50" <br>
else <br>
  echo "The number is greater than or equal to 50" <br>
fi

## 15) -le Integer operator
‘-le’ operator is used to compare two numbers and it returns true if any number is less than or equal to the other number. The following script shows the use of this operator.

n=50 <br>
if [ $n -le 50 ] <br>
then <br>
  echo "The number is less than or equal to 50" <br>
else <br>
  echo "The number is greater than 50" <br>
fi

## 16) -f file operator
‘-f’ operator is used to check any file exists or not. The following script shows the use of this operator.

if [ -f "test.txt" ] <br>
then <br>
  echo "File exists." <br>
else <br>
  echo "File does not exist." <br>
fi <br> 

## 17) -e file operator
'-e' test operator is used to check any file or folder is exists or not. Create a bash file with the following script to check any file exists or not. Here, the filename will provide as command-line argument in the script.

filename=$1 <br>
if [ -e $filename ] <br>
then <br>
  echo "File or Folder exists." <br>
else <br>
  echo "File or Folder does not exist." <br>
fi

## 18) -a logical operator
‘-a’ operator is used to create Boolean AND logic within two or more conditions. The following script shows the use of this operator.

n1=25 <br>
n2=65 <br>
if [ $n1 -gt 24 -a $n2 -lt 66 ] <br>
then <br>
  echo "You are eligible" <br>
else <br>
  echo "You are not eligible" <br>
fi

## 19) -z string operator
‘-z’ operator is used to check the length of a string is zero or not. The following script shows the use of this operator.


str="" <br>
if [ -z $str ] <br>
then <br>
  echo "The string length is zero" <br>
else <br>
  echo "The string length is more than zero" <br>
fi

## 20) -s file operator
‘-s’ operator is used to check the file size is more than zero or not. The following script shows the use of this operator.

filename=$1 <br>
if [ -s $filename ] <br> 
then <br>
  echo "File size is more than zero." <br>
else <br>
  echo "File size is zero." <br>
fi
