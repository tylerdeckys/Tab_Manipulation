#include <stdio.h>

#define Max 100
#define tabstop 5

int retab(char input[Max], char output[Max], int length);
int detab(char input[Max], char output[Max], int length);
int getline2(char input[]);

char inputstring[Max];
char outputstring[Max];

int main()
{
    int length;

    while((length = getline2(inputstring)) > 0)
    {
         

        detab(inputstring, outputstring, length);

        printf("%s\n", outputstring);
    }

    return 0;
}

//get line, return length
int getline2(char out[])
{
    int c, i;
    i = 0;
    while (( c = getchar()) != EOF && (c!= '\n'))
    {
        out[i] = c;
        i++;
    }   
    out[i] = '\0';
    return i;
}

//the big boi
int retab(char in[], char out[], int length)
{
    int i, l;
    l = 0;

    //tabber
    for (i = 0; i < length; i++)
    {
        if((in[i] == ' ') && (in[i+1] == ' ') && (in[i+2] == ' ') && (in[i+3] == ' '))
        {
            out[l] = '*';

            i = i + 3;
            l++;
        }

        else
        {
        out[l] = in[i];
        l++;
        }
    }
    
    out[l] = '\0';
    return 0;
}

//getline AND replace tabs with spaces up to every multiple of the #tabstop
int detab(char in[], char out[], int length) 
{
    int i, l;
    l = 0;

    for(i = 0; i <length;i++)
    {
        if (in[i] == '\t')
        {
            int x = 0;

            while(x<tabstop)
            {
                out[l+x] = ' ';
                x++;
            }


            l = l + tabstop;
        }

        else
        {
            out[l] = in[i];
            l++;
        }
    }

    out[l] = '\0';

    return i;
}
