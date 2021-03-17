By Gabriela Joselyn Canche Diaz 
# Functions-1

## F1-1 INVERTED STRING

//create a function that receives a string and print the inverted string, remember that to print an element i you can use printf("%c",string[i]); 
#include <stdio.h>
#include <string.h>

void INVERT(char x[])
{
  char inv[30];
  int i, ll,c;
  c=0;

 ll=strlen(x);
 for(i=ll-1;i>=0;i--)
  {
    inv[c]=x[i];
    c=c+1;
  }
  printf("%s",inv);
}

int main() {

 fgets(S,30,stdin);
 INVERT(S);

 return 0;
}

## F1-2 SAME LENGHT OR NOT

// create a function that returns 0 if both have the same length and 1 if is different.
#include <stdio.h>
#include<string.h>

int SAMEORNOT(char x[], char y[])
{
  int i, N1, N2;
  N1=strlen(x); 
  N2=strlen(y);
  if(N1==N2)
  i=0;
  else
  i=1;

 return i;
}

int main() {
  char W[30], w[30];
  int s;
  printf("INSERT WORD 1\n");
  fgets(W,30,stdin);
  printf("\nINSERT WORD 2\n");
  fgets(w,30,stdin);
  s=SAMEORNOT(W,w);
  printf("\n  SI ES 1 Ó 0\nDIFERENTE LONGITUD: 1\nIGUAL LONGITUD:     0\n");
  printf("\nLAS PALABRAS TIENEN %i",s);
  return 0;
}
## F1-3 SAME STRINGS OR NOT AND WHICH

// create a function that returns 0 if both strings have the same elements, and when there's a different element. returns the first different char... an example: "var1X" and "var1Y", returns "X"
#include <stdio.h>
#include <string.h>
#define MAX 30

char S1[MAX], S2[MAX];

int sameornotelements(char x[MAX],char y[MAX]);
{
int nx, ny, sone;

nx=strlen(x);
ny=strlen(y);

if(nx==ny)
sone=0;
else
{
sone=1;
printf("DO NOT HAVE THE SAME LENGHT");
}
}

void differentchar(char x[MAX], char y[MAX])
{
  int determin, str, i, breakk, aversisi;
  str=strlen(x);
  determin=sameornotelements(x,y);
  if(determin==0)
  {
    for(i=0;i<=str;i++)
    {
aversisi=0;
      if(x[i]!=y[i])
      {
        breakk=i;
        aversisi=1;
         printf("THIS IS THE FIRST DIFFERENT ELEMENT: %c",x[breakk]);
        break;
      }
    }
    if(aversisi==0)
    printf("0");
  }
}

int main()
 {
 printf("INSERT FIRST STRING\n");
 fgets(S1,MAX,stdin);

 printf("INSERT SECOND STRING\n");
 fgets(S2,MAX,stdin);
 differentchar(S1,S2);
 return 0;
 }

## F1-4 PALINDROMIC OR NOT

//create a function where you insert a string and return 1 if is palindromic or not, it means that returns 1 if is palindrome ("ala"), return 0 if is not ("hello")
#include <stdio.h>
#include <string.h>
#define MAX 30


int INVERT(char x[MAX])
{
  int mylen, i, ol;
  ol=0;
  mylen = strlen(x)-1;
for(i=mylen-1;i>=0;i--)
  {

    if(x[i]!=x[mylen-i-1])
    {
    ol=ol+1;
     break;
    }
    else 
    {
    ol=ol+0;
    }
  }
  return ol;
}

int main() {

int resultado;

fgets(S,MAX,stdin);
resultado=INVERT(S);
if(resultado!=0)
{
  printf("0 NO ES PALINDROMO");
}
else
  printf("1 SI ES PALINDROMO");
return 0;
}

## F1-5 PRINT ONLY CONSONANTS
 
// create a function where you enter a string of 30 chars and print only the consonants
#include <stdio.h>
#include <string.h>
#define MAX 30

char S[MAX];

