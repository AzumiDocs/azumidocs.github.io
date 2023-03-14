# Azumi Guide

 
🙂 Thanks to `docsify` for making this possible!
Check out the `docsify` project [here](https://docsify.js.org/).



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