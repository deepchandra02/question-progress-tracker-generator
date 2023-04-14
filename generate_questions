#!/usr/bin/env python3

import os
import glob

def create_question_file(file_name, question_counts):
    with open(file_name, 'w') as file:
        for question_type, count in question_counts.items():
            for i in range(1, count + 1):
                file.write(f"{question_type}{i} [TODO]\n")
            
            file.write(f"\n")

    print(f"Questions saved to {file_name}")

def main():
    pdf_files = glob.glob("*.pdf")

    if not pdf_files:
        print("No PDF files found in the current directory.")
        return

    for pdf_file in pdf_files:
        text_file = os.path.splitext(pdf_file)[0] + '.txt'

        if os.path.exists(text_file):
            print(f"{text_file} already exists. Skipping {pdf_file}.")
            continue

        question_counts = {}
        print(f"Enter the count of questions for {pdf_file}:")

        default_types = ['CT', 'ROC', 'FR']
        for question_type in default_types:
            question_counts[question_type] = int(input(f"{question_type}: "))

        while True:
            additional_question_type = input("Enter additional question type or 'q' to finish: ").strip()
            if additional_question_type.lower() == 'q':
                break
            additional_question_count = int(input(f"Enter the count for {additional_question_type}: "))
            question_counts[additional_question_type] = additional_question_count

        create_question_file(text_file, question_counts)

if __name__ == "__main__":
    main()
