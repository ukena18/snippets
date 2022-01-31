# customuser

#
#this is using custom user from abstractUser model 
# and then on the settings.py file you are specifed  

```python
#we do have base app
AUTH_USER_MODEL = "base.User"
```

## Usage

```python
from django.contrib.auth.models import AbstractUser

class User(AbstractUser):
    name = models.CharField(max_length=200,null=True)
    email = models.EmailField(unique=True,null=True)
    bio = models.TextField(null=True)
#it is specied make sure use email instead of email
    USERNAME_FIELD = "email"
    REQUIRED_FIELDS = []

```
