 # AES_C_encryption 
 
 While doing research about ransomware attacks, in an attempt to further understand how ransomware encrypts files I created a simple C program that serves as an example of how ransware could hypothetically encrypt files. I decided to utilize AES encryption and favored C over a simpler C++ program because I wanted the full experience of working with encryption in memory. 

 For the sake of the example, however, the program is only targeted at a specific directory (notice the directory input) and the encryption key is static (the encryption key is not randomized).

# Static and Randomized encryption keys

 When working in reverse engineering ransomware or attempting to recover from a ransomware attack it's important to understand if the encryption key is static or not. It's important because if the key is static, than one could hypothetically (very rarely, however) reverse engineer it with a tool like GDB and find, or more accurately, deduce the static key. Another possibility is to run the program in a vm and dump the memory to obtain it if the ransomware stores the key in memory.

 Figuring out whether a ransomware has a static key or not is simple in theory. A way to narrow it down is to simply run multiple instances of the ranswomware in either GDB or a vm and see if the encryption keys match, then you'll now it's static. The tricky part is, it's difficult to know if what you're looking at is even an encryption key at all! Reverse engineering binaries is a very diffacult task and I respect anyone who can or is dedicated enough to take that on.

 HOWEVER! if the key is randomized and sent from the victim pc to the attacker's host system upon infection, then obtaining the dencryption key is a lot more difficult of a task, and I imagine any attacker skilled enough to successfully impact a company is smart enough to know this. Not to mention, most ransomware attacks are carried out through the use of ransomware bought from brokers online, which are developed by skilled individuals.

# Educate me!

 Is any of this wrong? Do you have any more knowledge to add to this topic? Please let me know! I would love to corrected and learn more about the topic!
