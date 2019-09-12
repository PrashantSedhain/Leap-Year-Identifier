# Leap-Year-Identifier
This small C program gives the number of days in certain days of the month after taking input of year and month as an integer value from the user. It also accounts for possible leap year.

#include <stdio.h>
#include <stdlib.h>

int main(int argc, char** argv) {
    int year;
    int month; 
    while(1)
    {
        printf("Enter year month: ");
        scanf("%d", &year);
        scanf("%d", &month);
        
        switch(month)
        {
            case 1:
                printf("January has 31 days\n");
                break;
                
            case 2:
                if(year % 400 == 0)
                {
                   printf("February has 29 days. (leap year)\n"); 
                }
                else if(year % 100 == 0)
                {
                    if(year % 400 == 0)
                    {
                        printf("February has 29 days.(Leap year)\n");
                    }
                }
                else if(year % 4 == 0)
                {
                   printf("February has 29 days.(Leap year)\n");
                }
                
                else
                {
                    printf("February has 28 days. (Not a leap year)\n");
                }    
                break;
                
            case 3:
                printf("March has 31 days\n");
                break;
                
            case 4:
                printf("April has 30 days\n");
                break;    
                
            case 5:
                printf("May has 31 days\n");
                break;
                
            case 6:
                printf("June has 30 days\n");
                break;
                
            case 7:
                printf("July has 31 days\n");
                break;
                
            case 8:
                printf("August has 31 days\n");
                break;  
                
            case 9:
                printf("September has 30 days\n");
                break;
                
            case 10:
                printf("October has 31 days\n");
                break;
                
            case 11:
                printf("November has 30 days\n");
                break;
                
            case 12:
                printf("December has 31 days\n");
                break;        
        }
        
    }
     
}


