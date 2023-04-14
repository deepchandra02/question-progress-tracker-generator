# Generate Questions

This script helps you generate question templates for PDF files in the current directory. It supports default question types (CT, ROC, and FR) and allows you to add additional question types as needed. The script creates a text file for each PDF file in the directory with the same name and adds the specified question templates to the text file.

## Prerequisites

- Python 3.x installed on your system.

## Usage

1. Save the `generate_questions.py` script to your computer.
2. Open a terminal (macOS, Linux) or command prompt (Windows) and navigate to the directory containing the PDF files for which you want to generate question templates.
3. Run the script with the command `python generate_questions.py` (Windows) or `./generate_questions.py` (macOS, Linux).
4. Follow the prompts to enter the count of each question type for each PDF file in the directory.

## Example

Assuming you have two PDF files in the directory (`file1.pdf` and `file2.pdf`) and you want to generate the following questions:

- For `file1.pdf`: 2 CT, 1 ROC, 3 FR, 1 SA (additional question type)
- For `file2.pdf`: 1 CT, 2 ROC, 0 FR, 2 Q (additional question type)

After running the script and entering the question counts, it will create two text files (`file1.txt` and `file2.txt`) with the following content:

**file1.txt:**
```
CT1 [TODO]
CT2 [TODO]

ROC1 [TODO]

FR1 [TODO]
FR2 [TODO]
FR3 [TODO]

SA1 [TODO]
```

**file2.txt:**
```
CT1 [TODO]

ROC1 [TODO]
ROC2 [TODO]

Q1 [TODO]
Q2 [TODO]
```

## Global Installation

### macOS and Linux

1. Ensure the shebang line `#!/usr/bin/env python3` exists at the beginning of the `generate_questions.py` script.
2. Rename the script to a command-like name, such as `generate_questions`.
3. Make the script executable:

```sh
chmod +x generate_questions
```

4. Move the script to a directory listed in your `PATH`, such as `/usr/local/bin`:

```sh
sudo mv generate_questions /usr/local/bin/
```


Now you can run the script from any directory by typing `generate_questions` in your terminal.

### Windows

1. Rename the script to `generate_questions.py`.
2. Add the directory containing the script to your system's `Path` environment variable.
- Open the Environment Variables settings on your system (search for "Environment Variables" in the Start menu).
- Find the `Path` variable under "System Variables" and click "Edit."
- Add the path to the directory where the `generate_questions.py` script is located. For example, if the script is located in `C:\scripts`, add `C:\scripts` to the `Path` variable. Click "OK" to save the changes.
3. Move the `generate_questions.py` file to the directory you added to the `Path` variable.

Now you can run the script from any directory by typing `python generate_questions.py` in your command prompt.
