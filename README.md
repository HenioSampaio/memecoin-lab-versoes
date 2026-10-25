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

### 1.8 · 25/10/2026
- Nova tela Mercado: ranking das moedas em alta, das que acabaram de nascer, das que as nossas carteiras mexeram e das que várias compraram juntas, com o gráfico de quem mais subiu e atualização sozinha.
- Página da moeda com gráfico de velas (1m, 5m, 15m, 1h) que se atualiza sozinho, com as nossas compras e vendas marcadas, valor de mercado, liquidez, compras × vendas e checagem de segurança.
- Carteiras refeitas: quem o laboratório está copiando, quem está na geladeira e quem está fora (e por quê), o estilo de cada uma (trader, scalper, robô) e o resultado de copiar.
- Levar para a Phantom (Ajustes): a carteira do laboratório aparece no seu celular e você saca mesmo sem este computador.
- Menos botões repetidos: Radar e Checar moeda viraram parte do Mercado; "Avaliar novas" saiu (a avaliação já é automática).
- Mais dados para aprender: vigia de novo todas as carteiras boas, mas copia só os traders; as outras ficam em observação (o preço é seguido por 4 h e entra no aprendizado, sem mexer no resultado).
- Busca automática junta os rankings de 1, 7 e 30 dias do Kolscan: 88 carteiras em vez de 48.
- Repositório de versões privado: o botão Atualizar usa uma chave de leitura do GitHub (Ajustes › Atualizações).

### 1.7.2 · 25/10/2026
- QR code da carteira do laboratório (Ajustes e Meu saldo › Real), com o passo a passo para mandar SOL pela Phantom do celular.

### 1.7.1 · 24/10/2026
- Só copia traders de verdade: quem segura a moeda pelo menos 5 min (quem sai em 1 min nos usa de saída) e não é robô (robô opera nas 24 h e faz centenas de trocas por dia).
- Geladeira: carteira com 3 prejuízos seguidos para de ser copiada por 6 h.
- Saída mais rápida: perto do alvo ou do stop, ele confere na hora, sem esperar os 20 s da próxima cotação.
- Stop móvel: depois do alvo, sai se cair 30% do pico, em vez de segurar o resto até zerar.
- Opção: segurar quando a carteira copiada vende mas a moeda está subindo forte (Estratégia › Quando vender).
- Fita do Painel arrumada.

### 1.7 · 24/10/2026
- Recomendação automática (Estratégia): o laboratório revive cada operação com o preço real minuto a minuto e testa 200 combinações de venda (alvo, stop, tempo, seguir ou não o líder); também separa por horário, dia, liquidez, idade da moeda, atraso e número de carteiras.
- Só recomenda quando a melhora se repete na maioria dos sorteios estatísticos, com confiança baixa, média ou alta. Ligado, aplica sozinho as de confiança média ou alta, uma por vez, e avisa no Telegram. Tudo tem Desfazer.
- Segue o preço por 4 h também das moedas BARRADAS, para conferir se cada filtro está acertando. Afrouxar filtro nunca é automático.
- Contexto que dá prejuízo passa a ser evitado; no teste, 1 em cada 5 ainda é copiado para ele continuar aprendendo. No dinheiro real, a regra vale sempre.

<!-- NOVIDADES:FIM -->

---

<p align="center">Feito por <b>HBS</b> · <a href="https://github.com/HenioSampaio">github.com/HenioSampaio</a></p>
