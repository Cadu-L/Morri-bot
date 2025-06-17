import discord
from discord.ext import commands

intents = discord.Intents.all()
bot = commands.Bot('!', intents=intents)

@bot.event
async def on_ready():
     sincs = await bot.tree.sync()
     print(f'{len(sincs)} Comanddos foram sicronizados com sucesso.')
     print('Morris inicializado com sucesso.')
@bot.event
async def on_member_join(membro:discord.Member):
    canal = bot.get_channel('ID')
    await canal.send(f'{membro.mention} se tornou membro do servidor!')

@bot.event
async def on_member_join(membro:discord.Member):
    canal = bot.get_channel('ID')
    await canal.send(f'{membro.mention} saiu do servidor.')

@bot.command()
async def Morris(ctx:commands.Context):
    nome = ctx.author.name 
    await ctx.reply(f'Olá {nome}, me chamo Morris, sou um bot desenvolvido pelo Carlos do servidor Sangas, espero que você goste de mim.')

@bot.tree.command()
async def somar(interact:discord.Interaction, n1:float, n2:float):
    resultado = n1 + n2
    await interact.response.send_message(f'O resultado de {n1} + {n2} é igaul a {resultado}')

@bot.command()
async def bom_dia(ctx:commands.Context):
    minha_embed = discord.Embed()
    minha_embed.title = 'Título da imagem.'
    minha_embed.description = ('Mensagem de descrição.')

    imagem = discord.File('nome da imagem', 'nome da imagem')
    minha_embed.set_image(url='attachament://nome da imagem')

    await ctx.reply(embed=minha_embed, file=imagem)

@bot.command()
async def boa_noite(ctx:commands.Context):
        minha_embed = discord.Embed()
        minha_embed.title = 'Título da imagem.'
        minha_embed.description = ('Mensagem de discrição.')

        imagem = discord.File('nome da imagem', 'nome da imagem.')
        minha_embed.set_image(url='attachament://nome da imagem.')

        await ctx.reply(embed=minha_embed, file=imagem)

@bot.command()
async def oi(ctx:commands.context):
     minha_embed = discord.Embed()
     minha_embed.title = 'Título da imagem.'
     minha_embed.description = ('Mensagem de discrição.')

     imagem = discord.File('nome da imagem', 'nome da imagem')
     minha_embed.set_image(url='attachament://nome da imagem')

     await ctx.reply(embed=minha_embed, file=imagem)

bot.run('token do seu bot')
