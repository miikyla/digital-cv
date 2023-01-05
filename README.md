# digital-cv
Digital CV for Mikyla Peters

## Step-by-step Process

> Docker image for the following steps can be found at: 


1. Do the required setup depending on the operating system you're running 
<details>
<summary>Windows Setup</summary>
1. Install and configure WSL2 
Follow the instructions found at:
https://learn.microsoft.com/en-us/windows/wsl/install

2. Install Ubuntu in WSL2
Follow the instructions found at:
https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10

I had issues running ```jekyll new``` in Ubuntu 22.04, which is apparently due to an incompatibility with the Brightbox Personal Package Archive and Ubuntu 22.04 (according to https://levelup.gitconnected.com/how-to-install-jekyll-on-wsl-2-13c3b285d513)


3. Install Ruby
Follow the instructions found at:
https://gorails.com/setup/ubuntu/20.04

NOTE: When I did this I had issues with an error on jekyll serve that was due to an unsupported version of Ruby (3.2.0). I had to end up doing a version update using ```gem update --system``` to get this to work

4. Install Jekyll
Follow the instructions found at:
https://jekyllrb.com/docs/installation/ubuntu/

5. Install the Jekyll Gem
NOTE: GitHub pages is only able to support a certain version of jekyll, need to reference the GitHub dependencies page to see which version to install:
https://pages.github.com/versions/ . Thanks to https://www.vgemba.net/blog/Setup-Jekyll-WSL/ for pointing this out.
```
gem install jekyll --version 3.9.2
```
</details>

<br>
2. Open the terminal (WSL for Windows, Terminal for Linux), and enter the following commands into the terminal

```
# Change to your desired directory, I'm just going to use my home directory (but feel free to mount your C:/ drive if you're using WSL)
cd ~

# Create a new Jekyll website
jekyll new digital-cv

# Move into the newly created folder
cd digital-cv

# Run the website locally
jekyll serve
```
3. Open the new website by navigating to ```http://localhost:4000/``` in a browser.

