# k-nearest-neighbors
## Algoritmo simples para o problema K Nearest Neighbors(KNN) em Python puro
---
### Proposta:
Proposto como projeto de conclusão do primeiro módulo do curso de Ciência de Dados da Ada Tech, esse código teve como desafio montar uma solução em Python puro para o problema do K-ésimo Vizinho Mais Próximo, aplicado a um cenário de investidores e seus perfis de investimento. Isto é, a partir dos investidores já cadastrados, prever o perfil de investimentos de novos investidores.

---

### Contexto inicial:

Inicialmente temos uma lista de investidores. Cada investidor era representado por uma lista. O primeiro elemento dessa lista, é o CPF como indentificador único, o segundo, uma string determinando seu perfil de investimentos, podendo ser 'Conservador', 'Moderado' ou 'Agressivo', e o terceiro elemento é uma tupla com 4 valores de investimentos.

Exemplo:
~~~
[66707599984, 'Conservador', (5100., 3500., 1400., 200.)]
[54850120580, 'Moderado', (7000., 3200., 4700., 1400.)]
[47432932248, 'Agressivo', (6300., 3300., 6000., 2500.)]
~~~

---

### Solução:

Implementei a função classifica_investidor(), que recebe como parâmetros, a tupla de investimentos e o número K de vizinhos com o qual a análise será feita. Quanto mais vizinhos forem usados para comparação, mais precisa será a previsão. Essa função calcula, usando Pitágoras, a distância entre o item alvo da análise e seus K vizinhos mais próximos. A conclusão é tirada a partir do perfil da maioria dos viznhos mais próximos, e sua proximidade com o alvo, proximidade essa que também serve como critério de desempate para o caso de um item apresentar quantidades iguais de vizinhos com perfis diferentes.

Nesse repositório também se encontra um notebook com o gabarito da análise, constatando que o script conseguiu, com essa amostra pequena, prever todos os casos corretamente.

---

Esse projeto foi implementado por mim, [Paulo Jennings](https://github.com/PauloSJennings), com a orientação do professor [Tiago Marto](https://github.com/tiagomarto). Valeu, mestre!
