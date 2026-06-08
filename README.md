# Python-Security-Scripts
File: password_strength_checker.py
  def check_password(password):
    score = 0

    if len(password) >= 8:
        score += 1

    if any(char.isupper() for char in password):
        score += 1

    if any(char.islower() for char in password):
        score += 1

    if any(char.isdigit() for char in password):
        score += 1

    if any(not char.isalnum() for char in password):
        score += 1

    if score <= 2:
        print("Weak Password")
    elif score <= 4:
        print("Medium Password")
    else:
        print("Strong Password")

password = input("Enter Password: ")
check_password(password)

File: file_hash_generator.py
  import hashlib

filename = input("Enter file name: ")

with open(filename, "rb") as file:
    data = file.read()

hash_value = hashlib.sha256(data).hexdigest()

print("SHA256 Hash:")
print(hash_value)


## About

A collection of beginner-friendly cybersecurity scripts written in Python.

## Scripts

### Password Strength Checker
Checks the strength of a password.

### File Hash Generator
Generates SHA-256 hashes for files.

## Technologies Used

- Python

## Future Plans

- Port Scanner
- Network Scanner
- Log Analyzer
- Password Generator

## Author

Lasya Kalangi
