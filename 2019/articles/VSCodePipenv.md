# How to use Pipenv with Jupyter and VSCode

[<img src="XXXXXXXX">](
httpsasdfafasfasfdasf)
xxxxxxx - httpsasdfafasfasfdasf


Currently I study Artificial Intelligence at the JKU university and for some exercises we need to use jupyter notebooks. Having worked a little bit with Python the package manager "pipenv" proof to be valuable. Now, I encountered some problems using it with jupyter notebooks and within vscode. Therefore, a short guide on how I solved it.

## Table of Contents

##

As I described in my last article [Working with Jupyter and VSCode](https://towardsdatascience.com/working-with-vscode-and-jupyter-notebook-style-5ecaf47f9f84) I use pyenv and pipenv for managing all packages in my python development. I also referenced some articles why this way is helpful and easy to use.
Now we hve to dive a little more into it. There are 2 ways you would want to develop with jupyter notebook. Either you work with it directly in the browser or inside VSCode. In both use cases there emerge problems. And this is the way I worked around it.


## Developing with Jupyter Notebook in the browser

Let's say you already have the proper python environment on your system and now you want to create a specific one for a project.

First, create the Pipenv environment.
Make sure to navigate into the correct directory.
Use `pipenv install <packages>` to install all your packages.
Then use `pipenv shell` to activate your shell.
Then use `pipenv install jupyter` and afterwards `pipenv run jupyter notebook`.

Now the jupyter server is started and your notebook will have access to the correct environment.

![recodring of workflow](http://g.recordit.co/TKgvPApDuF.gif)

## Develop with Jupyter Notebook in VSCode

Now for the workflow within VSCode.
Here it is import to be aware of the different shells. I often use a separate terminal (iterm2) and sometimes an activated shell is not recognized by VSCode. Therefore the workflow is as follows:


First, create the Pipenv environment.
Make sure to navigate into the correct directory.
Use `pipenv install <packages>` to install all your packages.

Then, be sure to have a proper settings file in your vscode folder with content like this:

```json
{
    "python.venvPath": "${workspaceFolder}/.venv/bin/python",
    "python.pythonPath": ".venv/bin/python",
}
```
Afterwards you can choose the proper python environment within VSCode. ( It should be the one created with pipenv!)
Now the correct environment is recognized for python files.
Afterwards to work with jupyter notebook style in VSCode, you need to open the VSCode terminal and run `pipenv shell` to activate the shell.

Now, after opening the .ipynb file, you will be able to run the cells and not get the error "... was not able to start jupyter server in environment xxx"






---

## About

I consider myself a problem solver. My strengths are to navigate in complex environments, provide solutions and breaking them down.
My knowledge and interests evolve around business law and programming machine learning applications.
I provide services in building data analysis and evaluating business-related concepts.

Connect on:
- [LinkedIn](https://www.linkedin.com/in/createdd)
- [Github](https://github.com/Createdd)
- [Medium](https://medium.com/@createdd)
- [Twitter](https://twitter.com/_createdd)
- [Patreon](https://www.patreon.com/createdd)
- [Instagram](https://www.instagram.com/create.dd/)

## Support and Mails

[![supportPatreon](../../patreonImg.png)](https://www.patreon.com/createdd)
https://www.patreon.com/createdd

https://upscri.be/481d76

<!-- Written by Daniel Deutsch -->