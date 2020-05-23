# chrke

A simple tool to download rke and also change the current version of it

## Usage

Download the script:

```bash
$ curl -O https://raw.githubusercontent.com/siavashoutadi/chrke/master/chrke
```

See usage:

```bash
$ bash chrke
usage: chrke OPTIONS RKE_VERSION

options:
 install        Installs requested rke version if it isn't installed yet.
                Example: chrke install v1.1.1

 list           Display alias commands to easily switch between different
                version of rke.
                Example: chrke list v1.1.1
```

Install rke v1.1.1:

```bash
$ bash chrke install v1.1.1
rke version v1.1.1
rke is installed successfully!
alias rke=/home/siavash/.chrke/bin/rke-v1.1.1

$ alias rke=/home/siavash/.chrke/bin/rke-v1.1.1
$ rke --version
rke version v1.1.1
```

Use the alias to swith the rke version:

```bash
$ alias rke=/home/siavash/.chrke/bin/rke-v1.1.1
$ rke --version
rke version v1.1.1
```

List aliases for all available rke versions:

```bash
$ bash chrke list
alias rke=/home/siavash/.chrke/bin/rke-v1.1.0
alias rke=/home/siavash/.chrke/bin/rke-v1.1.1

$ alias rke=/home/siavash/.chrke/bin/rke-v1.1.1
$ rke --version
rke version v1.1.1

$ alias rke=/home/siavash/.chrke/bin/rke-v1.1.0
$ rke --version
rke version v1.1.0
```

Move chrke to a directory in PATH for easier access:

```bash
$ chmod +x chrke
$ sudo mv chrke /usr/local/bin/
$ chrke list
alias rke=/home/siavash/.chrke/bin/rke-v1.1.0
alias rke=/home/siavash/.chrke/bin/rke-v1.1.1
```
