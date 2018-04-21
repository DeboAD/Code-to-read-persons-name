# Code-to-read-persons-name 
#include "stdafx.h"
#include <stdio.h>
#include "string.h"

void main()
{
	int i, j=0; 
	int z;
	char fullName[100];
	char firstName[30], middleName[30], surname[30];
	char initial;

	printf("enter full name: ");

	gets_s(fullName);
	printf("Thank you %s\n\n", fullName);


	i = 0;
	do
	{
		firstName[i] = fullName[i];
		i++;
	} while (fullName[i] != ' ');

	firstName[i] = '\0';

	j = 0;
	do
	{
		middleName[j] = fullName[i];
		i++;
		j++;

	} while (fullName[i] != ' ');
	middleName[j] = '\0';


	z = 0;
	do
	{
		surname[z] = fullName[i];
		i++;
		z++;
	} while (fullName[i] != '\0');
	surname[z] = '\0';
	initial = middleName[1];
	printf("%s %c %s \n", firstName, initial, surname);
}

