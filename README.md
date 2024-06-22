# clase7import discord
from discord.ext import commands

description="este es un programa donde vinculamos vs code con discord para lanzar imagenes"

intents= discord.Intents.default()
intents.members=True
intents.message_content=True

bot=commands.Bot(command_prefix="/", description=description,intents=intents)

@bot.event
async def on_ready():
    print(f"logeado como {bot.user} (ID: {bot.user.id})")

@bot.event
async def on_message(message):
    if message.author==bot.user:
        return
    
    if message.content.lower()=="/sendcat":
        with open("nationalgeographic_1468962.jpg", "rb")as f:
            picture = discord.file(f)
            await message.channel.send(content="aqui esta la imagen de tu gatito", file=picture)
            
bot.run("MTI1Mzg5ODMyMTYzOTExNjgwMQ.G91vsT.S10AhDI8OAArdrDBQssnuPuPXZhTOXMpRDiKbQ")





f  = open("text.txt", "r", encoding="utf-8")
text = f.read()
print(text)
f.close()


f = open("text.txt", "w", encoding="utf=8")
text = "perro"
f.write(text)
f.close()

with open("text.txt", "r", encoding="utf-8") as f:
    print(f.read()) 
algunas otras cosas que utilice fueron estas:

gato

nationalgeographic_1468962.jpg
y pues ya :)
