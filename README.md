# Automated Blind SQL Injection

## Objective  
Simulate an automated blind SQL injection attack to extract password hashes from a vulnerable web application by leveraging conditional logic, character enumeration, and payload injection.

## Skills Learned

- **Blind SQL Injection Techniques**: Crafted payloads to infer information without directly viewing the results, using boolean-based logic.
- **Web Exploitation Automation**: Built a fully automated script to extract password hashes by interacting with a login form.
- **Payload Engineering**: Constructed SQL payloads for substring extraction, length checking, and character comparison.
- **Python Scripting**: Used Python functions and control flow to structure a modular and interactive attack script.
- **Data Exfiltration via Response Timing**: Detected successful injection paths by parsing the absence/presence of specific strings in HTTP responses.

## Tools Used

- **Python 3**: Primary language for scripting the injection logic.
- **Requests**: HTTP client library to send POST requests to the target application.
- **Kali Linux CLI**: Used as the runtime environment for launching the script.
- **Vulnerable Web App**: Test environment to simulate the attack.

## Steps

1. Define the target URL and the keyword (`"Welcome back"`) that indicates a successful login.
2. Send crafted SQL injection payloads via the username field using a POST request.
3. Determine if a user ID is valid by testing for existence.
4. Measure the password length using repeated queries with increasing values.
5. Extract each character of the password hash by testing one hex character at a time (`0-9`, `a-f`).
6. Store and return the full hash once all characters are found.
7. Print the total number of queries used for insight into attack efficiency.

<img width="1529" height="1294" alt="image" src="https://github.com/user-attachments/assets/cc73d032-5d83-4c16-91c1-9d7c9396e443" />

When entering a character with a quote:

<img width="538" height="232" alt="image" src="https://github.com/user-attachments/assets/6ebc74fd-b629-4f47-b409-8371e86d0569" />

Finding the number of users registered in the application and length of their password:

<img width="1186" height="599" alt="image" src="https://github.com/user-attachments/assets/522afaf3-8758-49bf-ba26-ea7e7d9121d0" />

⚠️ Note: This script is for educational and ethical penetration testing purposes only, and should not be used against any system without explicit authorization.
