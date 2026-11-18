
import discord
from discord.ext import commands
import random


# ♡ decoração dos stickers

STICKERS = [
    "https://media.giphy.com/media/TIXDy7zCGIFtfXwxoL/giphy.gif",  # coelhinho
    "https://media.giphy.com/media/8UtN9f7QJk9wI/giphy.gif",       # pudim
    "https://media.giphy.com/media/QWePdZrk7TMrEXTqMF/giphy.gif", # Hello Kitty
    "https://media.giphy.com/media/NMGc9JGgT89b2/giphy.gif"       # cherry blossom
]


# ♡ kaomojis

KAOMOJIS = [
    "૮ ˶ᵔ ᵕ ᵔ˶ ა",
    "૮꒰ྀི⸝⸝> . <⸝⸝꒱ྀིა",
    "˃̵ᴗ˂̵",
    "꒰ᐢ. .ᐢ꒱₊˚⊹",
    "ฅ^•ﻌ•^ฅ",
    "໒꒰ྀིっ˕ -｡꒱ྀི১",
    "(*ᴗ͈ˬᴗ͈)",
    "ʚ(｡˃ ᵕ ˂ )ɞ",
    "૮⸝⸝> ̫ <⸝⸝ ა",
    "૮₍˶ •. • ⑅₎ა♡",
    "°ʚ(´꒳`)ɞ°",
    "ദ്ദി ˉ͈̀꒳ˉ͈́ )✧",
    "⸜(｡˃ ᵕ ˂ )⸝♡",
    "(๑>◡<๑)",
    "(≧ヮ≦)",
    "( ˶ˆ꒳ˆ˵ )",
    "(˶˃ ᵕ ˂˶)",
    "(๑ᵔ⤙ᵔ๑)",
    "˶ˆ꒳ˆ˵",
    "𖦹ᯅ𖦹",
    "≽^•༚• ྀི≼",
    "໒꒰ྀི´ ˘ ` ꒱ྀིა",
    "(˶>⩊<˶)",
    "𐔌՞. .՞𐦯",
    "૮ ྀིᴗ͈ . ᴗ͈ ྀིა",
    "(..◜ᴗ◝..)",
    "₍^. .^₎⟆",
    "૮₍ ´ ꒳ `₎ა"
]


# ♡ símbolos decorativos

SIMBOLOS = [
    "♡",
    "୨ৎ",
    "⋆𐙚₊˚⊹♡",
    "⋆౨ৎ˚⟡˖ ࣪",
    "₊˚⊹♡",
    "☆⋆｡𖦹°‧★",
    "୧ ‧₊˚ 🍓 ⋅ ☆",
    "⋆˚✿˖°",
    "𓍢ִ໋🌷͙֒",
    "⊹₊｡ꕤ˚₊⊹",
    "˚ ༘ ೀ⋆｡˚",
    "⋅˚₊‧ ୨୧ ‧₊˚ ⋅",
    "₊˚⊹⋆",
    ".𖥔 ݁ ˖"
]


# ♡ frases para as bios

FRASES = [
    "eu, meu gloss e meus problemas",
    "apenas uma garota sonhadora",
    "vivendo no meu mundinho",
    "colecionando memórias",
    "coração de morango",
    "florescendo aos poucos",
    "mais brilho, menos drama",
    "entre estrelas e pensamentos",
    "só existindo em paz",
    "garota de fases",
    "perdida entre nuvens",
    "um caos organizado",
    "fofa por fora, surtada por dentro",
    "fazendo amizade com a lua",
    "sobrevivendo com música e café",
    "doce como morango",
    "um pouco tímida, um pouco doida",
    "meu próprio conto de fadas",
    "energia de princesa cansada",
    "pensando demais desde sempre",
    "vivendo um dia de cada vez",
    "brilhando do meu jeito",
    "pequena demais para tanto estresse",
    "entre laços e sonhos",
    "tentando não surtar",
    "coração fofinho e mente bagunçada",
    "só uma garota na internet",
    "versão limitada de mim mesma",
    "flores e pensamentos aleatórios",
    "bonita, confusa e ocupada"
]


# ♡ comando !bio

@bot.command()
async def bio(ctx):

    simbolo1, simbolo2 = random.sample(SIMBOLOS, 2)
    kaomojis = random.sample(KAOMOJIS, 3)

    frase = random.choice(FRASES)
    sticker = random.choice(STICKERS)

    texto = (
        f"{simbolo1}\n\n"
        f"{frase}\n\n"
        f"{kaomojis[0]}\n\n"
        f"{random.choice(SIMBOLOS)}\n\n"
        f"{kaomojis[1]}\n"
        f"{kaomojis[2]}\n\n"
        f"{simbolo2}\n\n"
        f"{sticker}"
    )

    await ctx.send(texto)
