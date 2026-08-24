# Hacking-and-Cryptanalysis-of-AES
## 1.Hacking key through Language Statistics
Here, we illustrate decryption of cipher message through general English language statistics. We analyze language statistical properties of message and contrast it with general statistical properties of English. This will help you understand vulnerabilities in cipher messages or say encryption algorithms e.g. our cipher text is encrypted from substitution cipher which has very large key space of order 29! which in raw checking all keys will take most fastest computer today 280 billion years i.e. 20,000 times current age of universe.

The substitution key is derived through character/word frequency analysis and linguistic pattern of the English language. Note I have written deduced alphabets as capital e.g. for p is deduced to e, p → E and also after deducing I replace every p with E in cipher message.  Here are the logical steps used to infer the characters:
1. Space is most frequently used, so in cipher text is character c i.e. c → space
2. 1-Letter Words: The general English pattern for 1-letter words consists of I and a. In the ciphertext, the characters b and m appear as isolated 1-letter words. Since b appears more frequently than m throughout the text, we deduce that b → A and m → I.
3. Most Frequent Characters: After the space character, e and t are most frequent characters in the English language, so here are p and d in ciphertext, and presence of words Id and Ad allowing us to deduce d → T and p → E.
4. Now, a and u are most frequent and word Ta appears frequently which can be only TO i.e. a → O. Words Iu, IuE, uOT implies u → N and words oNINTENTIONAttr, tITTtE, rOo, ANNOrINh, AhAIN decodes t→ L, r→ Y, h→ G and o→ U
5. Since every vowel is deduced, its much easy to guess words and phrases from cipher text. Phrases [NO INTE,EkT], [,IGHT TO T,EAT YOU] and [Ak ENEwIES]and [wOST ANNOYING] and words TsE, TsAT deduces comma→ R, k→ S, s→ H and w→ M.
6. Phrase [I HAeE THE RIGHT] deduces e→ V, [YOU HAVE yOME TO], [I yOULv], [yONTINUEv THE STRANGERf] and [YOU UNDERSTAND THENf SIRf] deduces
y→ C,v t→ D and f→ COMMA. Also [I ANS ERED], [BENEATH THE ATERS] deduces space→ W. [gORCE COULD DESTROY],Og deduces g→ F, [BROqEN ALL TIES [SINq BENEATH] deduces q→ K. CA.TAIN,[SE.ERATE MYSELF FROM YOU] deduces fullstop→ P and [FORGET THAT YOU HAD EVER ElISTEDx],[TIES OF HUMANITYx] deduces l→ X and x→ FULLSTOP and lastly [THIS zUESTION EMBARRASED ME] deduces z→ Q. In ciphertext letter i and n didn’t appear and j, z are left to map . We can have complete remaining map as i→ J and n→ Z

## 2. AES execution and hacking 
We have executed 8-byte Advanced Encryption Scheme (AES) which cleverly uses concept of round functions to provide Avalanche effect in cipher message i.e. single bit change of plaintext will result in completely different cipher message, although this is also reason it can be attacked since there is competitiveness in thieves also. Check AES_execution file.
In file AES_hacking, we have shared hacking of AES algorithm through Correlation Power Analysis(CPA). Through power traces files we have find linear correlation between actual power with estimated power through distribution overlap. In correct guessed key , overlap peak distinguishes and we hack the correct key.

