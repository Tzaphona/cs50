# cs50

#include <cs50.h>
#include <stdio.h>

int main()
{
    
    int height;
    printf("height: ");
    do
    {
        height = GetInt();
        while (height<0||height>23) 
        {
            printf("retry: ");
            height = GetInt();
        }
        break;
    }while (height<0||height>23);

/* spacetart of pyramid */


/*
 *   ## 
 *  ### 
 * ####
 *#####
 *
*/

int a;
int b;
int c;
int d = 0;

char space = 33;
char pound = 35;

while (d <= height)
{   
    // space. (b) //
    for (b = 2 ; b<=height-d; b++)
    {
        printf("%c", space);
    }   
    
    // second pound - (a) //
    for (a=1; a<=height-d ; a++)
    {
        if (d!=height-1)
        {
        printf("%c", pound);
        }
    }
       // one line down - (a) //    
    for (a=height-d; a>0; a++)
    {
        if(d!=height-1)
        {
        printf("\n");
        break;
        }
    }
    
    d++;
} // close-braket of main while loop //

 // last for formula - bottom line. //
for (c = 0; c<=height; c++)
{
    printf("%c", pound);
}
{
    printf("\n");
}
} // close-braket of int main() //
