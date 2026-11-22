#include <stdio.h>
#define MAX 100;

void main()
{
    int a[100], n, i, largest, smallest;
    int even = 0, odd = 0;
    long long sum = 0;
    double mean;

    printf("Enter number of elements (1-100): ");
    scanf("%d", &n);

    if (n < 1 || n > 100)
    {
        printf("Invalid array size.\n");
        return 1;
    }

    for (i = 0; i < n; i++)
    {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &a[i]);
    }

    largest = smallest = a[0];

    for (i = 0; i < n; i++)
    {
        sum += a[i];

        if (a[i] > largest)
            largest = a[i];

        if (a[i] < smallest)
            smallest = a[i];

        if (a[i] % 2 == 0)
            even++;
        else
            odd++;
    }

    mean = (double)sum / n;

    printf("\nSum = %lld\n", sum);
    printf("Arithmetic mean = %.2f\n", mean);
    printf("Largest = %d\n", largest);
    printf("Smallest = %d\n", smallest);
    printf("Even elements = %d\n", even);
    printf("Odd elements = %d\n", odd);

    getch();
}



Smallest = 17
Even elements = 1
Odd elements = 3