void novoca(char x[MAX])
{
  int i, maxi;
maxi=strlen(x);
  for(i=0;i<=maxi;i++)
  {
    if(x[i]=='a'||x[i]=='e'||x[i]=='i'||x[i]=='o'||x[i]=='u'||x[i]=='A'||x[i]=='E'||x[i]=='I'||x[i]=='O'||x[i]=='U')
    printf("");
    else
    printf("%c",x[i]);
  }
}

int main() {
  printf("ENTER THE STRING\n");
  fgets(S,MAX,stdin);
  novoca(S);
  return 0;
}

# FUNCTIONS 2

## EX01 
def MAX2(x,y):
  if x > y:
    return x
  else:
    return y

def MAX3(x,y,z):
  return MAX2(x, MAX2(y,z))

print(MAX3(10,2,6))

## EX01.C
#include <stdio.h>
//MAX OF 3 NUMBERS USING FUNCTIONS
int N1,N2,N3,max2,max3;

int MAX2(x,y)
{
  if(x>y)
  max2=x;
  else
  max2=y;
  return max2;
}

int MAX3(x,y,z)
{
max3=MAX2(x,MAX2(y,z));
return max3;
}

int main() {
  printf("INTRODUCE TUS 3 NUMEROS\n");
  scanf("%i %i %i", &N1, &N2, &N3);
  printf("\n%i",MAX3(N1,N2,N3));
  return 0;
}

def MAX2(x,y):
  if x > y:
    return x
  else:
    return y

def MAX3(x,y,z):
  return MAX2(x, MAX2(y,z))

print(MAX3(10,2,6))

## EX01.C
#include <stdio.h>
//MAX OF 3 NUMBERS USING FUNCTIONS
int N1,N2,N3,max2,max3;

int MAX2(x,y)
{
  if(x>y)
  max2=x;
  else
  max2=y;
  return max2;
}

int MAX3(x,y,z)
{
max3=MAX2(x,MAX2(y,z));
return max3;
}

int main() {
  printf("INTRODUCE TUS 3 NUMEROS\n");
  scanf("%i %i %i", &N1, &N2, &N3);
  printf("\n%i",MAX3(N1,N2,N3));
  return 0;
}


## EX02
#Write a Python function to sum all the numbers in a list. 
#Sample List : (8, 2, 3, 0, 7)
#Expected Output : 20

def SUMA(numbers):
  sum=0
  for x in numbers:
    sum+=x
  return sum

print(SUMA((8, 2, 3, 0, 7)))

## EX02.C
#include <stdio.h>

int SUMA(int x)
{
  int SUM;
  SUM=0;
  SUM=SUM+x;
  return SUM;
}

int main() {
  printf("%i", SUMA(7));
  return 0;
}


## EX03
#Write a Python function to multiply all the numbers in a list. Go to the editor
#Sample List : (8, 2, 3, -1, 7)
#Expected Output : -336 

def mult(numbers):
  multi=1
  for x in numbers:
    multi*=x
  return multi

print(mult((8, 2, 3, -1, 7)))
## EX03.C
#include <stdio.h>

int MULT(int x)
{
  int M;
  M=1;
  M=M*x;
  return M;
}

int main() {
  printf("%i", MULT(7));
  return 0;

}


## EX04
#3Write a Python program to reverse a string. Go to the editor
#Sample String : "1234abcd"
#Expected Output : "dcba4321"

def inve(string):
    w=''
    i=0
    x=len(string)
    for i in string:
        w += string[ x - 1 ]
        x = x-1
    return w
print(inve('olmar'))

def string_reverse(str1):

    rstr1 = ''
    index = len(str1)
    while index > 0:
        rstr1 += str1[ index - 1 ]
        index = index - 1
    return rstr1
print(string_reverse('1234abcd'))

## EX04.C
#include <stdio.h>
#include <string.h>



void INVERT(char x[])
{
  char inv[30];
  int i, ll,c;
  c=0;

  ll=strlen(x);
  for(i=ll-1;i>=0;i--)
  {
    inv[c]=x[i];
    c=c+1;
  }
  printf("%s",inv);
}

int main() {

  fgets(S,30,stdin);
  INVERT(S);

  return 0;
}


## EX05
#Write a Python function to calculate the 
#factorial of a number (a non-negative integer).
#The function accepts the number as an 
#argument.

