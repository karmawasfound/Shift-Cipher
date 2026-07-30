# Algorithm Design

## Initialization 
After receiving the text file (input), the program will store the text in a list called msg. In the program, a variable named new_msg will be initialized for later use, and a list called freq, with a length of 26 and each stored initially with 0 (in integer type), is created to store the frequency of alphabetical letters in msg. 


## Frequency of letters
 Then, a for loop will be executed, which will be as long as the length of the number of characters in msg. In each loop, the loop will be checking the letter corresponding to the number of times (nth times) it has looped. Inside the loop, a temporary variable ch will be used to store the ASCII code of the character. Since the text only contains capital letters, we only need to check whether the character’s ASCII code falls within 65 to 90 (inclusive). If it does, it will be stored in the (ASCII code of letter - 65)th term of the list freq, and the counter will go up by 1. If it doesn’t, the loop will automatically go to the next loop ((n+1)th), until all characters of msg have been checked. After the data frequency of the text message, decryption of the text will start.


## Special cases
  Each loop, the character will be turned into ASCII code form. Since the English language has some special rules and traits, this program will be utilizing them in order to quicken the decryption process.

  First, since SS, EE, TT, FF and LL are the 1st, 2nd, 3rd and 4th most common repeats of letters in English, by referencing the text, if there are repeats of letters, it will find the absolute value, k, of the highest number in list freq and S. If the user deems it wrong, then the absolute value, k, of the highest number in list freq and E will be found and shifted, and so on.

  Second, an apostrophe is usually accompanied by a S, and seldom a C. So, if an apostrophe appears, it will find the absolute value, k, of the highest number in list freq and S. If the user deems it wrong, then the absolute value, k, of the highest number in list freq and C will be found and shifted, and so on.

  Third, since Q is most likely followed by U, if there are 2 letters which have a difference of 4 (the difference of ASCII code of Q and U), and the latter letter has an equal or larger frequency than the first letter, it will find the absolute value, k, of the highest number in list freq and Q.

  Fourth, since E, T, A and O are the 1st, 2nd, 3rd and 4th most common letters in English, the text will shift so that E has the highest frequency. It will find the absolute value, k, of the highest number in list freq and E. If the user deems it wrong, then the absolute value, k, of the highest number in list freq and T will be found and shifted, and so on.

  If the number k used to shift was deemed wrong by the user, the letter in which k was referencing will be stored as 0 in freq in order to prevent repetition. Any frequency stored as 0 in freq will be skipped and not be referenced to shift.

  All outputs will be stored in new_msg. The most likely special case in the above will be outputted first, followed by the most likely special case of the next scenario. After all most likely cases have been exhausted, the 2nd most likely case will be outputted.


Shifting
  After the data frequency, a for loop will be executed as a function. After defining the function,  which will be responsible for shifting, the for loop will be as long as the length of the number of characters in msg. In each loop, it will be shifting the letter corresponding to the number of times (nth times) it has looped. k will be the number the whole text message will shift, and is inputted into the function.

  In order to find the number to shift the characters in the special cases, in each loop, the character will be turned into ASCII code form first. Then, the program will find the absolute value, k, of the original letter and the predicted letter, and add it to the ASCII code of the letters. It is noted that during shifting, if the ASCII code goes out of the alphabet bound (65-90), it will then deduct (instead of add) the number to be shifted (details of shifting in the above segment).  

  If the user deems the text to be deciphered correctly, the correct text message will be stored back into the original file. However, if the user still deems it incorrect, it will continue shifting as mentioned in the above segment. new_msg will be cleared for the next loop. If even after exhausting all the special cases, the message is still not decrypted, the program will shift the text message according to the alphabetical order until the message is decrypted. The program will output new_msg, then it will end.

