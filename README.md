#include <stdio.h>
#include <string.h>

char* revsestring(char* ptr){
    int i=0;
     int l=0;
    for(l;ptr[l]!='\0';l++);
    
    printf("%d\n",l);
    while(i<=l/2){
        char temp = *(ptr+i);
        *(ptr+i) = *(ptr+(l-1-i));
        *(ptr+(l-1-i)) = temp;
        i++;
    }
    return ptr;
}
int main()
{
     //reverse the given string
    char string[] = "alok";
    revsestring(string);
    printf("%s",string);    
    return 0;
}
// output: 4, kola
