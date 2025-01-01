# Python

We are using a combination of Brew installed Python for the global level of Python tasks i.e. anywhere on the Mac not specific to a project/repo. For project/repo specific install and build process, refer to the [Conda](#conda) section.

| Language Versioner | .zshrc Needed | Language Version | Alias Needed | Install & Build Tool |
| ------------------ | ------------- | ---------------- | ------------ | -------------------- |
| Brew and .zshrc    | Yes           | Brew             | Yes          | N/A                  |

## Globally Available Python

### List out what versions of Python are available to install

The trailing dot/period is needed to narrow down just to Python packages.

```bash
brew search python@3.
```

### List the current version of Python that is set for use

- Outside of a Conda env, this is set with an alias in the .zshrc file and Brew Python dependencies

```bash
python --version
```

### Update current Python version to latest i.e. Python released some patches

```bash
brew upgrade
```

### Install a different version of Python then the latest

```bash
brew install python@3.XX
```

Complete the below section afterwards

### Use or switch an installed version of Python

```bash
openzshrc
```

Change the alias for pip and Python to point to the version you are wanting

```bash
sourcezshrc
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

### Create and activate a Conda environment

```bash
conda create -n your-env-name python=3.X
conda activate your-env-name
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
