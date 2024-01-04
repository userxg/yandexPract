# some bash commands

---

```bash
mv that1 that2 ... **path** - *move something*
cp that1 **path** - *copy sthm*
~ - *homedirectory*
rm -rf - *delete dir with content without questions*
clip **filename** - *to copy content from file in Windows*
```

### by the way
*all fiels about configuration are located in ~/.gitconfig<br>you need to carefully set config to avoid any problems*

# GIT

---

## create repo

```bash
git init - *init repo*
rm -rf ./git *reinit repo*
git add --all or . *from workspace to index all changes in dir* 
git commit -m "something" *commite*
```
## SSH and GITHUB

---

### SSH and its generation

*SSH* - is protocol(there are public and private key)
Public for all to *encrypt* something
Private only for you to *decrypt* smth

---

#### generation SSH

```bash
ls -la ~/.ssh/  - *check ssh generated or not*
ssh-keygen -t ed25519 -C "git email"
 or  - *to generate*
ssh-keygen -t rsa -b 4096 -C "git email"
```
after that you can message
```
>Generating public/private rsa key pair.
and
> Enter a file in which to save the key
- *you can skip just type ENTER twise*
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

check two files

```bash
ls -a ~/.ssh/
(.pub and without extnetion)
```
#### link to github

* open github profile settings **SSH and GPG**
* **New SSH key**
* Don't change anything and paste copied in **Key**
* check key
```bash
ssh -T git@github.com
```

* check link in case you see special message ([this link](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/githubs-ssh-key-fingerprints))

### create repo

* create repo
* copy SSH link
* do cmd
```bash
git remote add origin "*ssh link*"
```
*origin* - is just name of remote server    
```bash
git remote --verbose - *check info*
```

# git log

---

## all commands

* reduced info from g log
```bash
git log --oneline
```
* ...

---

### HEAD

* **HEAD** consist of link to commit that he refers *refs/head/main*
* **HEAD** can be used as a 

### APPROACHES TO SIGN COMMITE

#### Corporative

* **jira id** *number of task* and text *ex*
```bash
git commit -m "LGC-239: corrected sort"
```

#### Convetional commite

* <type>: <message>
```bash
git commit -m "feat: new function"
```
> [more about this approach](https://www.conventionalcommits.org/ru/v1.0.0-beta.4/#спецификация)

