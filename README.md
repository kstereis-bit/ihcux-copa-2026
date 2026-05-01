# CopaNaMão — Protótipo de Baixa Fidelidade

> Lista de Exercícios XIII — Interação Humano-Computador e UX  
> Centro Universitário UNA — Prof. Daniel Henrique Matos de Paiva

---

## Integrantes

- Kate Santana Reis

---

## Problema Focado

A maior dor priorizada foi a **perda de lances importantes enquanto o torcedor está fora do assento**, combinada com as **filas imensas nos quiosques de comida**.

Esses dois problemas são interdependentes: o torcedor vai ao quiosque, demora na fila, perde um gol e não pode assistir ao replay de forma imediata. O app CopaNaMão resolve ambos ao mesmo tempo — pedido de comida sem sair do assento e replay disponível na palma da mão.

---

## Justificativa de Design

O protótipo foi organizado seguindo os princípios de **usabilidade sob pressão**:

- **Botões grandes e texto legível**: O torcedor está distraído, com sol no olho e barulho ao redor. Todos os elementos de ação têm área de toque generosa e contraste alto.
- **Hierarquia clara na Home**: O placar ao vivo domina o topo (informação mais urgente), seguido pelos 4 atalhos rápidos em grid 2x2 e o botão de emergência ao final.
- **Navegação fixa por ícones**: A barra inferior com 5 ícones permanece visível em todas as telas, permitindo troca de contexto instantânea sem perder o fluxo.
- **Fluxo de comida em poucos passos**: Cardápio → Adicionar → Carrinho → Pagar. Máximo 4 toques do desejo ao pedido confirmado.
- **Destaque para emergência**: O botão "Ajuda / Segurança" aparece tanto na Home quanto na tela de Perfil, com borda destacada, garantindo visibilidade em situações críticas.

---

## Telas do Protótipo

| # | Tela | Função principal |
|---|------|-----------------|
| 1 | Home / Dashboard | Placar ao vivo + atalhos rápidos para todas as funções |
| 2 | Mapa do Estádio | GPS com posição do usuário, banheiros e portões |
| 3 | Cardápio Digital | Lista de alimentos e bebidas do setor com botão de adicionar |
| 4 | Carrinho / Pagamento | Resumo do pedido, escolha de entrega e pagamento |
| 5 | Central de Replays | Lista de lances recentes com múltiplos ângulos |
| 6 | Perfil / Ingresso | QR Code do ingresso, identificação do setor e botão de emergência |

---

## Fluxo do Usuário

### Pedir um lanche

1. Na **Home**, toca no atalho **"Pedir"**
2. Na tela de **Cardápio**, navega pelas categorias (Lanches / Bebidas / Doces)
3. Toca no botão **"+"** para adicionar itens ao carrinho
4. Toca em **"Ver Carrinho"**
5. Na tela de **Carrinho**, escolhe entre *Retirar no local* ou *Entregar no assento*
6. Seleciona a forma de pagamento (Pix ou Cartão) e toca em **"Confirmar Pedido"**
7. Recebe **notificação push** quando o pedido está pronto

### Ver um replay

1. Na **Home**, toca no atalho **"Replay"**
2. Na **Central de Replays**, vê a lista de lances em ordem cronológica inversa
3. Toca no lance desejado (ex: GOL 72')
4. Escolhe o ângulo de câmera preferido
5. Assiste ao clipe curto sem sair do aplicativo

---

## Reflexão de IHC

> "Em um estádio, o brilho do sol e o barulho são ruídos externos constantes. Como seu layout de baixa fidelidade garante que o usuário não se perca no fluxo enquanto comemora um gol?"

O design responde a essa realidade com três estratégias: (1) **retomada fácil** — a barra de navegação inferior sempre visível permite ao torcedor voltar ao ponto certo após qualquer interrupção; (2) **confirmações explícitas** — cada ação importante (pedido confirmado, replay iniciado) gera feedback visual imediato; (3) **hierarquia implacável** — o que é urgente (placar, emergência) está sempre no topo ou em destaque, nunca enterrado em menus.

---

## Estrutura do Repositório

```
ihcux-copa-2026/
├── prototipo/
│   ├── prototipo.png
│   └── prototipo.pdf
└── README.md
```

---

## Desafio Extra (Opcional)

### Modo Acessibilidade
Tela com comandos de voz: botão central de microfone ocupando 40% da tela, feedback por vibração e áudio sintetizado confirmando cada ação. Comandos possíveis: *"Pedir hot dog"*, *"Onde fica o banheiro"*, *"Ver último gol"*.

### Fluxo de Emergência
O botão **"Ajuda / Segurança"** (disponível na Home e no Perfil) envia automaticamente a localização exata do assento (Setor + Fileira + Assento) para os fiscais do estádio via GPS, com confirmação na tela e código de protocolo de atendimento.