def fac(n):
    if n == 0:
        return 1
    else:
        return n * fac(n-1)
n=int(input("Input a number to compute the factiorial : "))
print(fac(n))
## EX05.C
#include <stdio.h>

int fac(int x)
{
  int i, f;
  f=1;
  for(i=1;i<=x;i++)
    f=f*i;

return f;
}

int main() {
  int N;
  printf("INTRODUCE N\n");
  scanf("%i",&N);
  printf("\n%i",fac(N));
  return 0;
}
NUMBER WITHIN OR OUT OF A RANGE


## EX06
#Write a Python function to check whether
#a number is in a given range


def wrange(n):
    if n>=l and n<=h:
        return print("WITHIN THE RANGE")
    else:
        return print("OUT OF THE RANGE")

l=int(input("low limit  : "))
h=int(input("high limit : "))
n=int(input("Number to know if is within the range: "))
print(wrange(n))

## EX06.C
#include <stdio.h>
//PROGRAMM TO KNOW IF A NUMBER IS WITHIN A RANGE
int l,h,n;

void range(int x, int y, int z)
{
  int i;
if(z>=x&&z<=y)
printf("IS WITHIN THE RANGE");
else
printf("IS OUT OF THE RANGE");
} 

int main() {

  printf("INTRODUCE LOW LIMIT\n");
  scanf("%i",&l);
  printf("INTRODUCE HIGH LIMIT\n");
  scanf("%i",&h);
  printf("INTRODUCE NUMBER\n");
  scanf("%i",&n);
  range(l,h,n);
  return 0;
}
UPPER AND LOW CASE LETTERS


## EX07
#Write a Python function that accepts a string
#and calculate the number of upper case letters
#and lower case letters. Go to the editor
#Sample String : 'The quick Brow Fox'
#Expected Output : 
#No. of Upper case characters : 3
#No. of Lower case Characters : 12

def upoelow(s):
    v={"UPPER":0, "LOWER":0}
    for c in s:
        if c.isupper():
           v["UPPER"]+=1
        elif c.islower():
           v["LOWER"]+=1
        else:
           pass#!!!!!!

    print ("No. of Upper case characters : ", v["UPPER"])
    print ("No. of Lower case Characters : ", v["LOWER"])

s=(input("INTRODUCE WORD : "))
upoelow(s)

## EX07.C
#include <stdio.h>
#include <string.h>
#define MAX 30

char S1[MAX];

void upalo(char x[MAX])
{
  int i, u, l;
  u=0;
  l=0;
for(i=0;i<=strlen(x);i++)
{
  if(x[i]>='A'||x[i]<='Z')
  u=u+1;
  else if(x[i]>='a'||x[i]<='z')
  l=l+1;
}
printf("\nNO. UPPER CASE: %i",u);
printf("\nNO. LOWER CASE: %i",l);


}

int main()
{
  printf("INTRODUCE THE WORD\n");
  fgets(S1,MAX,stdin);
  upalo(S1);
  return 0;
}


## EX08
#Write a Python function that takes a list
#and returns a new list with unique elements 
#of the first list. 
#Sample List : [1,2,3,3,3,3,4,5]
#Unique List : [1, 2, 3, 4, 5]

def uniq(number):
  x = []
  for a in number:
    if a not in x:
      x.append(a)
  return x

print(uniq([1,2,3,3,3,3,4,5])) 

## EX08.C
#include <stdio.h>
int main()
{
    int arr1[30], n, ctr;
    ctr=0;
    int i, j, k;

   printf("HOW MANY: ");
   scanf("%i",&n);
  
   for(i=0;i<n;i++)
        {
      printf("element");
      scanf("%d",&arr1[i]);
    }
printf("\nUNIQUE ELEMENTS: \n");
for(i=0; i<n; i++)
{
    ctr=0;
    for(j=0,k=n; j<k+1; j++)
    {
        if (i!=j)
        {
	       if(arr1[i]==arr1[j])
          {
             ctr=ctr+1;
           }
         }
    }
   if(ctr==0)
    {
      printf("%d ",arr1[i]);
    }
}
   printf("\n\n");
}

PRIME OR NOT


