# python-josso-auth 0.1.0

```python-josso-auth``` provides a ```JOSSOAuth``` authentication for ```python-social-auth``` which you subclass
to add JOSSO providers as social auth options. To use, just create a class for your provider which extends 
```JOSSOAuth``` and provide a name and base URL.

```python
from josso.backend import JOSSOAuth

class ExampleJOSSOProvider(JOSSOAuth):
    name = 'example_josso'
    base_url = 'https://example.com/josso/'
```

Now you can include your backend in your settings. For example, with Django:
 ```python
AUTHENTICATION_BACKENS += ('myapp.backends.ExampleJOSSOProvider',) 
 ```

# Install

```bash
$ pip install https://github.com/consbio/python-josso-auth/archive/0.1.0.tar.gz
```