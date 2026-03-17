# Backtracking

A medida que vai explorando o ambiente, o robo cria um mapa interno das rotas exploradas. Caso uma rota nao gere solucao, outro caminho e escolhido ate que a solucao seja obtida ou nao existam mais opcoes.

São criados labirintos com exatamente 1 entrada e ate 1 saída, com tamanho máximo de 100 x 100 posições. Pode não haver rota possível, mas se existir uma saída, ela está sempre na borda do labirinto e não é o ponto de partida.

## Formato de arquivo de entrada

```text
#NL
[Largura] [Altura]
M0,0 ... M0,L-1
...
MA-1,0 ... MA-1,L-1
```

Onde:

* 0 = espaço
* 1 = parede
* X = partida

## Exemplo de entrada

```text
2
5 4
1 1 1 1 1
1 0 0 0 1
1 0 X 1 1
1 1 0 1 1
3 4
1 1 1
1 X 1
1 0 1
1 1 1
```

## Formato de arquivo de saída

A rota é descrita pelas coordenadas visitadas.

## Exemplo de saída

```text
L0:INI@2,2|F->1,2|D->1,3|BT@1,3->1,2|E->1,1|T->2,1|BT@2,1->1,1|BT@1,1->1,2|BT@1,2->2,2|T->3,2|FIM@3,2
L1:INI@1,1|T->2,1|BT@2,1->1,1|FIM@-,-
```

---
