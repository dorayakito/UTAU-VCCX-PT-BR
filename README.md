# Documentação Completa - VCCX PT-BR

**Versão:** 1.0  
**Autor:** Dorayakito  
**Data:** 01/01/2026

> **Base sólida e estável para criação de voicebanks VCCX em Português Brasileiro.** Documentação completa com 652 amostras, guia de gravação detalhado, configuração de oto.ini, e sistema fonético otimizado para síntese vocal natural no OpenUtau.

---

## 📋 Índice

1. [Introdução](#introdução)
2. [Sistema Fonético](#sistema-fonético)
3. [Lista de Gravação](#lista-de-gravação)
4. [Guia de Gravação](#guia-de-gravação)
5. [Configuração do Voicebank](#configuração-do-voicebank)
6. [Uso do Phonemizer](#uso-do-phonemizer)
7. [Troubleshooting](#troubleshooting)
8. [Recursos Adicionais](#recursos-adicionais)

---

## 🎵 Introdução

### O que é o VCCX PT-BR?

**VCCX** (Vowel-Consonant-Consonant-X) é um formato de voicebank otimizado para **Português Brasileiro**, baseado no sistema VCCV tradicional com extensões adicionais. O "**X**" representa a **flexibilidade** do formato, podendo ser C, V, CV, VC, VCV, CC ou VV de acordo com a necessidade fonética. Este formato oferece:

- **CVVC**: Cobertura completa de todas as consoantes e vogais (312 amostras)
- **VCV**: Transições suaves para consoantes contínuas (180 amostras)
- **VV**: Ditongos e hiatos naturais (72 amostras)
- **Clusters**: Encontros consonantais complexos (88 amostras)

O sistema foi projetado para capturar a riqueza fonética do português brasileiro, incluindo **vogais nasais**, **ditongos**, **africadas** e **encontros consonantais** de forma natural e expressiva. No futuro, o sistema será expandido para suportar diferentes variantes do português, como **Português Europeu** (Portugal), **Português Angolano**, **Galego**, entre outros.

[Veja aqui os prós](https://github.com/dorayakito/UTAU-VCCX-PT-BR/blob/main/PROS.md) e [veja aqui os contras](https://github.com/dorayakito/UTAU-VCCX-PT-BR/blob/main/CONS.md) do VCCX antes de continuar.

### O VCCX PT-BR Phonemizer

O **VCCX Portuguese BR Phonemizer** é um phnoemizer/plugin **fonético (e também g2p)** para OpenUtau que permite a síntese de voz usando voicebanks gravadas no formato VCCX. Também possui uma versão **G2P (Grapheme-to-Phoneme)** para conversão automática de texto. Este phonemizer oferece:

- ✅ **Transições naturais** entre vogais e consoantes
- ✅ **Suporte completo** para ditongos, nasalização e encontros consonantais
- ✅ **Flexibilidade** para entrada de texto em português ou fonemas diretos
- ✅ **Fallbacks inteligentes** para fonemas não gravados
- ✅ **Compatibilidade** com X-SAMPA e outros sistemas de notação, como: **FLAVA/BRIGADEIRO**, **PRIZMA**, **BRAPA**, etc.
- ✅ **Timing automático** otimizado para português brasileiro

### Requisitos

- **OpenUtau** ou **UTAU Legacy** (versão mais recente recomendada).
- **Software de gravação** (Oremo, RecStar, Audacity, Reaper, etc.).
- **Editor de oto.ini** (SetParam, vLabeler, Copaiba, Utalet, UTAU, etc.).
- **Conhecimento básico** de síntese vocal UTAU/OpenUtau, gravação e edição de oto.ini.

---

## 🔤 Sistema Fonético

### Vogais Básicas

| Símbolo | IPA | Exemplo | Descrição |
|---------|-----|---------|-----------|
| `a` | /a/ | c**a**sa | Vogal aberta central |
| `e` | /e/ | p**e**so | Vogal média fechada frontal |
| `i` | /i/ | v**i**da | Vogal fechada frontal |
| `o` | /o/ | p**o**vo | Vogal média fechada posterior |
| `u` | /u/ | l**u**a | Vogal fechada posterior |

### Vogais Nasais

| Símbolo | IPA | Exemplo | Descrição |
|---------|-----|---------|-----------|
| `@` | /ɐ̃/ | c**ã** | Vogal nasal central (ã) |
| `7` | /ẽ/ | t**em** | Vogal nasal frontal (em/en) |
| `1` | /ĩ/ | f**im** | Vogal nasal frontal fechada (im/in) |
| `0` | /õ/ | b**om** | Vogal nasal posterior (om/on/õ) |
| `Q` | /ũ/ | **um** | Vogal nasal posterior fechada (um/un) |

### Vogais Abertas

| Símbolo | IPA | Exemplo | Descrição |
|---------|-----|---------|-----------|
| `X` | /ɛ/ | caf**é** | Vogal média aberta frontal (é) |
| `V` | /ɔ/ | av**ó** | Vogal média aberta posterior (ó) |

### Consoantes

| Símbolo | IPA | Exemplo | Descrição |
|---------|-----|---------|-----------|
| `b` | /b/ | **b**ola | Oclusiva bilabial sonora |
| `ch` | /tʃ/ | **tch**ia | Africada pós-alveolar surda |
| `d` | /d/ | **d**edo | Oclusiva alveolar sonora |
| `f` | /f/ | **f**aca | Fricativa labiodental surda |
| `g` | /ɡ/ | **g**ato | Oclusiva velar sonora |
| `h` | /h/ | **r**ato (R inicial) | Fricativa glotal surda |
| `j` | /ʒ/ | **j**ogo | Fricativa pós-alveolar sonora |
| `k` | /k/ | **c**asa | Oclusiva velar surda |
| `l` | /l/ | **l**ua | Lateral alveolar |
| `lh` | /ʎ/ | ga**lh**o | Lateral palatal |
| `m` | /m/ | **m**ão | Nasal bilabial |
| `n` | /n/ | **n**ó | Nasal alveolar |
| `nh` | /ɲ/ | so**nh**o | Nasal palatal |
| `p` | /p/ | **p**ato | Oclusiva bilabial surda |
| `r` | /ɾ/ | ca**r**o | Vibrante simples (tap) |
| `rh` | /ʁ/ | **r**ua | Vibrante uvular |
| `rw` | /ʁw/ | eng/fo**r** | Vibrante + glide |
| `s` | /s/ | **s**avana | Fricativa alveolar surda |
| `sh` | /ʃ/ | **ch**azinho | Fricativa pós-alveolar surda |
| `t` | /t/ | **t**udo | Oclusiva alveolar surda |
| `v` | /v/ | **v**aca | Fricativa labiodental sonora |
| `w` | /w/ | pa**u** | Aproximante labial-velar |
| `y` | /j/ | pa**i** | Aproximante palatal |
| `z` | /z/ | **z**ap **z**ap | Fricativa alveolar sonora |

### Mapeamentos Alternativos (X-SAMPA)

O phonemizer aceita entrada em X-SAMPA e outros formatos:

| Entrada | Mapeamento | Descrição |
|---------|------------|-----------|
| `S` | `sh` | Fricativa pós-alveolar surda (ʃ) |
| `Z` | `j` | Fricativa pós-alveolar sonora (ʒ) |
| `J` | `nh` | Nasal palatal (ɲ) |
| `L` | `lh` | Lateral palatal (ʎ) |
| `4` | `r` | Vibrante simples (ɾ) |
| `R` | `rh` | Vibrante uvular (ʁ) |
| `tS` / `tch` / `T` | `T` → `ch` | Africada surda (tʃ) |
| `dZ` / `dj` / `D` | `d j` | Africada sonora (dʒ) |
| `E` | `X` | Vogal média aberta frontal (ɛ) |
| `O` | `V` | Vogal média aberta posterior (ɔ) |
| `6` | `a` | Vogal central (ɐ) |
| `6~` | `@` | Vogal nasal central (ɐ̃) |
| `e~` | `7` | Vogal nasal frontal (ẽ) |
| `i~` | `1` | Vogal nasal frontal fechada (ĩ) |
| `o~` | `0` | Vogal nasal posterior (õ) |
| `u~` | `Q` | Vogal nasal posterior fechada (ũ) |
| `an` / `An` | `@` | Vogal nasal central (ã) |
| `en` / `En` | `7` | Vogal nasal frontal (em/en) |
| `in` / `In` | `1` | Vogal nasal frontal fechada (im/in) |
| `on` / `On` | `0` | Vogal nasal posterior (om/on/õ) |
| `un` / `Un` | `Q` | Vogal nasal posterior fechada (um/un) |
| `e]` | `7` | Vogal nasal frontal alternativa (ẽ) |
| `i]` | `1` | Vogal nasal frontal fechada alternativa (ĩ) |
| `o]` | `0` | Vogal nasal posterior alternativa (õ) |
| `u]` | `Q` | Vogal nasal posterior fechada alternativa (ũ) |
| `3` | `X` | Vogal média aberta frontal alternativa (ɛ) |
| `hr` | `rh` | Vibrante uvular alternativa (ʁ) |
| `c` | `k` | Oclusiva velar surda alternativa |
| `ç` | `s` | Fricativa alveolar surda (cedilha) |
| `ss` | `s` | Fricativa alveolar surda (duplo s) |
| `x` | `sh` | Fricativa pós-alveolar surda alternativa |
| `kw` / `qu` / `qw` | `kw` / `qu` | Oclusiva velar + glide |

### Regras Especiais de Entrada

#### Letra "C"
- **ca, co, cu** → `k` + vogal (ex: "casa" → `k a z a`)
- **ce, ci** → `s` + vogal (ex: "cedo" → `s e d u`)
- **ç** → `s` (ex: "caça" → `k a s a`)

#### Letra "X"
- **xa, xe, xi, xo, xu** → `sh` + vogal (ex: "xale" → `sh a l i y`)

#### Letra "Q"
- **que, qui** → `k` + vogal (ex: "queijo" → `k e i j u`)
- **quo, qua** → `k` + vogal (ex: "quarto" → `k u a r t u`)

#### Letra "L"
- **L em final de sílaba** → `w` (ex: "sol" → `s V w`, "Brasil" → `b r a z i w`)
- **Importante para gravação:** Ao gravar amostras CVVC com "l", pronuncie o "l" final como **"w"**
  - Exemplo: `l@_l@_l` deve ser gravado como **"lã-lã-w"** (não "lã-lã-l")
  - Isso reflete a pronúncia natural do português brasileiro onde "l" em final de sílaba vira [w]

#### Ditongos Nasais
- **ão** → `@ w` (ex: "mão" → `m @ w`)
- **em/en** (final) → `7 nh` (ex: "tem" → `t 7 nh`)

---

## 📝 Lista de Gravação

A lista completa consiste em **652 amostras** divididas em 4 categorias:

### 1. CVVC (Consoante-Vogal-Vogal-Consoante)

**Total: 312 amostras** (26 consoantes × 12 vogais)

#### Formato

```
ba_ba_b
```

- **Primeira sílaba** (`ba`): sílaba completa com consoante inicial
- **Underscore** (`_`): separador entre repetições
- **Segunda sílaba** (`ba`): repetição da mesma sílaba
- **Underscore** (`_`): separador antes da consoante final
- **Consoante final** (`b`): consoante de fechamento

#### Pronúncia

Pronuncie de forma **natural e contínua**, como se estivesse dizendo "ba-ba-b" em uma única respiração:

- `ba_ba_b` → **"bá-ba-b"** (com consoante final curta)
- `che_che_ch` → **"tchê-tchê-tch"**
- `d@_d@_d` → **"dã-dã-d"** (nasal)

#### Cobertura

Todas as consoantes combinadas com todas as vogais:

```
cons: b ch d f g h j k l lh m n nh p r rh rw s sh t v w y z
vog: a e i o u @ 7 1 0 Q X V
```

**Exemplos:**
```
ba_ba_b    # b + a
be_be_b    # b + e
b@_b@_b    # b + ã (nasal)
bX_bX_b    # b + é (aberta)
cha_cha_ch # ch + a
lha_lha_lh # lh + a
```

### 2. VCV (Vogal-Consoante-Vogal)

**Total: 180 amostras** (5 consoantes × 36 combinações)

#### Formato

```
ra_ra_re_ra_ri
```

- **Cinco sílabas** separadas por underscores
- Consoante central (`r`) cercada por diferentes vogais
- Permite transições suaves VCV

#### Consoantes que usam VCV

Apenas consoantes **contínuas/fricativas**:
- `r` (vibrante simples)
- `s` (fricativa alveolar)
- `h` (fricativa glotal)
- `w` (aproximante)
- `y` (aproximante)

#### Pronúncia

Pronuncie de forma **fluida e conectada**, enfatizando a transição vogal→consoante→vogal:

- `ra_ra_re_ra_ri` → **"rá-rá-ré-rá-rí"**
- `sa_sa_se_sa_si` → **"sá-sá-sé-sá-sí"**

#### Por que VCV?

O VCV complementa o CVVC fornecendo transições mais **naturais e longas** para consoantes que podem ser sustentadas. Isso é especialmente importante para:
- **Consoantes contínuas** (r, s, h)
- **Glides** (w, y)
- **Transições vocálicas** suaves

### 3. VV (Vogal-Vogal)

**Total: 72 amostras** (duplicadas para redundância)

#### Formato

```
a_a_e_a_i
```

- **12 (doze) vogais** separadas por underscores
- Transições puras entre vogais (sem consoantes)
- Cada combinação aparece **duas vezes** na lista

> [!NOTE]
> Os encontros VV serão **revisados no futuro com maior cautela**, pois alguns estão faltando. No entanto, eles **não são críticos** e podem ser facilmente substituídos por:
> - **VCV de w ou y** (ex: `a wa`, `e yi`)
> - **Apenas V** (vogal isolada)
> - O phonemizer faz esses fallbacks automaticamente

#### Pronúncia

Pronuncie de forma **legato**, conectando as vogais sem pausas ou glotais:

- `a_a_e_a_i` → **"á-á-é-á-í"** (sem interrupção)
- `i_i_o_i_u` → **"í-í-ó-í-ú"**

#### Importância

As transições VV são cruciais para:
- **Ditongos** (ai, ei, ou, etc.)
- **Hiatos** (saída, país, etc.)
- **Sequências vocálicas** suaves

> [!TIP]
> Grave as transições VV com **volume consistente** em todas as vogais para evitar quebras inaudíveis.

### 4. Clusters (Consoante-Consoante)

**Total: 88 amostras**

#### Formato

```
bl_bl
```

- **Duas consoantes** seguidas, repetidas
- Encontros consonantais comuns em português

#### Pronúncia

Pronuncie as duas consoantes de forma **rápida e conectada**, como em palavras reais:

- `bl_bl` → **"bl-bl"** (como em "**bl**usa")
- `pr_pr` → **"pr-pr"** (como em "**pr**ato")
- `tr_tr` → **"tr-tr"** (como em "**tr**em")

#### Lista Completa de Clusters

```
bl br by dl dr dy fb fl fr fy
gl gr gw hy jy kl kr kw ly my
ny pl pr py qb qw ry sb sd sg
sk sl sm sn sp sq sr st sv sw
sy sz tb td tg tl tr ty vb vd
vg vl vr vy wb wd wg wl wr wy
xb xd xg xl xr xy yb yd yg yl
yr zb zd zg zl zm zn zr zy
```

> [!IMPORTANT]
> Nem todos os clusters são naturais em português, mas estão incluídos para **máxima flexibilidade** ao sintetizar palavras estrangeiras e principalmente neologismos.

---

## 🎙️ Guia de Gravação

### Preparação

#### 1. Configuração do Ambiente

- **Local silencioso** sem ruído de fundo
- **Tratamento acústico** (recomendado, mas não obrigatório por não ser tão acessível)
- **Posicionamento do microfone** consistente (5-15cm de distância, encontre o ponto quente do seu microfone realizando testes antes)

#### 2. Equipamentos Recomendados (não-obrigatórios)

- **Microfone condensador (com phantom power ou USB único)** ou **dinâmico de qualidade**
- **Interface de áudio** com baixa latência (opcional)
- **Gravador de fonemas/Editor/DAW** (RecStar, Oremo, Audacity, Reaper, FL Studio, etc.)
- **Fones de ouvido** para monitoramento

#### 3. Tom de Referência

Escolha **um tom confortável** para sua voz:

- **Vozes masculinas:** C3, D3, E3
- **Vozes femininas:** C4, D4, E4
- **Vozes infantis:** F4, G4, A4
- **Vozes neutras/sem gênero (sobreposição de registros):** D3, E3, F3, G3, A3, B3, C4

> [!TIP]
> Use um **afinador físico ou virtual**, ou toque uma nota de referência no piano para cada amostra. Consistência tonal é essencial!

### Técnica de Gravação

#### Para CVVC (ex: `ba_ba_b`)

1. **Inspire profundamente**
2. **Pronuncie:** "bá-ba-b" em um único fluxo
3. **Mantenha** a vogal `a` estável e clara
4. **Feche** com a consoante `b` de forma curta e definida
5. **Duração total:** ~2-3 segundos

**Visualização:**
```
ba____ba____b
└─┬─┘ └─┬─┘ └┬
  CV    CV    C (consoante final curta)
```

#### Para VCV (ex: `sa_sa_se_sa_si`)

1. **Inspire profundamente**
2. **Pronuncie:** "sá-sá-sé-sá-sí" de forma conectada
3. **Sustente** levemente a consoante `s` entre vogais
4. **Mantenha** todas as vogais com volume similar
5. **Duração total:** ~5-6 segundos

**Visualização:**
```
sa___sa___se___sa___si
└┬─┘ └┬─┘ └┬─┘ └┬─┘ └┬─┘
 VCV  VCV  VCV  VCV  VCV
```

#### Para VV (ex: `a_a_e_a_i`)

1. **Inspire profundamente**
2. **Pronuncie:** "á-á-é-á-í" de forma **legato** (sem pausas)
3. **Evite** golpes de glote entre vogais
4. **Transições suaves** sem mudanças de volume
5. **Duração total:** ~2-3 segundos

**Visualização:**
```
a____a____e____a____i
└──┬──┬──┬──┬──┬──┬─┘
   VV VV VV VV VV
```

#### Para Clusters (ex: `bl_bl`)

1. **Inspire**
2. **Pronuncie:** "bl-bl" de forma rápida
3. **Mantenha** as consoantes juntas, sem vogal inserida
4. **Duração total:** ~1-2 segundos

> [!TIP]
> Você pode usar **palavras reais** durante a gravação para facilitar a pronúncia natural dos clusters. Por exemplo:
> - `bl_bl` → pense em "**bl**usa" ao pronunciar
> - `pr_pr` → pense em "**pr**ato" ao pronunciar
> - `tr_tr` → pense em "**tr**em" ao pronunciar

**Visualização:**
```
bl___bl
└┬─┘ └┬─┘
 CC   CC
```

### Boas Práticas

#### ✅ Faça (Recomendações)

**Preparação Vocal:**
- ✅ **Faça aquecimento vocal** antes de gravar (5-10 minutos de exercícios)
- ✅ **Hidrate-se** constantemente (água em temperatura ambiente)
- ✅ **Faça pausas** regulares para descansar a voz (a cada 30-45 minutos)

**Organização:**
- ✅ **Grave em blocos** (ex: todas as amostras com "a" primeiro, depois "e", etc.)
- ✅ **Revise** as gravações em tempo real para detectar problemas cedo
- ✅ **Retenha takes extras** das melhores amostras como backup
- ✅ **Mantenha postura consistente** durante toda a sessão

**Qualidade de Áudio:**
- ✅ **Use tratamento acústico improvisado**: coloque um **travesseiro, cobertor ou almofada** atrás do microfone para absorver reflexões
- ✅ **Grave em um "canto acústico"**: use roupas penduradas, cortinas ou estantes de livros para reduzir eco
- ✅ **Mantenha distância consistente** do microfone (5-15cm, encontre o "ponto quente")
- ✅ **Teste antes de gravar tudo**: grave algumas amostras e ouça com atenção para ajustar

#### ❌ Evite (O que NÃO fazer)

**Ruídos Ambientais:**
- ❌ **Evite ruídos intensos de grilos/cigarras** no fundo (grave em horários mais silenciosos)
- ❌ **Desligue ventiladores** próximos ao microfone durante a gravação
- ❌ **Reduza a velocidade da ventoinha do computador** (use software como SpeedFan ou configure na BIOS - FAÇA ISSO COM CUIDADO E APENAS SE SOUBER DO QUE ESTÁ FAZENDO)
- ❌ **Não grave muito longe do microfone** (gera eco e captura muito ruído ambiente)
- ❌ **Evite gravar com ar-condicionado ligado** (ruído constante de fundo). Se você tem ar-condicionado inverter, **espere ele terminar o ciclo de resfriamento** - quando atinge a temperatura desejada, ele fica silencioso e você pode gravar nesse período
- ❌ **Feche janelas** para evitar ruídos de trânsito, chuva ou vento

**Saúde Vocal:**
- ❌ **Não grave** com fome, sede ou cansaço vocal
- ❌ **Não force** tons fora do seu alcance confortável
- ❌ **Evite gravar** logo após acordar (voz ainda "suja") ou muito tarde (voz cansada)
- ❌ **Não grave** após consumir laticínios (aumenta produção de muco)

**Técnica:**
- ❌ **Não mude** a distância do microfone entre takes
- ❌ **Não edite** pitch/formante drasticamente (use tom natural da sua voz - Faça isto somente se é o conceito do teu UTAU/voicebank)
- ❌ **Evite respirações ruidosas** próximas ao microfone (respire pelo nariz ou afaste-se levemente)
- ❌ **Não use pop filter improvisado de má qualidade** (pode abafar frequências)

#### 💡 Dicas Extras de Qualidade

1. **Tratamento acústico caseiro:**
   - Pendure cobertores grossos nas paredes próximas
   - Use caixas de ovos (não é o ideal, mas ajuda)
   - Grave dentro de um guarda-roupa cheio de roupas (absorção natural)
   - Construa um "escudo" com travesseiros ao redor do microfone

2. **Redução de ruído do PC:**
   - Grave com laptop na bateria (geralmente mais silencioso que desktop)
   - Coloque o computador em outra sala e use cabos longos
   - Use um tablet/celular com interface de áudio portátil
   - Configure perfil de energia "silencioso" durante gravação

3. **Horários ideais:**
   - Grave de madrugada (menos ruído externo)
   - Evite horários de pico de trânsito
   - Escolha dias sem chuva/vento forte

4. **Monitoramento:**
   - Use fones de ouvido fechados para monitorar em tempo real
   - Grave com metrônomo/clique se tiver dificuldade com timing
   - Faça testes de ruído de fundo antes de começar a sessão completa  

---

## ⚙️ Configuração do Voicebank

### Estrutura de Arquivos

```
MeuVoicebank/
├── character.txt
├── character.yaml
├── oto.ini (vazia - necessária para o UTAU detectar o voicebank)
├── readme.txt
├── CVVC/
│   ├── ba_ba_b.wav
│   ├── be_be_b.wav
│   ├── bi_bi_b.wav
│   ├── ... (todas as 312 amostras CVVC)
│   └── oto.ini
├── VCV/
│   ├── ra_ra_re_ra_ri.wav
│   ├── sa_sa_se_sa_si.wav
│   ├── ... (todas as 180 amostras VCV)
│   └── oto.ini
├── VV/
│   ├── a_a_e_a_i.wav
│   ├── i_i_o_i_u.wav
│   ├── ... (todas as 72 amostras VV)
│   └── oto.ini
└── CC/
    ├── bl_bl.wav
    ├── pr_pr.wav
    ├── ... (todas as 88 amostras de clusters)
    └── oto.ini
```

> [!NOTE]
> - O arquivo `oto.ini` na **raiz** deve estar **vazio** - ele serve apenas para o UTAU detectar que existe um voicebank nessa pasta
> - Cada **subpasta** (CVVC, VCV, VV, CC) tem seu próprio `oto.ini` com as configurações específicas
> - Esta organização facilita a manutenção e edição do voicebank

### Nomenclatura de Arquivos

Os arquivos WAV devem ter **exatamente** o mesmo nome que os aliases:

- `ba_ba_b.wav`
- `cha_cha_ch.wav`
- `ra_ra_re_ra_ri.wav`
- `a_a_e_a_i.wav`
- `bl_bl.wav`

> [!CAUTION]
> Use **underscores** (`_`), não hífens (`-`) ou espaços nos nomes dos arquivos!

### Configuração de oto.ini (Uso e existência)

O arquivo `oto.ini` define como cada amostra é dividida em fonemas utilizáveis.

#### Parâmetros oto.ini (Como ela trabalha)

```
NomeArquivo.wav=Alias,Offset,Consonant,Cutoff,Preutterance,Overlap
```

- **Alias:** Nome do fonema (ex: `ba`, `a b`, `b a-`)
- **Offset:** Início do fonema útil (ms)
- **Consonant:** Duração da consoante (ms)
- **Cutoff:** Corte do final (negativo = do fim, ms)
- **Preutterance:** Ponto de início da vogal (ms)
- **Overlap:** Sobreposição para transição (ms)

#### Exemplos de Configuração

##### CVVC: `ba_ba_b.wav`

Esta amostra gera **múltiplos aliases**:

```ini
ba_ba_b.wav=ba,0,50,-350,80,30
ba_ba_b.wav=a b,250,80,-200,100,40
ba_ba_b.wav=b a,350,50,-100,80,30
ba_ba_b.wav=a b-,500,80,0,100,40
```

**Demonstração:**
- `ba` → CV inicial (consoante + vogal)
- `a b` → VC transição (vogal → consoante)
- `b a` → CV interno
- `a b-` → VC final (com dash para indicar fim de nota)

##### VCV: `ra_ra_re_ra_ri.wav`

```ini
ra_ra_re_ra_ri.wav=ra,0,40,-800,70,25
ra_ra_re_ra_ri.wav=a ra,200,40,-600,70,35
ra_ra_re_ra_ri.wav=a re,400,40,-400,70,35
ra_ra_re_ra_ri.wav=a ri,600,40,-200,70,35
```

**Demonstração:**
- `ra` → CV inicial
- `a ra` → VCV (a→r→a)
- `a re` → VCV (a→r→e)
- `a ri` → VCV (a→r→i)

##### VV: `a_a_e_a_i.wav`

```ini
a_a_e_a_i.wav=a,0,0,-800,50,20
a_a_e_a_i.wav=a e,200,0,-600,50,30
a_a_e_a_i.wav=a i,400,0,-400,50,30
a_a_e_a_i.wav=e i,600,0,-200,50,30
```

**Demonstração:**
- `a` → Vogal inicial isolada
- `a e` → Transição VV
- `a i` → Transição VV
- `e i` → Transição VV

##### Cluster: `bl_bl.wav`

```ini
bl_bl.wav=b l,0,100,-200,80,40
bl_bl.wav=-b l,50,100,-150,80,40
```

**Demonstração:**
- `b l` → Cluster padrão
- `-b l` → Cluster com dash (início de frase)

### character.yaml (Recomendado)

> [!TIP]
> Use o **Gerador de character.yaml** da Misc Labs para criar este arquivo facilmente:  
> 🔗 [https://misc-labs.github.io/Gerador-de-character-openutau.github.io/](https://misc-labs.github.io/Gerador-de-character-openutau.github.io/)

```yaml
name: Meu Voicebank VCCX
image: character.png
author: Seu Nome
voice: Nome do voicer
web: https://seusite.com
version: 1.0

text_file_encoding: utf-8
default_phonemizer: OpenUtau.Plugin.Builtin.PortugueseBrazilVCCXPhonemizer

subbanks:
  - color: "Default"
    prefix: ""
    suffix: ""
    tone_ranges:
      - C3-C5
```

---

## 🎼 Uso do Phonemizer

### Instalação

1. **Baixe** o plugin (ou compile a partir do código-fonte)
2. **Copie** `PortugueseBrazilVCCXPhonemizer.dll` para a pasta de plugins do OpenUtau:
   - **Windows:** `/OpenUtau/Plugins`
   - **MacOS:** `~/Library/Application Support/OpenUtau/Plugins`
   - **Linux:** `~/.config/OpenUtau/Plugins`
3. **Reinicie** o OpenUtau
4. **Selecione** "VCCX PT-BR" no menu de phonemizers

### Modos de Entrada

#### 1. Entrada Fonética Direta (Recomendado)

Use os símbolos fonéticos para controle preciso:

| Entrada | Descrição | Fonemas Gerados | Aliases |
|---------|-----------|-----------------|---------|
| `k a z a` | "Casa" (com espaços) | `k a z a` | `-k a`, `a z`, `z a` |
| `m @ w` | "Mão" (ditongo nasal) | `m @ w` | `-m @`, `@ w-` |
| `s X w` | "Céu" (vogal aberta) | `s X w` | `-s X`, `X w-` |
| `d j i y a` | "Dia" com africada | `d j i y a` | `- d`, `j i`, `i ya` |

#### 2. Texto em Português (Recomendado para iniciantes)

Digite palavras normalmente e o phonemizer converterá automaticamente:

| Entrada | Fonemas Gerados | Aliases |
|---------|-----------------|---------|
| `casa` | `k a z a` | `-k a`, `a z`, `z a` |
| `mão` | `m @ w` | `-m @`, `@ w-` |
| `queijo` | `k e i j u` | `-k e`, `e i`, `i j`, `j u` |
| `tchau` | `ch a w` | `-ch a`, `a w-` |

#### 3. Entrada X-SAMPA (Recomendado para usuários familiarizados no uso da Pururu PT-BR)

Para usuários familiarizados com X-SAMPA:

| Entrada | Conversão | Resultado |
|---------|-----------|-----------|
| `kaza` | `k a z a` | Casa (sonorizado) |
| `SE4a` | `sh e r a` | Xera |
| `bOla` | `b V l a` | Bóla (aberta) |

### Funcionalidades Avançadas

#### Fallbacks Automáticos

Se um alias não existir, o phonemizer tenta alternativas:

1. **Mapeamentos:** `T` → `ch`, `zh` → `j`, etc.
2. **Vogais abertas:** `é` → `e`, `ó` → `o`
3. **Dash removal:** `V C-` → `V C`
4. **VV fallback:** `a e` → `e` (vogal)

#### Timing Inteligente

O phonemizer ajusta automaticamente o timing dos fonemas:

- **VC transitions:** Posicionadas **antes** da nota (ticks negativos)
- **CV principal:** Posição 0 (início da nota)
- **Ditongos finais:** 70-80% da duração da nota
- **Clusters CC:** Timing curto e rápido (50-65% do base)

### Exemplos Práticos

#### Frase Simples

**Entrada:** `olá mundo`

**Notas:**
1. `o` (C4, 480 ticks)
2. `lá` (D4, 480 ticks)
3. `mun` (E4, 480 ticks)
4. `do` (C4, 960 ticks)

**Resultado:**
```
Nota 1 (o):
  - Phoneme: "- o" @ 0

Nota 2 (la):
  - Phoneme: "o l" @ -120
  - Phoneme: "l a" @ 0

Nota 3 (mun):
  - Phoneme: "a m" @ -120
  - Phoneme: "m Q" @ 0

Nota 4 (do):
  - Phoneme: "Q d" @ -120
  - Phoneme: "d u" @ 0
```

#### Ditongo Nasal

**Entrada:** `pão` (convertido para `p @ w`)

**Nota:** `pão` (C4, 960 ticks)

**Resultado:**
```
- Fonema: "-p @" @ 0
- Fonema: "@ w-" @ 672  (70% de 960)
```

#### Encontro Consonantal

**Entrada:** `prato` (convertido para `p r a t u`)

**Notas:**
1. `pra` (C4, 480 ticks)
2. `tu` (D4, 480 ticks)

**Resultado:**
```
Nota 1 (pra):
  - Fonema: "-p r" @ -78   (cluster, timing curto)
  - Fonema: "r a" @ 0

Nota 2 (tu):
  - Fonema: "a t" @ -120
  - Fonema: "t u" @ 0
```

#### Africada (dj)

**Entrada:** `dia` (pode ser digitado como `d j i y a`)

**Notas:**
1. `dji` (C4, 480 ticks)
2. `ya` (D4, 480 ticks)

**Resultado:**
```
Nota 1 (dji):
  - Fonema: "- d" @ 0  (VC apenas)
  - Fonema: "j i" @ 0  (CV da africada)

Nota 2 (ya):
  - Fonema: "i ya" @ -84  (VCV transition)
```

---

## 🔧 Troubleshooting

### Problemas Comuns

#### 1. "Alias não encontrado" / Fonema mudo

**Sintomas:**
- Nota não produz som
- Mensagem de erro no console

**Soluções:**
- ✅ Verifique se o **alias existe** no `oto.ini`
- ✅ Confira a **ortografia** do alias (underscores, dash, etc.)
- ✅ Teste o **fallback** digitando o fonema alternativo (ex: `ch` em vez de `T`)
- ✅ Adicione o **alias manualmente** ao `oto.ini`

#### 2. Transições abruptas / Cliques

**Sintomas:**
- Sons de "clique" ou "pop" entre notas
- Transições não suaves

**Soluções:**
- ✅ Ajuste o **Overlap** no `oto.ini` (aumente para 30-50ms)
- ✅ Verifique o **Preutterance** (deve estar na vogal)
- ✅ Certifique-se que **VV/VC transitions** estão configurados
- ✅ Use **crossfade** nas notas do OpenUtau

#### 3. Pronúncia incorreta

**Sintomas:**
- Palavra sintetizada soa errada
- Fonema não é o esperado

**Soluções:**
- ✅ **Digite fonemas diretamente e COMO É FALADO/CANTADO** em vez de texto (ex: `k a z a` em vez de `casa`)
- ✅ Use **X-SAMPA** se familiarizado (ex: `kaza` para "casa")
- ✅ Verifique **mapeamentos automáticos** (c→k/s, x→sh, etc.)
- ✅ Teste **espaços** entre fonemas para entrada manual

#### 4. Timing incorreto / Fonemas fora da nota

**Sintomas:**
- Fonemas aparecem muito cedo ou tarde
- Sons cortados

**Soluções:**
- ✅ Ajuste **Preutterance** e **Overlap** na `oto.ini`
- ✅ Verifique se **VC transitions** têm ticks negativos
- ✅ Certifique-se que **ditongos finais** estão posicionados corretamente
- ✅ Use notas **mais longas** (mínimo 240 ticks recomendado)

#### 5. Ditongos não funcionam

**Sintomas:**
- `@ w` (ão) soa como duas sílabas
- Glides (w, y) não se conectam

**Soluções:**
- ✅ Certifique-se que gravou **V glide-** (ex: `@ w-`)
- ✅ Configure o timing do **glide no final** da nota (70-80%)
- ✅ Digite **manualmente** `@ w` se automático não funcionar
- ✅ Verifique se o **glide está no oto.ini**

#### 6. Clusters não funcionam

**Sintomas:**
- Encontros como "pr", "bl" soam separados
- Erro de alias não encontrado

**Soluções:**
- ✅ Certifique-se que gravou os **88 clusters**
- ✅ Verifique se os aliases **estão no oto.ini** (ex: `p r`, `-p r`)
- ✅ Use **fallback manual**: digite `p`, depois `r a` separadamente
- ✅ Para clusters não gravados, o phonemizer usa **V C-** + **-C V**

### FAQ

**P: Preciso gravar TODAS as 652 amostras?**  
R: Para um voicebank **completo**, sim. Mas você pode começar apenas com **CVVC** (312 amostras) e adicionar VCV/VV/Clusters depois.

**P: Posso usar símbolos diferentes (X-SAMPA)?**  
R: Sim! O phonemizer aceita X-SAMPA e faz mapeamento automático.

**P: O que fazer se minha voz não alcança um tom consistente?**  
R: Grave em **múltiplos tons** (subbanks) e use `tone_ranges` no `character.yaml`.

**P: Posso gravar apenas vogais orais (não nasais)?**  
R: Tecnicamente sim, mas a síntese de palavras com **nasalização** ficará muito artificial. Recomenda-se gravar ao menos `@` (ã) e `7` (em).

**P: Como lidar com palavras estrangeiras?**  
R: Digite os **fonemas diretamente** usando os símbolos suportados, ou adapte para os fonemas mais próximos do português.

**P: O phonemizer suporta multilíngue?**  
R: Não nativamente, mas você pode **misturar fonemas** manualmente para palavras de outros idiomas.

**P: Posso usar este phonemizer com voicebanks CV simples?**  
R: Não diretamente. Este phonemizer é otimizado para **VCCX**. Para CV simples, use o phonemizer específico para `CV` ou similar.

---

## 📚 Recursos Adicionais

### Links Úteis

- **OpenUtau:** [https://github.com/stakira/OpenUtau](https://github.com/stakira/OpenUtau)
- **Documentação OpenUtau:** [https://github.com/stakira/OpenUtau/wiki](https://github.com/stakira/OpenUtau/wiki)
- **SetParam (Editor de oto.ini):** [https://sourceforge.net/projects/setparam/](https://sourceforge.net/projects/setparam/)
- **Vocal Synth Brasil:** [https://vocal-synth-brasil.fandom.com/](https://vocal-synth-brasil.fandom.com/)

### Ferramentas Recomendadas

- **Audacity** (grátis): Gravação e edição básica
- **Reaper** (trial/pago): DAW profissional
- **SetParam** (grátis): Editor de oto.ini para UTAU
- **Copaiba Lexicon** (grátis): Editor de oto.ini para UTAU
- **OREMO** (grátis): Software especializado para gravação de voicebanks
- **RecStar** (grátis): Software especializado para gravação de voicebanks

### Créditos

- **Phonemizer desenvolvido por:** xiao/xiapingguo
- **Baseado em:** OpenUtau Phonemizer Framework (stakira)
- **Sistema VCCX:** Inspirado em VCCV PT-BR de 2018, VCCV Inglês de 2015 da Czloid

### Como Contribuir

Encontrou um bug? Tem sugestões de melhoria?

1. **Reporte issues** no repositório do projeto
2. **Compartilhe** seus voicebanks criados com este sistema
3. **Contribua** com melhorias no código (Pull Requests)
4. **Ajude** a comunidade no Discord/Fórum

### Licença

Este phonemizer é distribuído sob licença compatível com OpenUtau. Consulte o repositório para detalhes.

---

## 🎉 Conclusão

Parabéns por chegar até aqui! Com esta documentação, você tem tudo o que precisa para:

✅ Entender o sistema fonético VCCX PT-BR  
✅ Gravar um voicebank completo e de qualidade  
✅ Configurar corretamente os arquivos oto.ini  
✅ Usar o phonemizer de forma eficiente  

**Boa sorte com seu voicebank!** 🎤🎶

Se tiver dúvidas, consulte a seção de [Troubleshooting](#troubleshooting), entre em contato comigo pelo Discord (lingwei.zh) ou entre em contato com a comunidade da Vocal Synth Brasil.

---

**Última atualização:** 01/01/2026  
**Versão da documentação:** 1.0
