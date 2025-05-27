# Square-Root-without-sqrt-
Orginally called Exercise5.c

// Exercise 5

#include <stdio.h>
#include <math.h>

int main(void)
{
    float a;
    float x;

    printf("please input 'a':\n");
    scanf("%f", &a);

    printf("please choose a starting number:\n");
    scanf("%f", &x);

    while(1)
    {
        float xnew = 0.5 * (x + a / x);
        if (fabs(xnew - x) < 0.0000001)
        {
            break;
        }

        printf("-> x is now %f\n", x);
        x = xnew;
    }

    printf("the square root of %f is %f\n", a, x);
    
    return 0;
}
