# PROJECTNAME

## Development environment setup

#### Prerequisites
- Python 3 (>= 3.7 recommended)
- Ruby (2.6.6, see .ruby-version)
- Bundler (2.1.4, see last line of Podfile.lock)
- Xcode (>= 12.1)

#### Setup (or "The 3 steps to awesomeness")

All these steps must be executed from within the root directory of the repository.  
Alternatively, you can run the `setup` script, which runs exactly these 4 steps.

1. Install requirements inside virtualenv:
    ```bash 
    pip install -r requirements.txt
    ```

2. Check the correct ruby version is selected (the one specified in `.ruby-version`) via `ruby --version`, then install
   the ruby depenencies via:
    ```bash
    bundle install
    ```

3. Update hooks directory in local git config
    ```bash
    git config core.hooksPath git_hooks/
    ```

###### This is it! Happy hacking!
