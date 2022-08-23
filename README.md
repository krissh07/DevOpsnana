# DevOpsnana
#!/bin/bash
#Assign the first argument from the command line to the variable
Input_Number=$1

if [ $Input_Number -eq 1 ]
then
echo "$Input_Number is neither prime nor composite number"
exit 0;
fi

Num_Factors=`factor $Input_Number|wc -w`
echo $Num_Factors

if [ $Num_Factors -eq 2 ]
then
echo "$Input_Number is a prime number"
else
echo "$Input_Number is not a prime number"
fi