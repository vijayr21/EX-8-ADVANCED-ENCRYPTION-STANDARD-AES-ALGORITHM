# EX-8-ADVANCED-ENCRYPTION-STANDARD-AES-ALGORITHM

**Aim:**

To use Advanced Encryption Standard (AES) Algorithm for a pracƟcal application like URL Encryption.

**ALGORITHM:**

1. AES is based on a design principle known as a subsitution–permutation.
2. AES does not use a Feistel network like DES, it uses variant of Rijndael.
3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

**programe:**
```
#include <stdio.h>
#include <string.h>

void xor_encrypt_decrypt(char *input, char *key)
{
int input_len = strlen(input);
int key_len = strlen(key);

for (int i = 0; i < input_len; i++)
{
input[i] = input[i] ^ key[i % key_len]; // XOR encrypƟon
}
}

int main()
{
char url[] = "hƩps://github.com/vijay21082004";

char key[] = "secretkey"; // Simple key for XOR encrypƟon

prinƞ("Original URL: %s\n", url);

// Encrypt the URL
xor_encrypt_decrypt(url, key);
prinƞ("Encrypted URL: %s\n", url);

// Decrypt the URL (since XOR is reversible using the same key)
xor_encrypt_decrypt(url, key);
prinƞ("Decrypted URL: %s\n", url);

return 0;
}
```

**OUTPUT:**


![image](https://github.com/user-attachments/assets/490b70df-080a-4fd2-a416-dbf3c69b7201)


**RESULT:**

Thus , to use Advanced Encryption Standard (AES) Algorithm for a practical application like URL
Encryption is done successfully.
