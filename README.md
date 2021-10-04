# Loan Qualifier App
## Project Overview

The python application works by calcualting if a lender will allow a loan knowing a few key questions. The 'daily_rate_sheet.csv' file is where lender information is stored and pulled from the application to calculate if loans qualify. 

---

## Technologies

Describe the technologies required to use your project such as programming languages, libraries, frameworks, and operating systems. Be sure to include the specific versions of any critical dependencies that you have used in the stable version of your project.

The application is in python and is uing the following libraries:

* [fire](https://github.com/google/python-fire) - For the command line interface, help page, and entrypoint.

* [questionary](https://github.com/tmbo/questionary) - For interactive user prompts and dialogs

* [Path](https://github.com/jaraco/path) - For relative and absolute path to the file

The operating system used in creating the application is Windows 10 64 bit. The application that used to code in python is visual studio and then tested in Gitbash and Terminal. 

The application is depend on qualidfier which are placed in submodules. Filters is where qualifiers are placed which inculdes credit_score.py, debt_to_income.py, loan_to_value.py, max_loan_size.py. Utils inculdes the calculator for the application and file input and putput python file. 

The output file was edited to inculde save_csv function as illustrated below:

```python
    def save_csv(csvpath, data, header=None):
        with open(output_path, "w", newline='') as csvfile:
            csvwriter = csv.writer(csvfile, delimiter=',')
            if header:
                csvwriter.writerow(header)
            csvwriter.writerow(data)
```
---

## Installation Guide

1. Open Gitbach or termianl and go ito the folder where you want to place the files.
2. Click on the blue "code" button which will allow you to clone.
![<Code button in Github>]()
3. Then click on SSH or HTTPS as a clone method depending on if you have the SSH key setup. You will copy the link. You will then type "git clone" in Gitback or Terminal. Then paste the ssh or https information and press enter.
4. Next type "git pull" command in Temrianl or GitBash to pull the repository from the remote Github repository to a local directory on your computer.
5. You have access to the application (app.py). Also there will be all the python files that the application is depended on,  plus the excel file. 

---

## Usage

1. After installing app.py and other files you want to test the file by typing "python app.py" in GitBash or Terminal. 
2. After that you will answer in the CLI about file path to the daily_rate_sheet, credit score, debt, income, loan amount and home value.
![<Git Run Command and Prompts>]()
3. The app will calcualte your debt-to-income ratio, which will in turn calculate how many loans you qualify for.
4. If you don't qalify for any lonas, appication will notify you before exiting: Sorry! You have no qualifying loans.:(
5. If you qualify for a loan(s) form the calulation, you then have the oppuntrunity to save the infromation.  
6. If you select YES, application will prompt you to choose a filename. This is the file that has bank information and how each bank is willing to loan out.
7. If you select an invalid filename, application will notify you before exiting: Opps! Can't find the path:...
8. If you select NO, the application will exit. 

---

## Contributors

This application was provided by the instrutor of Columbia University and addtioanl code was added by Khatija Azeem to complete the project.

---

## License

For this application, I used Github to uplaod the file into a repository. Since this is a public file, there will be no restriction on usage of this code. 
