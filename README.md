# Project Name : Video_Steganography
# Developed By- Parth Lotte

# Video Steganography ( Hiding TEXT in Video ) :
* In video steganography we have used combination of cryptography and Steganography. We encode the message through two parts
* We convert plaintext to cipher text for doing so we have used RC4 Encryption Algorithm. ***RC4 is a stream cipher and variable-length key algorithm***. This algorithm encrypts one byte at a time. It has two major parts for encryption and decryption:-
* ***KSA(Key-Scheduling Algorithm)***- A list S of length 256 is made and  the entries of S are set equal to the values from 0 to 255 in ascending order. We ask user for a key and convert it to its equivalent ascii code. S[] is a permutation of 0,1,2....255, now a variable j is assigned as   j=(j+S[i]+key[i%key_length) mod 256 and swap S(i) with S(j)  and accordingly we get new permutation for the whole keystream according to the key.
* ***PRGA(Pseudo random generation Algorithm (Stream Generation))*** -  Now we take input length of plaintext and initiate loop to generate a keystream byte  of equal length. For this we initiate i=0, j=0 now increment i by 1 and mod with 256. Now we add S[i] to j amd mod of it with 256 ,again swap the values. At last step take store keystreambytes which matches as S[(S[i]+S[j]) mod 256] to finally get key stream of length same as plaintext. 
* Now we xor the plaintext with keystream to get the final cipher.

 