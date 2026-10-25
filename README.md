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

### 2.7 · 25/10/2026
- Carteiras › carteira que está "fora" › Copiar mesmo assim (por minha conta): ela entra na cópia do teste mesmo sem passar nas regras (veredito, tempo segurando, robô); no dinheiro real continua valendo só "ok p/ testar". Aparece como "copiando por sua conta" e dá para desfazer; a geladeira continua valendo.
- Robô x pessoa mais justo: conta MOEDAS diferentes por hora, não trocas. Quem vende cada moeda em várias partes (ex.: Yami, 330 trocas em 32 moedas) deixou de ser marcado como robô; robô continua sendo quem entra numa moeda nova a cada 3 min, não dorme ou gira 1 a 3 moedas sem parar (robô de volume). Com isso 13 carteiras voltaram a ser copiáveis.

### 2.6 · 25/10/2026
- Telegram: escreva o nome da moeda (ex.: bonk), use /moeda ou cole o endereço. Vem a ficha com nota de confiança de 0 a 100 (🟢🟡🔴) e os motivos, cada um contando uma vez: filtros de segurança, verificada, movimento orgânico, liquidez, idade, concentração, insiders e quantas das nossas carteiras compraram.
- Avisos ao vivo mais leves: o nó manda centenas de avisos por segundo de robôs com transação que falhou; agora eles são descartados sem ler a mensagem inteira (11x mais rápido, conferido com 6 mil avisos reais).

### 2.5 · 25/10/2026
- Teste-sombra (Estratégia): cada compra vista e não copiada (só observada ou barrada) vira uma operação simulada com as suas regras de venda sobre o preço real das 4 h seguintes. Compara copiadas × observadas × barradas e diz se escolher traders e filtrar está valendo a pena. São ~30x mais dados que só as copiadas.
- O aprendizado das regras de venda usa também as sombras das carteiras observadas: chega muito mais rápido às 20 operações para recomendar com confiança (a tela mostra quantas são do teste e quantas são sombras).
- Muito mais leve: o banco ganhou índices. A tela Carteiras abria em 12 s (e travava o resto do programa nesse tempo); agora abre em 0,1 s. A avaliação de carteiras e a partida do laboratório também ficaram mais rápidas.
- Mercado: busque a moeda pelo nome ou símbolo (ex.: bonk), não só pelo endereço. A lista aparece enquanto você digita, com foto, valor de mercado, liquidez, idade, variação do dia e ✓ nas verificadas; tocou, abre o gráfico.

### 2.4 · 25/10/2026
- Conexão ao vivo mais estável: as carteiras observadas são divididas em conexões de até 80 (o nó público recusava centenas numa só), a assinatura vai aos poucos e, se cair, ele espera cada vez mais para reconectar (5 s, 10 s, 20 s… até 1 min) em vez de insistir a cada 5 s.
- Depois de uma queda, a recuperação das observadas olha só as moedas que temos (antes buscava o histórico das 200 a cada queda e sobrecarregava o nó, que caía de novo). Os traders copiados continuam com recuperação completa.
- Sem enxurrada de "erro lendo…" no registro: falha na recuperação vira um aviso só, e erro de leitura diz o motivo (limite de pedidos, demora, servidor).
- Garimpo: só escolhe moedas que dá para ler até o começo (não gasta mais 45 mil leituras para pular a moeda) e olha também as moedas novas que subiram nas últimas 6 h.

<!-- NOVIDADES:FIM -->

---

<p align="center">Feito por <b>HBS</b> · <a href="https://github.com/HenioSampaio">github.com/HenioSampaio</a></p>
