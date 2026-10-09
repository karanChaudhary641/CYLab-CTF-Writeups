# Python Wrangling

## Challenge Overview
* **Category:** General Skills
* **Concepts Tested:** Command Line Interface (CLI) execution, python arguments, file analysis.

## Methodology

### 1. Environmental Reconnaissance
First, I inspected the files provided in the challenge workspace using basic Linux utilities:
* `ende.py`: The python script responsible for encryption/decryption routines.
* `flag.txt.en`: The encrypted payload.
* `pw.txt`: The text file containing the clearance password.

### 2. Execution & Terminal Interaction
I leveraged the terminal to pull the challenge resources, check the script requirements, and execute the decryption payload. Here is the exact command sequence executed in the workspace shell:

```bash
# Downloaded the challenge files directly into the workspace terminal
wget https://picoctf.net
wget https://picoctf.net
wget https://picoctf.net

# Viewed the contents of the password file to get the decryption key
cat pw.txt

# Executed the decryption script using the terminal flag '-d' 
# Passed the password string into the prompt when requested
python3 ende.py -d flag.txt.en
```
*Result: The terminal successfully decrypted the cipher block and printed out the raw flag token string.*

## Key Takeaways
* Mastered passing conditional flags (`-d`) into python binaries directly via the shell.
* Developed comfort handling and piping operational scripts without needing to alter source code.
