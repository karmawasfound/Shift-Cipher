  The program can successfully decrypt messages through 2 methods: 1) allowing users to input the number to be shifted by themselves, and 2) the program trying to decrypt it on its own. 

  The shifting in this program works by first putting the text in the text file into a list. Then, the process of shifting will differ if users have the number to be shifted or not.
 
## Method 1
  After putting the letters into a list, it will ask the user for the number to be shifted upwards by (k). After that, the ASCII code of the current letter will be subtracted by k. If the letters go out of range, 26 is added to the ASCII code. Only alphabetical letters will be shifted. Rinse and repeat until all the letters have been shifted. If the output is not desirable, Users can either choose to input again, or change to Method 2, where the program will guess the number k by itself.

  Implementing the first method allows users who know the number to be shifted to input it directly, which removes the hassle for them to go through the process of guessing the correct message, making it less time consuming and more flexible.


## Method 2
  After putting the letters into a list, the program will find the frequencies of each letter. Then, it will subtract the ASCII code of the letter with the current highest frequency with the ASCII code of E/e (depending on the current letter to be shifted) to get the absolute value of the difference, which is the value of the number to be shifted, k. After that, the ASCII code of the current letter will be subtracted by k. If the letters go out of range, 26 is added to the ASCII code. Only alphabetical letters will be shifted. Rinse and repeat until all the letters have been shifted.

  Implementing the second method allows users who are unsure of the number that is shifted to also get the result they want, allowing more users to be able to use this program.

## Advantages of the current shifting method implemented
  The program does not shift non-alphabet letters, keeping the symbols of the original text. This program also keeps the upper and lower case of the original text. These all ensure that the text is as close to the original text as possible. 

  The program also allows people to choose to either save the new decrypted text in the original file, or a completely new file. This allows users to have more flexibility when using this program.

