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

### 2. Execution & Script Interactions
Running the script without arguments revealed its usage documentation:
```bash
python3 ende.py
```
*Output indicated that `-e` encrypts and `-d` decrypts.*

I executed the decryption sequence by targeting the ciphertext and feeding the contents of `pw.txt` when prompted:
```bash
python3 ende.py -d flag.txt.en
```

## Key Takeaways
* Mastered passing conditional flags (`-d`) into python binaries directly via the shell.
* Developed comfort handling and piping operational scripts without needing to alter source code.
