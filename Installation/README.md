### How to setup Git

## Add SSH Key

To add a ssh key, first we will need to generate ssh in the local pc

Open the terminal and run the following command

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

To show the key

```
cat ~/.ssh/id_ed25519.pub
```
Adding your SSH key to the ssh-agent
```
eval "$(ssh-agent -s)"
```
Adding Private key to the ssh agent
```
ssh-add ~/.ssh/id_ed25519
```
*Note replace id_ed25519 if you have generated ssh with different names


Open your github account
>Profile > settings > SSH and GPG keys

Click on New SSH keys
> add Title > copy paste the key > Add SSH key

To Test your ssh connection
```
ssh -T git@github.com
```

## To Add User Name and email id 

```
git config --global user.name "Your Username"
```
To Add email id

```
git config --global user.email "youremail@example.com"
```

To verify that your username and email have been set correctly, you can use the following command:

```
git config --global --list
```
