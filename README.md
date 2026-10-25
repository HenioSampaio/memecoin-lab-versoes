<p align="center">
  <img src="docs/icone.png" width="88" alt="">
</p>
<h1 align="center">Memecoin Lab</h1>
<p align="center">
  Copia as carteiras que mais lucram com memecoins na Solana, <b>primeiro em papel</b>,<br>
  e só deixa usar dinheiro de verdade quando o teste provar que dá lucro para quem copia.
</p>
<p align="center">
  <a href="https://github.com/HenioSampaio/memecoin-lab-versoes/releases/latest/download/MemecoinLab.exe"><img alt="Baixar o MemecoinLab.exe" src="https://img.shields.io/badge/Baixar-MemecoinLab.exe-F6851B?style=for-the-badge&logo=windows11&logoColor=white"></a>
  <a href="https://github.com/HenioSampaio/memecoin-lab-versoes/releases/latest"><img alt="Versão mais nova" src="https://img.shields.io/github/v/release/HenioSampaio/memecoin-lab-versoes?style=for-the-badge&label=vers%C3%A3o&color=661800"></a>
  <img alt="Windows 10 e 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?style=for-the-badge">
  <img alt="Telegram" src="https://img.shields.io/badge/avisos-Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white">
</p>

<p align="center"><img src="docs/tela-painel.png" width="860" alt="Memecoin Lab: painel com o lucro do teste ao vivo"></p>

## O que ele faz

- **Acha carteiras boas sozinho:** todo dia pega o top do Kolscan, lê o histórico real de cada carteira na blockchain e descarta isca, sniper, bot e quem só mostra o lucro e esconde o prejuízo.
- **Copia em papel, com preço de verdade:** quando uma carteira aprovada compra, o laboratório "compra" junto com atraso, taxa e slippage reais (cotação Jupiter), e vende pelas regras: lucro em 2x, stop, tempo e quando o líder vende.
- **Barra moeda perigosa:** dono que ainda pode criar moedas ou congelar, liquidez baixa, 10 maiores com quase tudo, criador com muito.
- **Radar:** avisa quando várias carteiras sem ligação compram a mesma moeda.
- **Aprende:** carteira que dá prejuízo para quem copia é pausada sozinha.
- **Dinheiro real só depois do portão:** 4 semanas, 200 operações e lucro depois das taxas. Mesmo ligado, tem teto por compra, por dia e botão de parar tudo.
- **Telegram:** avisos de compra e venda, painel com botões, vender pelo celular com confirmação, resumo às 21h.

## Instalar

1. Baixe o **MemecoinLab.exe** pelo botão acima.
2. Clique com o botão direito no arquivo → **Propriedades** → marque **Desbloquear** → **OK**.
3. Abra. Se aparecer *"O Windows protegeu o computador"*, clique em **Mais informações → Executar assim mesmo** (o programa não é assinado por empresa).
4. Siga a tela de boas-vindas: chave grátis do Helius, carteiras e ligar o laboratório.

Não precisa instalar Python nem mais nada. Versões novas aparecem sozinhas: **Atualizar agora**, e ele reabre na versão nova.

## Como ele decide

```mermaid
flowchart TB
    subgraph A["🔎 1 · ACHAR · sozinho, todo dia"]
        direction LR
        K["Kolscan<br/>top do mês"] --> S["Scout<br/>lucro REAL na blockchain"] --> V{{"isca? sniper?<br/>bot? prejuízo?"}}
    end
    subgraph B["⚡ 2 · COPIAR · em segundos"]
        direction LR
        L["Carteira aprovada<br/>compra"] --> F{{"Filtros<br/>de segurança"}} --> C["Compra no teste<br/>(ou real, com teto)"]
    end
    subgraph D["💰 3 · VENDER · pelas regras"]
        direction LR
        T["2x: vende metade"] ~~~ X["−40%: stop"] ~~~ Y["120 min: sai"] ~~~ Z["líder vendeu: sai"]
    end
    subgraph E["🧠 4 · APRENDER"]
        direction LR
        RR[("resultado de cada<br/>carteira copiada")] --> P["pausa quem dá<br/>prejuízo a quem copia"]
    end
    A --> B --> D --> E
    E -. lista melhor .-> A

    classDef passo fill:#F6851B,stroke:#661800,color:#fff
    classDef check fill:#EAC2FF,stroke:#661800,color:#3D065F
    classDef guarda fill:#fef3c7,stroke:#d97706,color:#78350f
    class K,S,L,C,T,X,Y,Z,P passo
    class V,F check
    class RR guarda
```

