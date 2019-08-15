# go to the terminal or command prompt and type in "python -m pip install discord.py"\

import discord
from discord.ext import commands
import random

bot = commands.Bot(command_prefix='$')
cat_list = ['https://media2.giphy.com/media/13CoXDiaCcCoyk/200.webp',
            'https://media3.giphy.com/media/JIX9t2j0ZTN9S/200w.webp',
            'https://media0.giphy.com/media/yFQ0ywscgobJK/giphy.webp',
            'https://media3.giphy.com/media/OmK8lulOMQ9XO/200w.webp', 'https://media1.giphy.com/media'
                                                                      '/3oriO0OEd9QIDdllqo/200.webp?cid'
                                                                      '=790b761164f0fe178a7bdc32b25f86098006b683405d15ae&rid=200.webp']

dog_list = ['https://media1.giphy.com/media/QvBoMEcQ7DQXK/giphy.webp?cid'
            '=790b76111bca112891c689abd4c88dc2c3d919cebaeee512&rid=giphy.webp',
            'https://media.giphy.com/media/Z3aQVJ78mmLyo/giphy.gif',
            'https://media1.giphy.com/media/fnlXXGImVWB0RYWWQj/200w.webp?cid'
            '=790b76111bca112891c689abd4c88dc2c3d919cebaeee512&rid=200w.webp',
            'https://media2.giphy.com/media/9Ji1s0nTBLlKQEhpLu/200w.webp?cid'
            '=790b76111bca112891c689abd4c88dc2c3d919cebaeee512&rid=200w.webp', 'https://media2.giphy.com/media'
                                                                               '/fsbTLYjtw1MHErU5tX/200w.webp?cid'
                                                                               '=790b761143a093d388190e1daf64747fd1de0e149f3e112b&rid=200w.webp']


@bot.event
async def on_ready():
    print('Bot Online:')
    print('NAME OF BOT')
    print(bot.user.id)
    print('------')


@bot.command()
async def fliptable(ctx):
    await ctx.send("(╯°□°）╯︵ ┻━┻ ")


@bot.command()
async def unflip(ctx):
    await ctx.send("┬─┬ ノ( ゜-゜ノ)")


@bot.command()
async def shrug(ctx):
    await ctx.send("¯\_(ツ)_/¯ ")


@bot.command()
async def creeper(ctx):
    await ctx.send("Aww man")


@bot.command()
async def add(ctx, a: int, b: int):
    await ctx.send(a + b)


@bot.command()
async def multiply(ctx, a: int, b: int):
    await ctx.send(a * b)


@bot.command()
async def greet(ctx):
    await ctx.send(":smiley: :wave: Hello, there!")


@bot.command()
async def cat(ctx):
    num = random.randint(0, 4)
    link = cat_list[num]
    await ctx.send(link)


@bot.command()
async def doggo(ctx):
    num = random.randint(0, 4)
    link = dog_list[num]
    await ctx.send(link)


@bot.command()
async def info(ctx):
    embed = discord.Embed(title="NAME OF BOT", description="BOT DESCRIPTION", color=0xeee657)

    # give info about you here
    embed.add_field(name="Username", value="USERNAME")

    # give users a link to invite this bot to their server
    embed.add_field(name="Add", value="Add me to your server! ")

    await ctx.send(embed=embed)


bot.remove_command('help')


@bot.command()
async def help(ctx):
    embed = discord.Embed(title="NAME OF BOT", description="DESCRIPTION OF BOT. List of commands are:", color=0xeee657)

    embed.add_field(name="$add X Y", value="Gives the addition of **X** and **Y**", inline=False)
    embed.add_field(name="$multiply X Y", value="Gives the multiplication of **X** and **Y**", inline=False)
    embed.add_field(name="$greet", value="Gives a nice greet message", inline=False)
    embed.add_field(name="$cat", value="Gives a cute cat gif to lighten up the mood.", inline=False)
    embed.add_field(name="$info", value="Gives a little info about the bot", inline=False)
    embed.add_field(name="$help", value="Gives this message", inline=False)
    embed.add_field(name="$doggo", value="Gives a cute doggo gif", inline=False)
    embed.add_field(name="$creeper", value="You know what this does", inline=False)
    embed.add_field(name="$shrug", value="I don't know", inline=False)
    embed.add_field(name="$fliptable", value="For when you really hate your job", inline=False)
    embed.add_field(name="$unflip", value="For when you really love your job", inline=False)

    await ctx.send(embed=embed)


bot.run('BOT TOKEN')
