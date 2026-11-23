# Caixa Postal — roteiro visual de animação 3D (Short vertical)

Ficção · PT-BR · 9:16 · cerca de 30 s

---

## Narração (texto preservado, sem alterações)

> Depois que o pai morreu, todo domingo Bia ligava pro celular dele só pra ouvir a caixa postal. Até que um dia alguém atendeu. Era o irmão. “Você ainda paga essa linha?”, ela perguntou. Ele respondeu: “Pago. Eu ligo aos sábados.”

**Regra de ouro da montagem:** nenhum quadro antes da última fala pode mostrar que o irmão também liga pro pai. O celular do irmão, o histórico de chamadas dele e qualquer “sábado” na tela ficam escondidos até ele dizer **“Eu ligo aos sábados.”**

---

## Configuração no Blender

| Item | Valor |
|---|---|
| Resolução | 1080 × 1920 (9:16), 100% |
| Taxa de quadros | 24 fps |
| Duração | 720 quadros (0:00–0:30) |
| Motor | Eevee Next (prévia) / Cycles com 128 amostras + denoise (final) |
| Gestão de cor | AgX, aparência *Medium High Contrast* |
| Áreas seguras | Legendas e elementos importantes entre 15% e 75% da altura (fora da interface do Shorts/TikTok) |
| Câmeras | `CAM_01` a `CAM_04` com *markers* na Timeline (Ctrl+B para vincular a câmera ao marker) |

**Personagens (rigs):**
- `BIA`: cerca de 30 anos, moletom largo que era do pai, cabelo preso de qualquer jeito. Shape keys: `olhos_fechados`, `respira`, `labio_treme`, `sorriso_choro`.
- `IRMAO`: um pouco mais velho, barba por fazer, camisa xadrez do pai. Shape keys: `engole_seco`, `olhar_baixo`, `meio_sorriso`.

**Objetos-chave:**
- `CEL_PAI`: celular antigo, capinha gasta e tela trincada no canto. A tela é um material emissivo com textura trocável por *Image Sequence*.
- `CEL_BIA`: celular de Bia.
- `CEL_IRMAO`: celular do irmão. **Fica oculto (`hide_render`) até o quadro 600.**
- `BANCADA_PAI`: bancada de marcenaria com óculos, relógio de pulso parado e caneca com lápis.

**Cenários:**
- **Apartamento de Bia:** manhã de domingo, luz fria azulada vindo da janela (Area Light 5600 K) e chuva fina no vidro.
- **Oficina do pai:** penumbra quente, uma lâmpada pendente (Point Light 2700 K) e poeira em suspensão (partículas com volume leve).

---

## CENA 1: O toque
**0:00–0:08 · quadros 1–192**
**Narração:** “Depois que o pai morreu, todo domingo Bia ligava pro celular dele só pra ouvir a caixa postal.”

### Plano 1A (quadros 1–60): primeiro quadro, o celular tocando
- **Enquadramento:** plano detalhe, em plongée de 70°, sobre `CEL_PAI` deitado na `BANCADA_PAI`. Lente de 85 mm, f/1.8, foco na tela; os óculos e o relógio do pai ficam desfocados no fundo.
- **Quadro 1:** o celular já está tocando. A tela acesa mostra **“Bia 💛 chamando…”**. Nenhuma pessoa em cena.
- **Ação do objeto:** vibração com o modificador *Noise* na curva de Location X/Y (amplitude de 0,002 m, em pulsos de 1 s ligado e 0,5 s desligado). A poeira na bancada treme a cada pulso.
- **Câmera:** *push-in* lento de 8% até o quadro 60.
- **Som:** toque de celular abafado, chuva distante.

### Plano 1B (quadros 61–192): Bia escuta
- **Enquadramento:** plano médio-curto de Bia sentada no chão, encostada no sofá, com o celular no ouvido. Lente de 50 mm, câmera na altura dos olhos e leve *dutch angle* de 3°. A janela com chuva fica à esquerda, como contraluz.
- **Ações de BIA:**
  - Quadros 61–100: olhos já fechados (`olhos_fechados` = 1), joelhos dobrados e o braço livre abraçando as pernas.
  - Quadro 110: o toque para (a caixa postal atende). Ela solta o ar (`respira`, pico no quadro 115), os ombros descem 2 cm e a cabeça inclina na direção do celular.
  - Quadros 130–192: ela escuta em silêncio. O polegar acaricia a borda do celular (ciclo de 40 quadros) e há um leve sorriso triste.
- **Inserto opcional (quadros 150–170):** close de um calendário de parede com os **domingos** marcados por um coraçãozinho. Isso reforça a rotina dela sem revelar nada do irmão.
- **Câmera:** *dolly* lateral muito lento, da esquerda para a direita (0,3 m em 130 quadros).
- **Som:** bipe da caixa postal no quadro 112. A voz do pai fica **inaudível**, só um murmúrio grave e abafado.

---

## CENA 2: Alguém atende
**0:08–0:12 · quadros 193–288**
**Narração:** “Até que um dia alguém atendeu.”

### Plano 2A (quadros 193–228): outro domingo
- **Enquadramento:** o mesmo plano detalhe de 1A, para criar uma rima visual. `CEL_PAI` toca de novo na bancada e mostra **“Bia 💛 chamando…”**.
- **Ação:** no quadro 215, uma **mão masculina entra pela borda superior do quadro** e pega o celular. Não mostrar rosto, braço inteiro nem roupa identificável (a manga fica fora do quadro). O celular sai do quadro com *ease-out* rápido.
- **Câmera:** fixa. No quadro 220, o foco passa para os óculos do pai, que ficam sozinhos na bancada.
- **Som:** o toque é cortado no meio de um pulso.

### Plano 2B (quadros 229–288): o silêncio
- **Enquadramento:** close de Bia (lente de 85 mm), com o rosto ocupando o terço central do quadro.
- **Ações de BIA:**
  - Quadro 229: olhos ainda fechados, à espera do bipe.
  - Quadros 240–255: o bipe não vem. As sobrancelhas sobem e os olhos se abrem devagar (`olhos_fechados` de 1 para 0 em 15 quadros).
  - Quadros 255–288: ela congela. A mão aperta o celular (dedos se fecham 10°) e ela afasta o aparelho 2 cm do ouvido, como se tivesse levado um choque.
- **Câmera:** *push-in* de 5% e corte seco no quadro 288.
- **Som:** silêncio total por 1 s. Só se ouve uma respiração do outro lado da linha.

---

## CENA 3: Era o irmão
**0:12–0:20 · quadros 289–480**
**Narração:** “Era o irmão. ‘Você ainda paga essa linha?’, ela perguntou.”

### Plano 3A (quadros 289–336): a revelação de quem atendeu
- **Enquadramento:** plano médio do IRMAO sentado num banquinho na oficina do pai, com `CEL_PAI` no ouvido. Lente de 35 mm, câmera um pouco abaixo dos olhos dele. A lâmpada pendente fica atrás da cabeça, como contraluz.
- **Ações do IRMAO:**
  - Quadro 289: ele está de olhos baixos (`olhar_baixo` = 1) e engole seco (`engole_seco`, pico no quadro 300).
  - Quadros 305–336: a mão livre esfrega a nuca, num gesto de alguém flagrado.
- **Atenção:** `CEL_IRMAO` continua **oculto**. A bancada fica fora do quadro ou com a área do celular coberta por um pano.

### Plano 3B (quadros 337–480): tela dividida
- **Enquadramento:** split-screen vertical. **Metade de cima:** Bia em close (85 mm), com fundo azul frio. **Metade de baixo:** o irmão em close (85 mm), com fundo âmbar quente. A linha divisória fica no meio, com 6 px de *feather*.
  - Montagem no Blender: duas cenas (`SC_BIA` e `SC_IRMAO`) combinadas no Compositor com *Translate* e uma máscara retangular, ou no VSE com *Transform strips*.
- **Ações de BIA** (fala “Você ainda paga essa linha?”, quadros 380–440):
  - Ela se senta ereta, e o espanto vira desconfiança. Um olho se aperta levemente.
  - Sincronize a boca com a voz pelos visemas (Rhubarb Lip Sync ou keyframes manuais).
  - Na palavra “paga”, ela inclina a cabeça 5°.
- **Ações do IRMAO:**
  - Ele escuta sem olhar para a câmera, com o olhar fixo na bancada (fora do quadro).
  - No quadro 445, o polegar passa na tela trincada do `CEL_PAI`.
- **Câmera:** as duas metades ficam fixas, com um *breathing* sutil (Noise de 0,1° na rotação).
- **Som:** chuva só na metade de cima e o zumbido da lâmpada só na de baixo (panorama estéreo leve).

---

## CENA 4: “Eu ligo aos sábados.”
**0:20–0:30 · quadros 481–720**
**Narração:** “Ele respondeu: ‘Pago. Eu ligo aos sábados.’”

### Plano 4A (quadros 481–560): “Pago.”
- **Enquadramento:** close do irmão em tela cheia (o split termina com uma *wipe* para cima no quadro 481). Lente de 85 mm.
- **Ações do IRMAO:**
  - Quadros 481–515 (“Ele respondeu”): ele respira fundo e levanta o olhar pela primeira vez (`olhar_baixo` de 1 para 0).
  - Quadros 520–540 (“Pago.”): fala curta e firme, com um aceno mínimo de cabeça.
  - Quadros 540–560: pausa. O lábio aperta, como quem segura algo.
- **Câmera:** fixa. Nada de movimento: o peso fica na pausa.

### Plano 4B (quadros 561–660): a revelação, “Eu ligo aos sábados.”
- **Enquadramento:** a câmera desce num *pedestal down* do rosto do irmão até a bancada (lente de 50 mm, quadros 561–600).
- **Quadro 600:** `CEL_IRMAO` aparece pela primeira vez (desligar `hide_render`), virado para cima ao lado dos óculos do pai.
- **Quadros 605–640** (sincronizado com **“Eu ligo aos sábados.”**): a tela do `CEL_IRMAO` acende e mostra o histórico de chamadas:
  - `Pai · sáb 10:02`
  - `Pai · sáb 10:00`
  - `Pai · sáb 09:58`
  - `Pai · sáb 10:01` …
  - Use uma lista longa com rolagem automática para baixo (textura animada) que sugere meses de ligações.
- **Ação do IRMAO** (fora de foco, no fundo): ele abaixa a cabeça e solta um meio sorriso que se quebra (`meio_sorriso` para `engole_seco`).
- **Legenda na tela:** “Eu ligo aos sábados.” só aparece nesta fala, palavra por palavra.

### Plano 4C (quadros 661–720): o espelho
- **Enquadramento:** split-screen vertical de novo, agora só com **as telas dos dois celulares** em plano detalhe.
  - **Em cima:** `CEL_BIA` com o histórico `Pai · dom`, `Pai · dom`, `Pai · dom`…
  - **Embaixo:** `CEL_IRMAO` com `Pai · sáb`, `Pai · sáb`, `Pai · sáb`…
- **Ação de BIA** (inserto rápido, quadros 670–690, close a 85 mm): os olhos se enchem d’água. Ela solta um riso-choro (`sorriso_choro`) e cobre a boca com a mão.
- **Quadros 695–720:** as duas metades se aproximam até a linha divisória sumir, e as duas telas ficam lado a lado como um único histórico. Fade para preto em 12 quadros.
- **Som:** o bipe da caixa postal toca uma última vez, bem baixo, no quadro 705. Depois, silêncio.

---

## Resumo de tempo

| Cena | Tempo | Quadros | Enquadramento principal | Fala |
|---|---|---|---|---|
| 1. O toque | 0:00–0:08 | 1–192 | Detalhe do celular tocando, depois plano médio de Bia | “Depois que o pai morreu… caixa postal.” |
| 2. Alguém atende | 0:08–0:12 | 193–288 | Detalhe com a mão anônima, depois close de Bia | “Até que um dia alguém atendeu.” |
| 3. Era o irmão | 0:12–0:20 | 289–480 | Plano médio do irmão, depois split-screen dos rostos | “Era o irmão. ‘Você ainda paga essa linha?’…” |
| 4. Sábados | 0:20–0:30 | 481–720 | Close do irmão, *pedestal* até o celular dele, depois split das telas | “Ele respondeu: ‘Pago. Eu ligo aos sábados.’” |

## Checklist de continuidade
- [ ] O quadro 1 mostra `CEL_PAI` **já tocando**, com “Bia 💛” na tela.
- [ ] Nenhum rosto ou roupa do irmão aparece antes do quadro 289.
- [ ] `CEL_IRMAO` fica com `hide_render = True` até o quadro 599.
- [ ] A palavra “sábado” não aparece em tela, legenda ou objeto antes do quadro 605.
- [ ] A voz do pai na caixa postal fica sempre inaudível, sem acrescentar falas ao texto.
- [ ] A paleta fica fria em Bia e quente na oficina, e as duas se misturam só no plano final.
