# Password Generator

This project is a Python-based password generator that creates secure passwords and checks if the generated passwords exist in a breach dictionary using the Have I Been Pwned API.

## Features
- **Generate Secure Passwords**: Creates strong passwords based on user-defined parameters (length, number of uppercase letters, lowercase letters, digits, and symbols).
- **Password Breach Check**: Verifies if a password exists in known data breaches using the Have I Been Pwned API to ensure the generated password is safe.
- **Password File Generation**: Allows you to generate and save a list of secure passwords in a `.txt` file.
- **Customizable Default Configuration**: Modify the default settings for password generation (length, number of characters of each type).
  
## How It Works
1. **Password Generation**: 
    - The program generates passwords by combining uppercase letters, lowercase letters, digits, and symbols based on user input or the default configuration.
    - Random characters are chosen from predefined sets and combined to meet the specified requirements.
    
2. **Password Breach Check**:
    - The generated password is hashed using SHA-1 and sent to the "Have I Been Pwned" API to check if it has been compromised in known data breaches.
    - The API response is checked to determine whether the password is safe or compromised.

## Installation

### Dependencies
To use this project, you need to install the following Python libraries:
- `requests`: For making HTTP requests to the "Have I Been Pwned" API.
- `hashlib`: To hash passwords before checking them in the breach database (this is included in Python's standard library).

To install the required dependencies, you can use `pip`:

```bash
pip install requests
```

## Usage

### Main Menu
When you run the program, you'll be presented with a menu of options:
1. **Generate a password**: Generates a secure password using either the default or custom configuration.
2. **Check if a password exists in a dictionary**: Check if a given password is already compromised in known data breaches.
3. **Generate a list of passwords in a text file**: Create a list of passwords and save them in a `.txt` file.
4. **Change default configuration**: Customize the default configuration for password generation.
5. **Exit**: Exit the program.

### Example Output

#### Password Generation
```plaintext
--- Password Generator ---
1. Generate a password
2. Check if a password exists in a dictionary
3. Generate a list of passwords in a text file
4. Change default configuration
5. Exit
Select an option (1-5): 1
Do you want to use the default configuration? (yes/no): yes
Generated password: aB!f9ZkqT%mb72
This password was not found in a data breach. This password is safe!
```

#### Breach Check
```plaintext
Enter the password to check: password123
This password has been found in a data breach!
```

#### Password File Generation
```plaintext
Enter the number of passwords to generate: 5
Password list saved as passwords.txt
```

### Example of `passwords.txt`:
```plaintext
aB!f9ZkqT%mb72
gH3y^2fLz8TbM0
Lw4@Dop5uQe!36
1Fg7xT#hrGp9Lz
M$kpO2Xy8h%Vzq
```

## Contributing
If you wish to contribute to this project, feel free to fork the repository, make improvements, and submit a pull request.

## License
This project is open-source and available for modification and distribution.