# Coming soon!

### Extending from Azumi

This section of the guide will show you how to create a bot extension from Azumi. This will allow you to run your own instance of Azumi.


#### Requirements

- IDE/Code Editor
- A copy of Azumi's source code. (Good luck getting a hold of this... 😂)
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
token_name = os.getenv("YOUR_TOKEN_REGISTRY") # Make sure that your token variable is not called 'token', as this powers things behind the scenes.

bot = Azumi(intents=Azumi().intents)

# Your extension code goes here.


bot.run(mytoken)
```

There you go! That's all!