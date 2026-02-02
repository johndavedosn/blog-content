+++
date = '2026-02-01T14:48:06+01:00'
draft = false
title = 'MPC - P2'
+++

# Section 1: Setup.

Before we get into writing our lovely, juicy code. We need to set our programming environment up so that we have everything we need to write, run, and test our code properly. The setup process will not be explained much in detail as it is assumed that you have some basic knowledge of how to use a computer (as specified in the previous post).

### 1.1: The code editor.

Code editors are pieces of software used to...well...write and edit code. There are numerous code editors out there, but I'm going to mainly focus on two for this course :

* [**JetBrains PyCharm:**](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.jetbrains.com/pycharm/&ved=2ahUKEwiD5_jauLiSAxWlV6QEHWdZLzEQFnoECAwQAQ&usg=AOvVaw08gOuiX9h_nAkWJhXYmZeT) This is a complete set of development tools for the Python programming language. In programming terms, it is called an IDE (Integrated Development Environment). I highly recommend this one as it is ready out-of-the-box and requires no setup whatsoever.
* [**Visual studio code (VScode)**](http://code.visualstudio.com/): Developed and maintained by Microsoft. This is a very popular and widely known code general purpose code editor. It requires a little bit of setup for Python but it is generally pretty intuitive and easy to use.

For VScode, you have to get the Python Extension Pack from the extensions tab on the left side. Click on the extensions tab, and then search for "Python" in the top, scroll down until you find the needed extension and click it, then click install.

After the pack installs, you're gonna be ready to write, test, and run Python code on your editor. Not yet, however. We're gonna have to first install the Python interpreter (as specified in the previous post, this is the program that executes your code).

### 1.2: The interpreter.

Go to [Python.org](https://python.org), and download and install the latest Python version for your operating system. The installation process should be pretty straightforward. If I remember correctly, it is as simple as clicking "Next" through the installer in Windows.

**Important note:** Make sure to add Python to your PATH. If you don't, VScode and other text editors will not be able to even see it.

* **For Windows**: It is as simple as checking "Add Python to PATH" in the installer. 
* **For Linux & MacOS**: Depending on your shell, you might have to edit your ``PATH`` variable manually: 
```sh 
export $PATH="$PATH:<PYTHON PATH>" # for Bash and Zsh.
```

```sh 
set -Ux $PATH PATH <PYTHON PATH> # for Fish.
``` 

Replace ``PYTHON PATH`` with the path to your Python installation.

### 1.3: Testing that your setup works - The Hello World.

In order to test that everything works properly, create a folder somewhere to house your code. In VScode, click on "File" in the top menu (it might be hidden under a little menu button on the top left if you're zoomed in), and click "Open Folder", then select the folder you just created.

In the Explorer tab in the sidebar, and near the folder's name, you're gonna see four little icons if you hover over it. The first one shows "New File" if you hover over it, click on that.

Name your file anything, but **make sure** to add the ``.py`` extension at the end of the name. So, if your file is gonna be called ``mycode``, name it ``mycode.py``. This is required for both VScode and the Python interpreter to recognize the file.

An editor should appear in the main middle section of VScode, with a blinking cursor and a line number. Type the following:

```py
print("Hello, World!")
```

(**Note**: VScode should provide suggestions when you start typing "print", press Tab in order to let it auto-complete for you, it also will auto-close parantheses and quotation marks by default).

In the top right corner, there should be a small green triangle button. This is your "run" button, which tells VScode to ~~run away~~ execute your code, click on it. A section should appear below with a lot of text in it. But it should say "Hello, World!"

Congratulations! If everything worked correctly, you have wrote and ran your first piece of code ever! 🥳🥳

Go drink something, have a snack, and feel good about yourself!