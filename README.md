PRINT PATTERN  13*14*15*16  9*10*11*12
For any input number N Print the following code – For below code N=4

13*14*15*16
9*10*11*12
5*6*7*8
1*2*3*4
PREREQUISITE:
Basic knowledge in Java programming, usage of loops.

ALGORITHM:
Take input from user i.e number of lines required (N value).
Take two loops one for each line (say ‘i’) and other for each digit in a particular line (say ‘j’). i starts from n and j starts from 1.
Take a result variable (say ‘a’) and initialize it with (i*(i-1))+1, Since each line starts with 13,9,5,1.
Here ‘i’ loop is used to access each line from N to 1 and ‘j’ loop is used to print values in each line. For example in line 2 the value of i=3 and for contents in second line (i.e 9*10*11*12) the value for j for digit 9 is j=1 and for digit 10 is j=2.
Print ‘a’ value along with * and post decrement  until the j loop reaches a value less than n.
Print the final value ‘a’ of each line.
Repeat the ‘i’ loop until it reaches 1.
CODE IN JAVA:
import java.lang.*;
import java.io.*;
class Main
{
    public static void main (String[]args) throws IOException
    {
        BufferedReader br =new BufferedReader (new InputStreamReader (System.in));
        int n, i, j, a;
        System.out.print ("Enter N value:");
        n = Integer.parseInt (br.readLine ());
    
        for (i = n; i >= 1; i--)
        {
	        a = (i * (i - 1)) + 1;
	        for (j = 1; j < n; j++)
	        {
	            System.out.print ((a++) + "*");
	        }
	        System.out.println (a++);
        }
    }
}
 

TAKING INPUT:


DISPLAYING OUTPUT:
