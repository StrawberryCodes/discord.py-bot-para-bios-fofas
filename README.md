# discord.py-bot-para-bios-fofas
Comando: !bio  Gera uma bio estética aleatória usando kaomojis, símbolos decorativos e frases em português.

# ================= BIO =================

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

@bot.command()
async def bio(ctx):
    simbolo1 = random.choice(SIMBOLOS)
    simbolo2 = random.choice(SIMBOLOS)

    while simbolo2 == simbolo1:
        simbolo2 = random.choice(SIMBOLOS)

    kaomojis = random.sample(KAOMOJIS, 3)

    texto = f"""
{simbolo1}

{random.choice(FRASES)}

{kaomojis[0]}

{random.choice(SIMBOLOS)}

{kaomojis[1]}

{kaomojis[2]}

{simbolo2}
"""

    await ctx.send(texto)
