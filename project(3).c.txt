#include <stdio.h>

struct Student {
    int roll;
    char name[30];
    float cutoff;
    char city[30];
    char dream[30];
};

int main() {
    struct Student s[50];
    int n, i;

    printf("Enter number of students: ");
    scanf("%d", &n);

    if (n <= 0 || n > 50) {
        printf("Invalid student count!");
        return 0;
    }

    for (i = 0; i < n; i++) {
        printf("\nEnter details of Student %d\n", i + 1);

        printf("Roll Number: ");
        scanf("%d", &s[i].roll);

        printf("Name: ");
        scanf("%29s", s[i].name);

        printf("Cut-off Mark: ");
        scanf("%f", &s[i].cutoff);

        printf("City: ");
        scanf("%29s", s[i].city);

        printf("Dream: ");
        scanf("%29s", s[i].dream);
    }

    printf("\n--- STUDENT DETAILS ---\n");

    for (i = 0; i < n; i++) {
        printf("\nStudent %d\n", i + 1);
        printf("Roll Number: %d\n", s[i].roll);
        printf("Name: %s\n", s[i].name);
        printf("Cut-off Mark: %.2f\n", s[i].cutoff);
        printf("City: %s\n", s[i].city);
        printf("Dream: %s\n", s[i].dream);
    }

    return 0;
}


OUTPUT:

       Enter number of students: 2

Enter details of Student 1
Roll Number: 101
Name: Arun
Cut-off Mark: 185.5
City: Chennai
Dream: Engineer

Enter details of Student 2
Roll Number: 102
Name: Kumar
Cut-off Mark: 190.5
City: Madurai
Dream: Doctor

--- STUDENT DETAILS ---

Student 1
Roll Number: 101
Name: Arun
Cut-off Mark: 185.50
City: Chennai
Dream: Engineer

Student 2
Roll Number: 102
Name: Kumar
Cut-off Mark: 190.50
City: Madurai
Dream: Doctor