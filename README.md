## Advanced Copy ##

Advanced Copy is a mod for the GNU cp and GNU mv tools which adds a progress
bar and provides some info on what's going on. It was written by Florian Zwicke
and released under the GPL.

This repository exists because the original website
(http://beatex.org/web/advancedcopy.html) appears to be dead. You can still
find it via the Internet Archive:
https://web.archive.org/web/20131115171331/http://beatex.org/web/advancedcopy.html

advcpmv-0.5-8.21.patch was the last patch released by the author (on February
14, 2013). advcpmv-0.6-8.24.patch is simply a rebase of that on top of the 8.24
version of coreutils.

## Build instructions

```
wget http://ftp.gnu.org/gnu/coreutils/coreutils-8.25.tar.xz
tar xvJf coreutils-8.25.tar.xz
cd coreutils-8.25/
wget https://raw.githubusercontent.com/xearonet/advcpmv/master/advcpmv-0.5-8.25.patch
patch -p1 -i advcpmv-0.5-8.25.patch
./configure
make
```
## Usage
Copy bianries to /bin
```
sudo mv ./src/cp /usr/local/bin/gcp
sudo mv ./src/mv /usr/local/bin/gmv
```
and add aliases to ~/.bashrc for your convenience
```
echo alias gcp '/usr/local/bin/gcp -g' >> ~/.bashrc
echo alias gmv '/usr/local/bin/gmv -g' >> ~/.bashrc
```
## Upstream merge
I sent the patch to the team, that maintains the GNU CoreUtils. They won't merge this patch, because mv and cp are feature complete.

