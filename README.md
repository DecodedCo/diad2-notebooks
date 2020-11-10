# diad2-notebooks
DiaD 2.0 Jupyter notebooks and datasets

## Usage
In order to run this notebook locally it is advisable to use a Python 3 [virtual environment](https://realpython.com/python-virtual-environments-a-primer/)
which will manage dependencies and consistency of your Jupyter runtime environment. To set one up, navigate to your 
local root directory for this repository. Once there, run:

```bash
python3 -m venv venv
```

Which will create a new virtual environment named `venv` in the same directory. To activate the virtual environment,
run:

```bash
source venv/bin/activate
```

Which should put `(venv)` on the left of your Terminal command prompt. To check which packages come pre-installed with
a virtual environment, run:

```bash
pip list
``` 

You'll notice a default virtual environment has only the bare minimum installed. To add the necessary dependencies to
run the Jupyter notebooks in this repository from within the virtual environment, run:

```bash
pip install -r requirements.txt
``` 

Which will install the dependencies as listed in the `requirements.txt`. You can then run `pip list` again to
check the necessary dependencies have indeed installed.

One of the dependencies unfortunately also needs some packages installed globally on your machine. To do so, first 
deactivate the virtual environment (technically not required, but good practice), with `deactivate`. Then run:

```bash
brew install graphviz
```

Note that this may take a while if your machine needs to update Homebrew. Once `graphviz` is installed, you can 
reactivate your virtual environment and start Jupyter:

```bash
source venv/bin/activate
jupyter notebook
```

Once the notebook is up and running, it's good practice to run `Kernel` -> `Restart & Clear Output` and then run
`Kernel` -> `Restart & Run All`. Confirm that everything has run as intended and you're good to go for a live demo!