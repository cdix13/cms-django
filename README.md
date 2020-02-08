### Basic GitHub Checkout

1. **Run.**

   ```sh
   git clone https://github.com/pyenv/pyenv.git ~/.pyenv
   ```

2. **Define environment variable `PYENV_ROOT`** to point to the path where

   ```sh
   echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
   echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile
   ```

   - **Zsh note**: Modify your `~/.zshrc` file instead of `~/.bash_profile`.
   - **Ubuntu and Fedora note**: Modify your `~/.bashrc` file instead of `~/.bash_profile`.
   - **Proxy note**: If you use a proxy, export `http_proxy` and `HTTPS_PROXY` too.

3. **Add `pyenv init` to your shell** to enable shims and autocompletion.

   ```sh
   echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
   ```

   - **Zsh note**: Modify your `~/.zshrc` file instead of `~/.bash_profile`.
   - **fish note**: Use `pyenv init - | source` instead of `eval (pyenv init -)`.
   - **Ubuntu and Fedora note**: Modify your `~/.bashrc` file instead of `~/.bash_profile`.

4. **Restart your shell so the path changes take effect.**

   ```sh
   exec "$SHELL"
   ```

5. **Install Python build dependencies** before attempting to install a new Python version. The
   [pyenv wiki](https://github.com/pyenv/pyenv/wiki) provides suggested installation packages
   and commands for various operating systems.

6. **Install Python versions into `$(pyenv root)/versions`.**

   ```sh
   pyenv install 3.8.1
   ```

   ```sh
    echo 'export PATH="$(pyenv root)/shims:$PATH"' >> ~/.zshrc
   ```

   \$(pyenv root)/shims:/usr/local/bin:/usr/bin:/bin

### Homebrew on macOS

```sh
 brew update
 brew install pyenv
```

```sh
 brew install pipenv
 sudo apt install pipenv
```
