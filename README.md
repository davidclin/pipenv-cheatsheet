![Banner](https://github.com/davidclin/pipenv-cheatsheet/blob/master/images/pipenv_banner.gif)


## Command Summary

| Operation     | Description |
| ------------- |-------------|
| `pip install pipenv` | Install pipenv on a machine |
| `pipenv --venv` | Check information about initialized venv |
| `pipenv shell` | Activate pipenv |
| `exit` | Disable pipenv |
| `pipenv install` | Generate pipenv based on Pipfile |
| `pipenv install <package_name>` | Install python package |      
| `pipenv install <package_name> --dev` | Install python dev-package |
| `pipenv install -r requirements.txt` | Install python packages from requirements.txt |
| `pipenv install -d` | Install all packages including dev ones |
| `pipenv update` | Update all installed packages |
| `pipenv update -d` | Update all installed packages including dev ones |
| `pipenv uninstall <package_name>` | Delete python package from pipenv |
| `pipenv uninstall --all` | Delete all python packages from pipenv |
| `pipenv graph` | Show packages dependency graph |    
| `pipenv check` | Check for security vulnerabilities and PEP asserts of installed packages |  
| `pipenv lock` | Generate lock file |
| `pipenv lock -r` | Display all installed python packages |
| `pipenv --rm` | Delete installed pipenv |
| `pipenv run <command>` | Execute `command` from pipenv not activating it |


## Tips
If you need to change the Python version in your pipenv, simply update **python_version** in the Pipfile then reinitialize pipenv using  `pipenv --python <typed version>`.

To check whether you need to update packages for say known vulnerabilities, type `pipenv check`.
Then change to the appropriate version number for packages specified in the output of `pipenv check` in your Pipfile and type `pipenv install` in your command line.

You can also bake in environment variables by creating an **.env** file within your pipenv root directory. Just remember to add the file to **.gitignore** so as not to expose any sensitive information such as passwords/tokens/etc.


## Learn More
[Official pypi.org pipenv Project](https://pypi.org/project/pipenv/)<br>
[PipEnv: A Guide to the New Python Packaging Tool](https://realpython.com/pipenv-guide/)<br>
[YouTube: Easily Manage Packages and Virtual Envinronments](https://www.youtube.com/watch?v=zDYL22QNiWk)
