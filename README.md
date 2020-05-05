# home

## Update

```
sudo apt update
sudo apt upgrade
```

## Network transfer

### [cURL](https://curl.haxx.se/)

```
sudo apt install curl
```

### [Wget](https://www.gnu.org/software/wget/)

```
sudo apt install wget
```

## Terminal

Using [Bash](https://www.gnu.org/software/bash/).

### [Oh-my-bash](https://ohmybash.github.io/)

```
sh -c "$(curl -fsSL )://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```
or
```
sh -c "$(wget https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh -O -)"
```

Add aliases from https://github.com/quibaritaenperdresatrompe/dotfiles/aliases/ in `~/.oh-my-bash/custom/aliases/`.

### [Robbyrussell theme](https://github.com/denysdovhan/robbyrussell-node)

n.b. `npm` is required see [`nvm`](#nvm)

```
npm install -g robbyrussell
```

## Development

### Version your code with [Git](https://git-scm.com/)

```
apt-get install git
```

### Use multiple version of NodeJS with [`nvm`](https://github.com/nvm-sh/nvm)

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```
or
```
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

### Manage your npm packages with [Yarn](https://classic.yarnpkg.com/)

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```

Because we use `nvm` it's recommended to avoid npm install :
```
sudo apt update && sudo apt install --no-install-recommends yarn
```

Add this alias (in `~/.oh-my-bash/custom/aliases/productivity.aliases.sh`) :
```
alias node=nodejs
```

To use it globally add it to the PATH :
```
export PATH="$PATH:`yarn global bin`"
```

### Edit with [Visual Studio Code](https://code.visualstudio.com/)

Download [.deb package](https://code.visualstudio.com/Download).

### Create nice commit messages with [`git-cz`](https://www.npmjs.com/package/git-cz)

```
yarn global add git-cz
```
