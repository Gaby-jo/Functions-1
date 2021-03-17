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
