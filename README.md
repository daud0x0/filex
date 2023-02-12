# filex
## filex - A Command Line Tool for File Encryption/Decryption
filex is a simple command line tool that can encrypt and decrypt files using the Fernet encryption method from the cryptography library in Python3. The tool allows you to either encrypt a file with a generated key or decrypt a file using a provided key.

## Instalation
    $ git clone https://github.com/daud0x/filex.git
    $ cd filex
    $ python3 -r requirements.txt

## Usage
- The -key or --key option is used to provide a key file for decryption. If the option is not provided, the tool will encrypt the file instead.
- The FILE argument is the name of the file to be encrypted or decrypted.

## Encrypting a File
- To encrypt a file, simply run filex without the -key option, and provide the file name as an argument:

    $ python3 filex.py file.txt
- The tool will generate a new key and write it to a file called key. It will then encrypt the contents of file.txt and overwrite the original file with the encrypted data.

## Decrypting a File
- To decrypt a file, run filex with the -key option, and provide the file name and key file as arguments:

    $ python3 filex.py -key key file.txt

- The tool will read the key from the key file, use it to decrypt the contents of file.txt, and overwrite the original file with the decrypted data.
