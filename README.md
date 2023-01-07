# L0cky Install Script(LIS)

## Installtion:
On Arch-based distribution as root, run the following:

```
curl -LO https://l0cky.xyz/lis.sh
sh lis.sh
```

You are done!

## What is LIS?

Lis is a auto install script for my dotfile and programs I use almost daily.

LIS can be run on a fresh install of Arch or Artix Linux and provides a full
envorment for you to play around in.


## Customization

You can change what is install on your system by the script by editing progs.csv. By default it will install my [artix rice](https://github.com/Luharion/artixrice.git),but you can easily change this by either modifying the default variables at the
beginning of the script or giving the script one of these options:

- `-r`: custom dotfiles repository (URL)
- `-p`: custom programs list/dependencies (local file or URL)
- `-a`: a custom AUR helper (must be able to install with `-S` unless you
  change the relevant line in the script


### The `progs.csv` list

LIS will parse the given programs list and install all given programs. Note
that the programs file must be a three column `.csv`.
The first column is a "tag" that determines how the program is installed, ""
(blank) for the main repository, `A` for via the AUR or `G` if the program is a
git repository that is meant to be `make && sudo make install`ed.

The second column is the name of the program in the repository, or the link to
the git repository, and the third column is a description (should be a verb
phrase) that describes the program. During installation, LARBS will print out
this information in a grammatical sentence. It also doubles as documentation
for people who read the CSV and want to install my dotfiles manually



### The script itself
The script is based on [LARBS](https://lukesmithxyz/LARBS). So are the programs but I wanted my own script with my own settings. So if you want you could just totally  rid apart this script and make your own.
