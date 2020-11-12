sudo apt update
sudo apt install -y curl software-properties-common
sudo add-apt-repository -y ppa:neovim-ppa/stable
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
sudo apt update
sudo apt install -y git curl bzip2 build-essential libssl-dev libreadline-dev zlib1g-dev postgresql postgresql-contrib libpq-dev neovim yarn nodejs screen
curl -sLf https://spacevim.org/install.sh | bash
git clone https://github.com/magicmonty/bash-git-prompt.git ~/.bash-git-prompt --depth=1
echo '
if [ -f "$HOME/.bash-git-prompt/gitprompt.sh" ]; then
    GIT_PROMPT_ONLY_IN_REPO=1
    source $HOME/.bash-git-prompt/gitprompt.sh
fi
' > ~/.bashrc
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
cd ~/.rbenv && src/configure && make -C src
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
~/.rbenv/bin/rbenv init
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash
cd ~/.rbenv/plugins/ruby-build
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
. ~/.bashrc
rbenv install ${RUBY-2.7.1}
