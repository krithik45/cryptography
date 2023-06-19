#include <stdio.h>
#include <string.h>

int main()
{
    char plaintext[100], ciphertext[100];
    int i, j, len;
    char key[26] = {'Q', 'W', 'E', 'R', 'T', 'Y', 'U', 'I', 'O', 'P', 'A', 'S', 'D', 'F', 'G', 'H', 'J', 'K', 'L', 'Z', 'X', 'C', 'V', 'B', 'N', 'M'};

    printf("Enter a message: ");
    fgets(plaintext, 100, stdin);
    len = strlen(plaintext);

   
    for (i = 0; i < len; i++)
    {
        if (plaintext[i] >= 'a' && plaintext[i] <= 'z')
        {
            ciphertext[i] = key[plaintext[i] - 'a'];
        }
        else if (plaintext[i] >= 'A' && plaintext[i] <= 'Z')
        {
            ciphertext[i] = key[plaintext[i] - 'A'];
        }
        else
        {
            ciphertext[i] = plaintext[i];
        }
    }
    ciphertext[i] = '\0';

    printf("Encrypted message: %s\n", ciphertext);

    for (i = 0; i < len; i++)
    {
        if (ciphertext[i] >= 'a' && ciphertext[i] <= 'z')
        {
            for (j = 0; j < 26; j++)
            {
                if (key[j] == ciphertext[i])
                {
                    plaintext[i] = j + 'a';
                    break;
                }
            }
        }
        else if (ciphertext[i] >= 'A' && ciphertext[i] <= 'Z')
        {
            for (j = 0; j < 26; j++)
            {
                if (key[j] == ciphertext[i])
                {
                    plaintext[i] = j + 'A';
                    break;
                }
            }
        }
        else
        {
            plaintext[i] = ciphertext[i];
        }
    }
    plaintext[i] = '\0';

    printf("Decrypted message: %s\n", plaintext);

    return 0;
}
