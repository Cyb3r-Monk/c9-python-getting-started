# Managing keys

It's a best practice to store environmental variables outside of the code so that you don't have to modify the code when an environmental variable, for example database connection string, changes.

## Steps
1. Create `.env` file under the project folder.
2. Add `.env` file to the `.gitignore` file
3. Install `python-dotenv` package (in the virtual environment)

Sample code to get environment variables

```python
from dotenv import load_dotenv
load_dotenv()
import os

# PASS is an environment variable defined under the .env file
password = os.getenv('PASS')

print(password)
```