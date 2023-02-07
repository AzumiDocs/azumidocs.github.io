# Azumi Guide

### Extending from Azumi

This section of the guide will show you how to create a bot extension from Azumi. This will allow you to run your own instance of Azumi.


#### Requirements

- IDE / Code Editor / Notepad
- A copy of Azumi's source code. (There must be a clear and valid reason in your application for receiving source code. Source code is currently not available to non-developers.)
- Basic Python object knowledge.


#### Guide

1. Unzip your source code and place it somewhere safe.
2. Create a new file in the root directory of the source, called YOUR_BOT.py

Type in the following code.

```py
import src
from src import *

import os

import dotenv
from dotenv import load_dotenv

load_dotenv('.env')
token_name = os.getenv("YOUR_TOKEN_REGISTRY") # Make sure that your token variable is NOT called 'token', as this powers things behind the scenes for the official bot instance.

bot = Azumi(intents=Azumi().intents)

# Your extension code goes here.


bot.run(mytoken)
```

There you go! That's all!

# End of Guide