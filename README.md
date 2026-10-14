

# Lúmina — A cor é o seu maior poder

Jogo de plataforma 2D em preto e branco, feito para rodar no navegador (computador e celular). Um mundo sem cor esconde segredos coloridos: a cada orbe que Lúmina encontra, ela evolui, ganha novos poderes e a cor volta aos poucos.

> Estado atual: **Regiões 1 a 3 jogáveis** da Floresta Sombria. A Região 4 e os chefes ainda estão em construção.

---

## Como jogar

### Teclado

| Ação | Teclas |
|---|---|
| Mover | Setas ou **A / D** |
| Pular (pule de novo no ar para o **pulo duplo**) | **Espaço**, seta para cima ou **W** |
| Ataque básico (bolha de ar; com o orbe vermelho, bola de fogo) e interagir (puxar raiz) | **X** (também J, K) |
| Poder do orbe (fumaça de sombra; com o vermelho, jatos incendiários) | **Z** (também C, V, L) |
| Alternar entre orbes (quando tiver mais de um) | **Q** |
| Menu / fechar mapa | **Esc** |

### Celular (botões na tela)

- **◀ ▶** mover, **▲** pular (toque duas vezes para o pulo duplo)
- **◉** ataque básico, **☁** poder do orbe (aparece depois do primeiro orbe)
- **Roda de poderes** (lado esquerdo): toque no orbe do centro para alternar
- **Globo** no canto: abre o mapa. **☰**: menu. **🔊**: liga/desliga o som

> O navegador só toca som depois de um toque ou tecla. Toque uma vez na tela para ativar a música.

---

## Regras do jogo

- **Corações e vidas:** você tem 3 corações. A cada **50 moedas** ganha **+1 vida**; ao zerar os corações, uma vida extra é usada.
- **Orbes protegem a vida:** com um orbe equipado, o golpe tira o **poder primeiro** (você volta à forma pequena) e o orbe cai do céu para ser pego de novo. Orbes extras podem ser guardados (até 2 de reserva).
- **Pedras:** moeda especial (cristais), usada no futuro **Mercado**. Ficam salvas no navegador.
- **Lanternas** (pontos de retorno) acendem ao toque e curam 1 coração.
- **Bandeiras de região** ficam no fim de cada região: salvam o progresso e liberam a região no **Mapa**.
- **Mapa:** escolha a região para continuar. Aparece também ao perder todas as vidas. Mercado, Novos Mundos, Galeria e Missões estão **bloqueados por enquanto**.

---

## Poderes

**Lúmina pequena** começa com a **bolha de ar** (alcance curto, aciona flores e destrói espinhos).

| Orbe | Ataque básico (X) | Poder (Z) | Bloqueados (em breve) |
|---|---|---|---|
| Sem orbe | Bolha de ar | — | — |
| **Negro** (Região 1) | Bolha de ar | Fumaça negra | Nuvem negra (voar), Almas desgarradas (especial) |
| **Vermelho** (Região 3) | Bolas de fogo (no lugar da bolha) | Jatos incendiários | Rastro de fogo, Meteoros (especial) |

A fumaça desfaz **barreiras de sombra** e ativa **símbolos**; o fogo queima **teias**. Cada poder tem usos no cenário, não só contra inimigos.

---

## Regiões

| Região | Áreas | Novidades |
|---|---|---|
| **1** | Limite da Floresta, Trilha das Pedras Baixas, Caminho das Raízes, Clareira do Orbe Negro | Controles, flor e portão, marcas, tronco e alavanca, cipós, árvores com galhos, **Orbe Negro** |
| **2** | Bosque da Fumaça Negra, Pântano das Pedras Afundadas | Barreiras de sombra, plataformas que somem, lama, pedras de passagem, peixes |
| **3** | Ruínas Afundadas, Passagem das Cinzas, Santuário do Orbe Vermelho | Fragmentos da memória, plataformas que racham e móveis, corujas, teias, **Orbe Vermelho** |
| 4 | Retorno pelos Caminhos Queimados… | Em construção |

Obstáculos: espinhos (destrutíveis), plataformas que somem/racham/andam, barreiras de sombra, teias, tronco empurrável, alavanca, cipós para balançar, árvores com galhos, escadas e rampas, lama que machuca e peixes saltando.

Inimigos: aranhas (algumas com escudo), mini aranhas, morcegos, criaturas de sombra, corujas que lançam penas.

---

## Arquivos e estrutura técnica

O jogo é **um único arquivo**:

```
lumina.html
```

- **HTML/CSS:** menu, mapa e botões de toque.
- **JavaScript:** todo o jogo (canvas 2D), com física, câmera, inimigos, fases, mapa e roda de poderes.
- **Imagens:** embutidas em base64 (WebP) dentro do arquivo.
- **Som:** música e efeitos gerados por código (Web Audio), sem arquivos de áudio.
- **Salvamento:** `localStorage` do navegador (chave `lumina_v1`: pedras e regiões liberadas).
- **Tamanho:** cerca de 4,7 MB.

Para jogar, abra `lumina.html` no navegador (Chrome, Edge, Firefox ou Safari atuais).

### Publicar

- **itch.io ou site próprio:** envie o `lumina.html` (ou um `.zip` com ele renomeado para `index.html`).
- **App de celular:** pode ser empacotado depois (por exemplo, PWA ou Capacitor).

---

## Próximos passos

- Região 4 e os 4 chefes (Aranha Gigante, Coruja Real, Senhora das Sombras, Colosso de Cristais).
- Poderes bloqueados (nuvem, almas, rastro de fogo, meteoros) e especiais com recarga de 5 minutos.
- Mercado (compra com pedras), Galeria, Missões e Novos Mundos.
- Orbes de água, natureza, luz, sombra roxa e a **fusão dos elementos** (as artes já estão no arquivo, ainda não conectadas ao jogo).
- Opcional: separar em `index.html`, `game.js`, `style.css` e `assets/` para edição mais fácil.

---

## Observações

- O jogo foi testado por simulação automática, mas **não passou por teste completo de jogabilidade**: dificuldade e ritmo ainda podem precisar de ajuste.
- Algumas animações (pernas, capa, cipós) são efeitos aplicados sobre imagens únicas. Quadros separados de braços e pernas melhorariam o movimento.

## Créditos

- **Direção, ideias e arte:** você.
- **Código do jogo:** feito em conversa com o Claude (Anthropic).