## EX09
#Write a Python function that takes
#a number as a parameter and check the 
#number is prime or not.
#Note : A prime number (or a prime) is a 
#natural number greater than 1 and that has 
#no positive divisors other than 1 and itself. 
#FIRST TIME USING RANGE!!!!!
def prime(n):

if (n==1):
    return print("IT IS")
elif (n==2):
    return print("IT IS")
else:
    for x in range(2,n):
        if(n % x==0):
            return print("IT IS NOT")
    return print("IT IS")       

print(prime(2))
## EX09.C
#include <stdio.h>
int num1;

void prime(int x)
{
int i,a;
a=0; 

  for(i=1;i<=x;i++)
  {
      if(x%i==0) 
      a++;
  }

  if(a==2) 
  {
      printf("El número es primo");
  }
  else
  {
      printf("El número no es primo"); 
  }

}

int main()
{
printf("Introduce un numero: ");
scanf("%d",&num1);
prime(num1);
}
EVEN NUMBERS FROM A RANGE
## EX10
#Write a Python program to print the even
#numbers from a given list. Go to the editor
#Sample List : [1, 2, 3, 4, 5, 6, 7, 8, 9] 
#Expected Result : [2, 4, 6, 8]
#append!!!!

def even(numbers):
    x = []
    for i in numbers:
        if i % 2 == 0:
            x.append(i)
    return x
print(even([1,4,5,4,6,7,10 ]))
## EX10.C
#include <stdio.h>
//FUNCTION TO EVEN NUMBERS
void even(x,y)
{
  int i;
for (i =x ; i <= y; i++) 
{
    if (i % 2 == 0) 
      printf("%d ", i);
}
}

int main() {
  int l, h;
  printf("low range:\n");
  scanf("%d", &l);
  printf("high range:\n");
  scanf("%d", &h);
  even(l, h);

  return 0;
}
PERFECT NUMBER


## EX11
#PERFECT NUMBER

def perf(n):
    sum = 0
    for x in range(1, n):#TO STOP IN THE NUMBER AND START IN 1
        if n % x == 0:
            sum += x
    return sum == n
print(perf(12))
 ## EX11.C
#include <stdio.h>
//PERFECT NUMBER
int N1;

int CARITO(int x)
{
  int i, sum;
  sum=0;
  for(i=1;i<x;i++)
  {
    if((x%i)==0)
    {
      printf("\n%i", i);
      sum=sum+i;
      printf("\n%i", sum);
    }
  }
  return sum;
}

void CARITO2(int x)
{
  int c;
  c=CARITO(x);
  if(c==x)
  {
    printf("IS PERFECT");
  }
  else
    printf("IS NOT PERFECT");
}

int main(void) {

  printf("ENTER THE NUMBER\n");
  scanf("%i",&N1);
  CARITO2(N1);
  return 0;
}


## EX12
#PALINDROMO 
def PALI(string):
  menor = 0
  mayor = len(string) - 1

  while mayor >= menor:
    if not string[menor] == string[mayor]:
      return False
    menor += 1
    mayor -= 1
  return True
print(PALI('ararara')) 

## EX12.C
#include <stdio.h>
#include <string.h>
#define MAX 30
// PALINDROMO 
char S[MAX];

int INVERT(char x[MAX])
{
  int mylen, i, ol;
  ol=0;
  mylen = strlen(x)-1;
for(i=mylen-1;i>=0;i--)//VA REVIRTIENDO LA PALABRA
  {

    if(x[i]!=x[mylen-i-1])//COMPARA LOS CARACTERES
    {
    ol=ol+1;
     break;//CON UNO QUE ENCUENTRE DIFERENTE DEJA DE COMPARAR
    }
    else 
    {
    ol=ol+0;//LA SUMA DA 0 CUANDO NO HAY NINGUNA DIFERENCIA
    }
  }
  return ol;
}

int main() 
{
  int resultado;
  fgets(S,MAX,stdin);
  resultado=INVERT(S);//LLAMO LA FUNCION METIENDOLA EN UNA VARIABLE DE ETSA FUNCION
  if(resultado!=0)
  {
    printf("0 NO ES PALINDROMO");
  }
  else
    printf("1 SI ES PALINDROMO");
return 0;
}
