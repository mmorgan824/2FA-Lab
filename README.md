In this lab we will create 2FA using Ubuntu.

Step 1, update the system. On your Ubuntu VM open terminal and run sudo apt update && sudo apt upgrade -y. This updates your system's package list and upgrades any outdated packages. It ensures you're working with the most secure and stable versions of software. Always update your system before installing anything new to avoid conflicts or bugs. 
![image](https://github.com/user-attachments/assets/77dcdfba-48c0-432e-94f7-33d2e9c6986e)

Step 2, install OpenSSH Server and Google Authenticator PAM Module. The OpenSSH server allows your system to accept SSH logins. The Google Authenticator module lets Linux use two-factor authentication (2FA) based on time-generated codes. Together, these tools help you lock down your system with stronger login security.
![image](https://github.com/user-attachments/assets/9b767a51-8de6-4b9d-bc0c-6b68277ac6bd)
![Install authenticator](https://github.com/user-attachments/assets/4fff95b2-3171-4469-ad85-7c398c9b4742)

Step 3, run google-authenticator. This command generates a QR code and secret key for 2FA. You scan the code with the Google Authenticator app, which then generates 6-digit login codes every 30 seconds. Answer “yes” to all prompts to enable extra security options like scratch codes and rate-limiting.
![Run google-authenticator](https://github.com/user-attachments/assets/94ae0e4a-2194-471a-95e6-199d01829eeb)

Step 4, configure PAM to require 2FA for SSH. 
![pam d sshd](https://github.com/user-attachments/assets/cc99563c-2459-4894-a62c-0b0cda0f33d1)

Step 5, enable 2FA in SSH Config.
![Screenshot 2025-06-21 001858](https://github.com/user-attachments/assets/253789a4-0c82-42f0-86cc-64faaefa6ccc)

Step 6, restart SSH to apply and save changes.
![sudo systemctl restart](https://github.com/user-attachments/assets/e2c83eb6-3c66-4473-bccf-2e2895bbbc92)

Step 7, test SSH login with 2FA.
![verification code and password](https://github.com/user-attachments/assets/85928796-f472-4e53-91e1-c2ed288a71a7)
![Remoting in Ubuntu](https://github.com/user-attachments/assets/3301c4bb-696e-459f-88bb-a1d20241a062)
