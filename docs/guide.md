# Azumi Guide

### Extending from Azumi

This section of the guide will show you how to create a bot extension from Azumi. This will allow you to run your own instance of Azumi.


#### Requirements

- IDE / Code Editor / Notepad
- A copy of Azumi's source code. (There must be a clear and valid reason in your application for receiving source code. Source code is currently not available to non-developers.)
- Basic Python object knowledge.
- Experience with Pycord.


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

# YOUR CODE


bot.run(mytoken)
```

There you go! That's all!

### Contributing code to Azumi

To contribute code to Azumi, you must first write code!

#### Commands

##### Requirements

- IDE / Code Editor / Notepad
- Basic Python object knowledge.
- Experience with Pycord.

##### Guide

1. Create a new `.py` file.
2. Import all of the necessary modules for your code.
3. Create a cog inside of the file, like so:

```py
class CogName(commands.Cog):

    def __init__(self, bot):
        self.bot = bot

    # YOUR CODE


def setup(bot):
    bot.add_cog(CogName(bot))
```

4. Create a private GitHub gist [here](https://gist.github.com).
5. Add your code to the gist.
6. Grab the link to the gist.
7. DM the gist to AquaQuokka.
8. The code will be reviewed by the developers, and if decided to be suitable, will be added.

# End of Guide