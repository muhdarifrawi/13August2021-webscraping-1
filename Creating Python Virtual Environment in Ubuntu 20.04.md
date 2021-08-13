# Creating Python Virtual Environment in Ubuntu 20.04

### Source

https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-programming-environment-on-ubuntu-20-04-quickstart

## Directions

### 1. Update and Upgrade

Ensure that your shipped version of Python 3 is up-to-date. Run the following codes:

```bash
$ sudo apt update
$ sudo apt -y upgrade
```

Confirm installation if prompted.

### 2. Check version of Python

Check which version of Python 3 is installed:

```bash
$ python3 -V
```

Check that it is the current version of Python 3 that you want.

### 3. Install pip

Use the following command:

```bash
$ sudo apt install -y python3-pip
```

You can start installing python packages with the following command once pip is installed:

```bash
$ pip3 install <package name>
```

### 4. Install Additional Tools 

This would ensure that the Python code can be organised and compiled properly:

```bash
$ sudo apt install build-essential libssl-dev libffi-dev python3-dev

```

### 5. Install venv

Install with the following command:

```bash
$ sudo apt install -y python3-venv
```

### 6. Creating Virtual Environment 

Type in the following to create python venv:

``` bash
$ python3 -m venv <venv name here, example "django-venv">
```

### 7. Activating Virtual Environment

To activate, type the following command:

```bash
$ source <your venv name here>/bin/activate
```



Your terminal should now be prefixed with the environment name:

```bash
(your venv name here) user@user-K52F:~$
```

### 8. Testing and Using the Virtual Environment

Note that in the virtual environment, you can use the command `python` instead of `python3` and `pip` instead of `pip3`.

To bring up the python interpreter, type in the following command:

```bash
(your venv name here) user@user-K52F:~$ python
```

Something like this should come up:

```python
Python 3.8.2 (default, Mar 13 2020, 10:14:16) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

You can try putting something simple like `print("hello world")` to see if the interpreter is working. 

To quit the interpreter, simply key in:

```python
>>> quit()
```

### 9. Deactivating Virtual Environment

To exit and deactivate the virtual environment, key in the following command:

```bash
(your venv name here) user@user-K52F:~$ deactivate
```

## Additional Notes

###  Locating Venv

If you are using Ubuntu and need to look for your virtual environments, use this command provided by [Bhupesh Varshney](https://stackoverflow.com/users/8209510/bhupesh-varshney) on [Stack Overflow](https://stackoverflow.com/a/62607798).

``` bash
locate -b '\activate' | grep "/home"
```

However before this, you would need to install the `mlocate` package.

```bash
sudo apt install mlocate
```

### Removing Venv

##### Source: [How do I remove/delete a virtualenv](https://stackoverflow.com/questions/11005457/how-do-i-remove-delete-a-virtualenv)

```bash
sudo rm -rf <venv-name>
```



