# Python

We are using Brew installed Python for the global level of Python tasks i.e. anywhere on the Mac not specific to a project/repo. For project/repo specific install and build process, refer to the [Conda](#conda) section.

| Language Versioner | .zshrc Needed | Language Version | Alias Needed | Install & Build Tool |
| ------------------ | ------------- | ---------------- | ------------ | -------------------- |
| Brew               | No            | Brew             | No           | N/A                  |

## Globally Available Python

### List out what versions of Python are available to install

The trailing dot/period is needed to narrow down just to Python packages.

```bash
brew search python@3.
```

### List the current version of Python that is set for use

- Outside of a Conda env, we are not using an alias and require the full `python3` naming convention. This is because the .zshrc file's alias and the conda environment's alias clash.

```bash
python3 --version
```

### Update current Python version to latest i.e. Python released some patches

```bash
brew upgrade
```

### Install a different version of Python then the latest

```bash
brew install python@3.XX
```

## Conda

| Language Versioner | .zshrc Needed      | Language Version | Alias Needed | Install & Build Tool |
| ------------------ | ------------------ | ---------------- | ------------ | -------------------- |
| Conda              | No, see note below | Conda commands   | No           | TBD                  |

**_NOTE:_** .zshrc is modified during the initial Conda installation/init process. It is not adjusted afterwards.

### Update Conda to the latest version

```bash
conda --version
conda update conda
conda --version
```

### List out what versions of Python are available

```bash
conda search python
```

### Environments

### Create and activate a Conda environment

Using aliases

```bash
condac
condaa
```

Using the commands behind the above aliases

```bash
conda create -p venv/ python=3.13
conda activate venv/
```

### Creating a replicable environment

Saving the dependencies of an activated environment

```bash
conda env export --prefix ./venv > environment.yml
```

Instantiating an environment from an environment file

```bash
conda env create --prefix ./venv -f environment.yml
```

### Updating (read upgrading minor version) python within an active Conda environment

**_NOTE:_** The specific environment will need to be activated first.

This will take the Python version all the way to the highest supported within that environment i.e. if current version is 3.10, the below command will take the Python version up to 3.13

```bash
conda update python
```

### Upgrading (read upgrading patch version) python within an active Conda environment

**_NOTE:_** The specific environment will need to be activated first.

This will take the Python version all the way to the highest patched version within that environment i.e. if current version is 3.13.0, the below command will take the Python version up to 3.13.X

```bash
conda install python=3.13
```
