# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main()
{
    char plain[100], cipher[100];
    int key, i, length;

    printf("Enter the plain text: ");
    scanf("%99s", plain);

    printf("Enter the key value: ");
    scanf("%d", &key);

    printf("\nPLAIN TEXT: %s", plain);

    length = strlen(plain);

    printf("\nENCRYPTED TEXT: ");

    for (i = 0; i < length; i++)
    {
        cipher[i] = plain[i] + key;

        if (isupper(plain[i]) && cipher[i] > 'Z')
            cipher[i] -= 26;

        if (islower(plain[i]) && cipher[i] > 'z')
            cipher[i] -= 26;

        printf("%c", cipher[i]);
    }

    cipher[length] = '\0';

    printf("\nDECRYPTED TEXT: ");

    for (i = 0; i < length; i++)
    {
        plain[i] = cipher[i] - key;

        if (isupper(cipher[i]) && plain[i] < 'A')
            plain[i] += 26;

        if (islower(cipher[i]) && plain[i] < 'a')
            plain[i] += 26;

        printf("%c", plain[i]);
    }

    printf("\n");

    return 0;
}

## OUTPUT:
<img width="1227" height="770" alt="image" src="https://github.com/user-attachments/assets/89353487-9746-43a0-bdd6-ead028cadd10" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
