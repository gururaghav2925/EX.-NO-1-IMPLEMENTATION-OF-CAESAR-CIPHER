## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
 

## AIM:

To implement the simple substitution technique named Caesar cipher using Python language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-
```py

def caesar_cipher_encrypt(text, key):
    cipher = ""
    for ch in text:
        if ch.isupper():
            cipher += chr((ord(ch) - ord('A') + key) % 26 + ord('A'))
        elif ch.islower(): 
            cipher += chr((ord(ch) - ord('a') + key) % 26 + ord('a'))
        else:
            cipher += ch  
    return cipher
def caesar_cipher_decrypt(cipher, key):
    plain = ""
    for ch in cipher:
        if ch.isupper():  
            plain += chr((ord(ch) - ord('A') - key) % 26 + ord('A'))
        elif ch.islower():  
            plain += chr((ord(ch) - ord('a') - key) % 26 + ord('a'))
        else:
            plain += ch
    return plain
plain = input("Enter the plain text: ")
key = int(input("Enter the key value: "))

print("\nPLAIN TEXT:", plain)

cipher = caesar_cipher_encrypt(plain, key)
print("ENCRYPTED TEXT:", cipher)

decrypted = caesar_cipher_decrypt(cipher, key)
print("DECRYPTED TEXT:", decrypted)

```


## OUTPUT :-


<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/fa5e0f01-fa74-43ee-ab20-76567822e3d9" />



## Result:
The implementation of the simple substitution technique named Caesar cipher using Python language was completed and executed successfully.
