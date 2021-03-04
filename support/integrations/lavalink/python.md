# Python

## Introduction

To use this code just do:

1. Download in [`Releases`](https://github.com/discloud/lavalink-python/releases) or [Click here](https://github.com/discloud/lavalink-python/releases/latest/download/lavalink-python.zip)

2. Once downloaded, simply place your Bot code in the bot directory

3. In the `config.json` file in `fileRunBot` change the name of the main file \(in this case, it is `main.py` but if it is another name \(such as `bot.py`\) change to the correct name\)  
  
4. In your code, area where you connect Lavalink please enter this data:

> ```python
> {
>   host: "localhost",
>   port: 2333,
>   password: "discloud"
> }
> ```
>
> After everything is done and send it to DisCloud by placing index.js as Main File

### LAVALINK FAQ

### Java/Lavalink is corrupted what do I do now?

The quickest way to resolve it is to delete the `Java directory` \(which is the directory where the OpenJDK and LavaLink files are located\) and start the BOT again which will download everything again

### I want to backup my files but it is very heavy what do I do?

To reduce the weight of the backup download you can remove:

* Directory `java`
* If you do not want to receive backup logs, also remove the directory`logs`

### Why does my BOT take so long to go online?

In the first Deploy it is clear that it takes more time than expected already before starting Bot you have to download **OpenJDK** and Lavalink \(and of course it depends on the internet\) and start Lavalink first. In the next Deploy, just wait for Lavalink to start

**Note:** removing the **Java directory** will be like the **first Deploy** when starting.

### It looks like this code has not been updated, how can I update it?

The fastest way in DisCloud is just to delete the Java directory \(there may be an update in the files\) to download the new[`Release`](https://github.com/discloud/lavalink-python/releases/latest/download/lavalink-python.zip), make changes to the `fileRunBot` that I have already commented on and send the changes.

### How do I make changes to my Bot with this code?

Simply put, your code change zip file must look like this:

```text
zip > bot > <your code>
```

Remember to always put your project code in the Bot folder, if you don't, the commit will save your files at the root of the instance and your Bot will not work

