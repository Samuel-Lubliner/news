# Newspaper website

## Set up

```shell
$ cd ~/desktop/code
$ mkdir news
$ cd news
$ python3 -m venv .venv
$ source .venv/bin/activate
(.venv) $

(.venv) $ python -m pip install django~=4.2.0
(.venv) $ python -m pip install black
(.venv) $ django-admin startproject django_project .
(.venv) $ python manage.py startapp accounts
```

- Add `.gitignore`
- Initialize repository
- Migrate after creating custom user model

## [Custom User Model](https://docs.djangoproject.com/en/4.2/topics/auth/customizing/#using-a-custom-user-model-when-starting-a-project)

- For simplicity use AbstractUser.
- For more control, create a custom user model with AbstractBaseUser.

Steps to creating custom user model:

- update `django_project/settings.py`
- create a new `CustomUsermodel`
- create new forms for `UserCreationForm` and `UserChangeForm`
- update `accounts/admin.py`
