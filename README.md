# Endless Calculator — RPG Simulator

Página independente para calcular vida dos bosses da Endless, dificuldade por wave e Endless Coins.

## Publicar no GitHub Pages

1. Crie um repositório novo chamado **`endless-calculator`** no GitHub. Para usar o GitHub Pages grátis, deixe-o público.
2. Envie `index.html` para a raiz deste repositório.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`, depois salve.
6. Quando a publicação terminar, a página deverá estar em:
   <https://darkstar600000sacrificio-dot.github.io/endless-calculator/>

## Link para colocar na wiki Fandom

```wikitext
== Endless Calculator ==
[https://darkstar600000sacrificio-dot.github.io/endless-calculator/ Endless Calculator — Boss HP & Endless Coins]
```

## Fórmulas implementadas

- Dificuldade do boss na wave `W` (múltiplo de 10): `D% = 19 × (W / 10) − 9`
- Vida estimada do boss: `HP = 300B × (1 + 1.25 × (D / 100) × players)`
- Dificuldade após derrotar o boss: `D_after = D_before + 10` pontos percentuais
- Endless Coins totais até a wave `W`: `3 × W × (W + 10) / 200`
- Coins daquela wave: `Coins_total(W) − Coins_total(W − 10)`
- Bônus de fim de semana: `×1.5`; bônus de coins `×2`; ambos ativos: `×3`

A calculadora formata automaticamente a vida com unidades abreviadas, incluindo B, T, Qa e unidades superiores.

> As fórmulas são o modelo estimado com base nos valores observados no jogo; ajuste o código se novos testes demonstrarem outra regra.
