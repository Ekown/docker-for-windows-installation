You need some things before you can fully use the Docker for Windows feature.

Install Git on Windows (if none is currently installed) <https://www.atlassian.com/git/tutorials/git-ssh>:
1. Run the Git-2.25.0-64-bit.exe using Administration rights.
2. Run these on a cmd terminal or the freshly installed Git Bash
git config --global user.name "<Username>"
git config --global user.email "<Email>"
3. Now, create a SSH key for your GitHub:
ssh-keygen -t rsa -b 4096 -C "<Email>"
4. Just press Enter when prompted and you will be able to generate a SSH key.
5. Navigate to your .ssh directory in ~<User>/.ssh/
6. Read the contents of the ssh_rsa.pub file:
cat ssh_rsa.pub
7. Copy the output starting from the "ssh_rsa" ending with the email address that you entered previously.
8. Add this to your Github profile under Settings > SSH and GPG Keys
9. You're done! Nice.