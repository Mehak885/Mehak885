#include <stdio.h>

void printMonth(int month, int startDay)
{
    const char *monthNames[] = {"January", "February", "March", "April", "May", "June",
                                 "July", "August", "September", "October", "November", "December"};
    int daysInMonth;

    switch (month) 
    {
        case 0: daysInMonth = 31; break; 
        case 1: daysInMonth = 28; break; 
        case 2: daysInMonth = 31; break; 
        case 3: daysInMonth = 30; break; 
        case 4: daysInMonth = 31; break; 
        case 5: daysInMonth = 30; break; 
        case 6: daysInMonth = 31; break; 
        case 7: daysInMonth = 31; break; 
        case 8: daysInMonth = 30; break; 
        case 9: daysInMonth = 31; break; 
        case 10: daysInMonth = 30; break; 
        case 11: daysInMonth = 31; break; 
    }

    printf("\n  %s  \n", monthNames[month]);
    printf("Su Mo Tu We Th Fr Sa\n");

    for (int i = 0; i < startDay; i++) {
        printf("   ");
    }

    for (int day = 1; day <= daysInMonth; day++) {
        printf("%2d ", day);
        if (++startDay > 6) {
            startDay = 0;
            printf("\n");
        }
    }
    printf("\n");
}

int main()
{
    int startDay = 3; 

    printf("Calendar for the Year 2025\n");
    for (int month = 0; month < 12; month++) {
        printMonth(month, startDay);
        
        switch (month) {
            case 0: startDay = (startDay + 31) % 7; break; 
            case 1: startDay = (startDay + 28) % 7; break; 
            case 2: startDay = (startDay + 31) % 7; break; 
            case 3: startDay = (startDay + 30) % 7; break; 
            case 4: startDay = (startDay + 31) % 7; break; 
            case 5: startDay = (startDay + 30) % 7; break; 
            case 6: startDay = (startDay + 31) % 7; break; 
            case 7: startDay = (startDay + 31) % 7; break; 
            case 8: startDay = (startDay + 30) % 7; break; 
            case 9: startDay = (startDay + 31) % 7; break; 
            case 10: startDay = (startDay + 30) % 7; break; 
            case 11: startDay = (startDay + 31) % 7; break; 
        }
    }

    return 0;
}

<!---
Mehak885/Mehak885 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
