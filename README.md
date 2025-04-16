# EX-4-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM

## Aim:
  To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM: 

Name: Muthulakshmi D
reg : 212223040122
```
def simple_aes_encrypt(plaintext, key):
    ciphertext = ''
    for i in range(len(plaintext)):
        ciphertext += chr(ord(plaintext[i]) ^ ord(key[i % len(key)]))
    return ciphertext

def simple_aes_decrypt(ciphertext, key):
    decrypted = ''
    for i in range(len(ciphertext)):
        decrypted += chr(ord(ciphertext[i]) ^ ord(key[i % len(key)]))
    return decrypted

def print_ascii(ciphertext):
    print("Encrypted Message (ASCII values):", end=' ')
    for char in ciphertext:
        print(ord(char), end=' ')
    print()

# Main
plaintext = input("Enter the plaintext: ")
key = input("Enter the key: ")

ciphertext = simple_aes_encrypt(plaintext, key)
print_ascii(ciphertext)

decrypted_text = simple_aes_decrypt(ciphertext, key)
print("Decrypted Message:", decrypted_text)
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/a37c3321-4bf5-4010-ac2d-6b973ee1f89d)

## RESULT: 
THE PROGRAM IS EXECUTED SUCCESSFULLY
