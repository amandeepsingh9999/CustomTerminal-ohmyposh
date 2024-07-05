# CustomTerminal-ohmyposh
> This Installation is only for linux if you wanna know about your os just comment .

## To Install Oh My Posh , Follow these:
1. Install .NET SDK, 
OhMyPosh is built on .NET 

```
sudo apt update
sudo apt install -y dotnet-sdk-6.0
```

2. Now Download and Install OhMyPosh 
```
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh

```

3. Configure your shell with OhMyPosh\
If you are using Bash Follow this :
```
echo 'eval "$(oh-my-posh init bash)"' >> ~/.bashrc
source ~/.bashrc
```
If you are using Zsh follow this :
```
echo 'eval "$(oh-my-posh init zsh)"' >> ~/.zshrc
source ~/.zshrc
```
4. Because oh-my-posh does not have any config file we will create one 
```
mkdir .config/ohmyposh
cd .config/ohmyposh
```
5. Now we will import the base configuration 
```
oh-my-posh config export --output ./base.json
```
6. You can say that it is the final step but there more<br>
Now you will open neovim or your favorite text editor 
```
nvim .zshrc
```
Now we will edit the line we have added in the step - 3 and make it look like something like this
```
eval "$(oh-my-posh init zsh --config $HOME/.config/ohmyposh/base.json)"
```
escape the neovim using `Esc` key and then pressing `:wq`

# Now how will you be able to choose theme for your terminal 

For first thing when you open your terminal you will be greeted with new terminal theme


![alt](Assets/Images/Screenshot_05-Jul_22-53-40_23117.png)

Now i will tell you that how you can change yours first Go to this link and select any theme you like 

[Terminal theme](https://ohmyposh.dev/docs/themes)

then tap on its name to go to its github page and copy the json text of your suitable theme , now open `.config/ohmyposh/base.json` select all text and delete it then paste what you have copied in that file then jsut run this command so that it can apply to your terminal

```
source .zshrc
```