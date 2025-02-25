# Steganography

This project provides a simple implementation of **image-based steganography**, where secret messages are hidden within an image and later retrieved using a decryption script. The encryption and decryption processes involve modifying the pixel values of an image to store message bytes securely.

## Features

- **Message Hiding:** Embed a secret message within an image using pixel manipulation.
- **Password Protection:** Secure the message with a user-defined passcode.
- **Message Extraction:** Retrieve the hidden message only with the correct password.
- **Lightweight and Simple:** Minimal dependencies using Python and OpenCV.

## Requirements

Ensure you have the required dependencies installed before running the script:

```sh
pip install opencv-python
```

## How It Works

1. **Encryption Process:**
   - The script reads an image and embeds a secret message within its pixel values.
   - A passcode is required for encrypting the message.
   - The modified image is saved as `encryptedImage.jpg`.

2. **Decryption Process:**
   - The script reads `encryptedImage.jpg`.
   - You must enter the correct passcode to retrieve the hidden message.
   - If the passcode is incorrect, access will be denied.

## Usage

### Encrypt a Message
1. Run the script.
2. Enter the secret message.
3. Set a passcode for encryption.
4. The encrypted image will be saved.

### The Encryption and Decryption code is in the same file so it will decrypt at the same time
1. Enter the correct passcode.
2. If the password matches, the hidden message will be displayed.

## Running the Script

To execute the script, use the following command:

```sh
python stego.py
```

## Example Workflow

```
Enter secret message: Hey What's Up!
Enter a passcode: 1234
Encrypted image saved as 'encryptedImage.jpg'
Enter passcode for Decryption: 1234
Decryption message: Hey What's Up!
```

## Important Notes

- The encryption process modifies pixel values to store message data.
- Ensure that the message length does not exceed the image capacity.
- A termination marker is used to detect the end of the message.

## License

This project is open-source and available under the MIT License.

## Author

Anupam Biswas
