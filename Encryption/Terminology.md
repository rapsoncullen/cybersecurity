## Plaintext
- Data before encryption or hashing, could be text but it could also be a photograph or other file
## Encoding
- This is not encryption, it is just a form of data representation like how I could be writing this out in hexadecimal.
## Hash
- The output of a hash function, typically in raw bytes which are then encoded into something like base64
## Cryptoanalysis
- Attacking cryptography by trying to find a weakness in the underlying maths
## Hash Function
- A mathematical function that takes some input data of any size and returns an output of fixed size that is very difficult to reverse. Used very often in passwords.
## Hash Collision
- Attacking a hash function by finding multiple inputs that give the same output. Since input can be of any size but output is a fixed size there are infinite number of inputs that can get the same output. SHA1 and MD5 have been attacked in this way.