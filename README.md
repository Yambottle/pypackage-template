# pypackage-template
***Drew Yang @ DataJoint*** | ***2021.07.29***

---

This is a customized Cookiecutter python project template that you can generate an inital python project directory structure and common-used files

- Cookiecutter: [Cookiecutter Github](https://github.com/cookiecutter/cookiecutter/tree/1.7.2)
- Reference: [cookiecutter-pypackage](https://github.com/audreyfeldroy/cookiecutter-pypackage), a python Cookiecutter template that managed by Cookiecutter team

---

## Generate a python project
**from github**
```
pip install cookiecutter
cd ~/Projects
cookiecutter git@github.com:Yambottle/pypackage-template.git
# set value to each variable, or skip to use default value
# a python project will be generated at ~/Project/project_name/

# cookiecutter will clone this specified template repo to your user directory's ~/.cookiecutters
```

**from local**
```
pip install cookiecutter
cd ~/Projects
# assume the template exists and it's called ./pypackage-template
cookiecutter ./pypackage-template
# set value to each variable, or skip to use default value
# a python project will be generated at ~/Project/project_name/
```

**context of cookiecutter.json**
```
{
    "author_name":  # author name in setup.py and LICENSE
    "author_email": # author email in setup.py
    "project_name": # uncleaned project name, might contain space or dash
    "project_slug": # please skip, by default automatically replace space or dash in 'project_name' by underscore
    "version":      # version in setup.py
    "open_source_license": # license options that predefined under ~/pypackage_template/{{cookiecutter.project_slug}}/LICENSE
}
```
## Roughly explain
`cookiecutter` cmd will find the `cookiecutter.json` file under the specified template directory whether it's on local or on github, and take each key-value pair as `{variable : default value}`. It will ask you to input a value for each variable to replace the default value. Then, it will use `Jinja` to embed each variable to each file name, folder name or file content that refered it.


If you want to know more details, read this [page](https://cookiecutter.readthedocs.io/en/1.7.2/first_steps.html), it explains the basic logic about how cookiecutter works.