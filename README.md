# DexScript - ALPHA

DexScript is a set of commands developed by DotZZ on September 14, 2024, used for **BallsDex and CarFigures** Discord bot forks.
Below is a guide on how to use DexScript, and what DexScript is capable of.
Currently, DexScript is in alpha. DexScript will have more commands, the ability to support more models, and overall quality-of-life improvements as time passes.

<img src="https://i.imgur.com/uKfx0qO.png" width="200"> 

## Installation & Updating

> [!NOTE]
> Using the same command to install DexScript will update if DexScript is detected in your Discord bot.

Installing and updating DexScript to your Discord bot is easy. All you need is permission to use the `eval` command.
To install and update DexScript for your Discord bot, copy the code below and run it using the `eval` command:

```py
import base64, requests
r = requests.get("https://api.github.com/repos/Dotsian/DexScript/contents/installer.py")

if r.status_code == requests.codes.ok:
  content = base64.b64decode(r.json()["content"])
  await ctx.invoke(bot.get_command("eval"), body=content.decode("UTF-8"))
else:
  await ctx.send("Failed to install DexScript.\nReport this issue to `dot_zz` on Discord.")
  print(f"ERROR CODE: {r.status_code}")
```

After you run the installation code, you must restart the bot for the commands to take effect.
DexScript should be up and running when you're finished!

## Uninstalling

Uninstalling is the same as installing DexScript. All you need is permission to use the `eval` command.
To uninstall DexScript, copy the code below and run it using the `eval` command:

```py
import base64, requests
r = requests.get("https://api.github.com/repos/Dotsian/DexScript/contents/uninstaller.py")

if r.status_code == requests.codes.ok:
  content = base64.b64decode(r.json()["content"])
  await ctx.invoke(bot.get_command("eval"), body=content.decode("UTF-8"))
else:
  await ctx.send("Failed to uninstall DexScript.\nReport this issue to `dot_zz` on Discord.")
  print(f"ERROR CODE: {r.status_code}")
```

## Commands

There are three commands DexScript has at the moment.

1. **UPDATE**
2. **REMOVE**
3. **DISPLAY**

To run a command, you must put `b.run`, swapping `b.` with your bot's prefix.

-----------

> [!WARNING]
> CarFigures uses different field names for their models. Some of the examples below might not work on CarFigures.

### UPDATE

The `UPDATE` command updates a ball depending on the field given. The function is structured like this:<br>
```sql
UPDATE > BALL > ball_name > FIELD > value
```

- `ball_name` has to be replaced with the country of the ball you are trying to edit.
- `FIELD` has to be replaced with the field you are trying to edit. (EXAMPLE: CREDITS)
- `value` has to be replaced with the new value you want that field to be.

Changing a Roman Empire ball's credits (EXAMPLE):<br>
```sql
UPDATE > BALL > Roman Empire > CREDITS > dotzz (Spawn & Card)
```

-----------

### REMOVE

The `REMOVE` command deletes a ball depending on the name given:<br>
```sql
REMOVE > BALL > ball_name
```

- `ball_name` has to be replaced with the country of the ball you are trying to delete.

Deleting a Parthian Empire ball (EXAMPLE):<br>
```sql
REMOVE > BALL > Parthian Empire
```

-----------

### DISPLAY

The `DISPLAY` command displays the value of a specified field for a ball:<br>
```sql
DISPLAY > BALL > ball_name > FIELD
```

- `ball_name` has to be replaced with the country of the ball you are trying to access.
- `FIELD` has to be replaced with the field you are trying to view. (EXAMPLE: ATTACK)

Displaying an Ancient Greece ball's health (EXAMPLE):<br>
```sql
DISPLAY > BALL > Ancient Greece > HEALTH
```

-----------

Written by DotZZ <br>
DexScript Version: 0.2.1
