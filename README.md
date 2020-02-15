# docker-for-windows-installation

You need some things before you can fully use the Docker for Windows feature.

1. Install [Git](https://www.atlassian.com/git/tutorials/git-ssh) on Windows if none is currently installed:

2. Run the Git-2.25.0-64-bit.exe using Administration rights.

3. Run these on a cmd terminal or the freshly installed Git Bash

```
git config --global user.name "<Username>"
git config --global user.email "<Email>"
```

4. Now, create a SSH key for your GitHub:

```
ssh-keygen -t rsa -b 4096 -C "<Email>"
```

5. Just press Enter when prompted and you will be able to generate a SSH key.

6. Navigate to your ```.ssh``` directory in ```~<User>/.ssh/```

7. Read the contents of the ssh_rsa.pub file:

```
cat ssh_rsa.pub
```

8. Copy the output starting from the ```ssh_rsa``` ending with the email address that you entered previously.

9. Add this to your Github profile under ```Settings > SSH and GPG Keys```

10. You're done! Nice.
