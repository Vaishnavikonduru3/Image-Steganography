Python GUI based application for Image Steganography

Steganography is the process of hiding a secret message within a larger one in such a way that someone can not know the presence or contents of the hidden message. The purpose of Steganography is to maintain secret communication between two parties. Unlike cryptography, which conceals the contents of a secret message, steganography conceals the very fact that a message is communicated.

Encoding

The algorithm is as follows:
For each character within the data, its ASCII value is taken and converted into 8-bit binary.

Three pixels are read at a time having a complete of 3*3=9 RGB values. the primary eight RGB values are wont to store one character that's converted into an 8-bit binary.

The corresponding RGB value and binary data are compared. If the digit is 1 then the RGB value is converted to odd and, otherwise, even.

The ninth value determines if more pixels should be read or not. If there's more data to be read, i.e. encoded or decoded, then the ninth pixel changes to even. Otherwise, if we would like to prevent reading pixels further, then make it odd.

Decoding

For decoding, we shall attempt to find the way to reverse the previous algorithm that we wont to encode data. Again, three pixels are read at a time. the primary 8 RGB values give us information about the key data, and therefore the ninth value tells us whether to maneuver forward or not.

For the primary eight values, if the worth is odd, then the binary bit is 1, otherwise it's 0.

The bits are concatenated to a string, and with every three pixels, we get a byte of secret data, which suggests one character. Now, if the ninth value is even then we keep reading pixels three at a time, or otherwise, we stop.