| | Tela | O que mostra |
|:-:|---|---|
| 📈 | **Painel** | Lucro e prejuízo ao vivo, gráfico, posições com termômetro do stop ao alvo, fita do que está acontecendo. |
| 📡 | **Radar** | Moedas que várias das suas carteiras compraram juntas. |
| 👛 | **Carteiras** | Quem é vigiado, a nota de cada uma e a busca automática. |
| 🛡️ | **Checar moeda** | Cole o endereço e veja se passa nos filtros e os sinais sociais. |
| 🎛️ | **Estratégia** | Quando vender, filtros e tamanho das entradas, com análise de risco. |

| Carteiras | Estratégia |
|---|---|
| <img src="docs/tela-carteiras.png" alt="Carteiras e busca automática"> | <img src="docs/tela-estrategia.png" alt="Estratégia com análise de risco"> |

> [!WARNING]
> **Memecoins são de altíssimo risco.** A maioria vai a zero e a maioria de quem copia carteiras perde dinheiro. O programa existe para **medir antes de arriscar**. Não é recomendação de investimento.

<!-- NOVIDADES:INICIO -->
## Novidades

### 2.2 · 25/10/2026
- Recomendação mais clara: mostra só o que muda (ex.: Stop −20% → −40%), o efeito em média por operação e por que a confiança é baixa ou alta.
- Mudanças na estratégia mostram o que mudou em cada vez; Desfazer só na mais recente (desfazer uma antiga misturaria as regras).
- Celular: os botões Teste/Real e o período do gráfico não saem mais da tela; textos de Ajustes, Estratégia e das janelas quebram a linha em vez de cortar com "…"; campos de PIN cabem na tela; seletores (cores, movimento) descem para a linha de baixo.
- Ajustes › Instalar o Tailscale avisa que no computador ele precisa de administrador; sem isso, o acesso de fora é pelo bot do Telegram.
- Botões lado a lado nunca quebram o texto em duas linhas: se não cabem, descem inteiros; seletores um pouco mais altos para tocar.

### 2.1 · 25/10/2026
- Garimpo na blockchain (Carteiras › ⛏️ Garimpar, e junto da busca automática): pega as moedas que mais subiram em 24 h, lê na blockchain quem comprou pelo menos 3x mais barato que o preço de agora (pulando os robôs do primeiro minuto) e manda essas carteiras para a avaliação de lucro real. Acha trader que nenhum ranking mostra.
- PIN de segurança de 6 números: pedido para sacar e para mostrar a chave da carteira (criado na primeira vez; 5 erros travam por 15 min). Troca em Ajustes › Dinheiro real.
- Carteira do laboratório em cartão: saldo grande em SOL e reais, endereço curto com Copiar e QR, e Retirar / Levar para a Phantom como botões lado a lado.
- Mais fotos de moedas: se a fonte da foto falha, tenta de novo e busca a cópia do DexScreener; a tela não guarda mais "sem foto" por 1 hora (a foto aparece assim que existir).

### 2.0 · 25/10/2026
- Toque numa operação fechada (Painel › Últimas operações ou no Raio-x) e veja tudo dela: o caminho do preço com as marcações, a linha do tempo, cada venda nossa em SOL e reais, como estava a moeda na entrada (idade, liquidez, concentração, quanto o líder comprou, nosso atraso) e o que a moeda fez DEPOIS que saímos (saímos cedo ou saímos bem).

### 1.9.9 · 25/10/2026
- Carteiras › Colar uma lista aceita links (solscan.io/account/…, gmgn.ai, birdeye), um por linha, além do endereço puro.

<!-- NOVIDADES:FIM -->

---

<p align="center">Feito por <b>HBS</b> · <a href="https://github.com/HenioSampaio">github.com/HenioSampaio</a></p>
