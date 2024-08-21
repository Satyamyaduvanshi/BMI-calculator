def caesar_cipher(text, shift):
    result = ""
    
    for char in text:
        if char.isalpha():
            if char.isupper():
                result += chr((ord(char) + shift - 65) % 26 + 65)
            else:
                result += chr((ord(char) + shift - 97) % 26 + 97)
        else:
            result += char  # Skip non-alphabetic characters
    
    return result

# Get user input
text = input("Enter the plain text: ")
shift = int(input("Enter the shift value: "))

# Display the result
cipher_text = caesar_cipher(text, shift)
print("Ciphered text:", cipher_text)
