# Shift-Cipher
  A shift cipher is a simple encryption method. When encrypting a message, every letter in the original message is replaced by a different letter, k positions down the alphabet (module by 26), where k is an integer. 

  The purpose of this program is to implement a shift cipher decrypter to decrypt encrypted messages using the shift cipher method. It is assumed that the message only contains upper case letters, space characters and punctuation marks. Space characters, punctuation marks and numbers remain unchanged during the encryption. A shift cipher decrypter can guess the message without knowing k. If a message is long enough, the most frequent letter will be ‘E’.

  The input of the program will be a text message received via file importation in order to ensure data verification (make sure the data is accurate and consistent) and prevent any data discrepancies by typing errors. After receiving the text, the program will decrypt the text. Finally, the decrypted text will be outputted (and stored back into the file that was imported to the program).

