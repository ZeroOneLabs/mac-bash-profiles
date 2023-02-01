# mac-bash-profiles
A collection of some bash profiles, aliases, and functions.

## How to install

```bash
# - - - - Optional - - - - #
# Create directory to download files
mkdir ~/Repos/

# Change to new directory 
cd ~/Repos/
# - - - -/Optional - - - - #

# Clone this repo
git clone https://github.com/ZeroOneLabs/mac-bash-profiles.git .

cd mac-bash-profiles

cp profiles/aliases ~/.bash_aliases
cp profiles/exports ~/.bash_exports

# Add alias source IF block to main Bash profile
cat << EOF >> ~/.bash_profile
if [ -f ~/.bash_aliases ];then
    source ~/.bash_aliases
fi
EOF 

# Add export source IF block to main Bash profile
cat << EOF >> ~/.bash_profile
if [ -f ~/.bash_exports ];then
    source ~/.bash_exports
fi
EOF 

source ~/.bash_profile
```


