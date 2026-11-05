# Aprendizagem Conexionista de Máquina
## Implementação de Rede Neural de 2 Camadas

Abaixo está a explicação do código para o treinamento de uma rede neural simples utilizando a biblioteca NumPy.

## Arquitetura e Parâmetros

Trata-se de uma rede neural de **2 camadas** com as seguintes especificações:

*   **Tamanho do lote (`N`):** Processa 64 exemplos simultaneamente.
*   **Entrada (`D_in`):** Recebe dados com 1000 dimensões.
*   **Camada oculta (`H`):** Possui 100 neurônios e utiliza a função de ativação Sigmoide.
*   **Camada de saída (`D_out`):** Retorna 10 dimensões (predições).
*   **Ciclos de treino:** O loop executa 2000 iterações.
*   **Taxa de aprendizado:** Definida como `1e-4` (0.0001) para a atualização dos pesos.

## Etapas do Treinamento

O funcionamento do código é dividido em quatro partes principais:

*   **Definição da rede:** Define o tamanho das camadas e inicializa as matrizes de dados de entrada (`x`), saídas alvo (`y`) e os pesos (`w1`, `w2`) com valores aleatórios.
*   **Forward pass (Propagação):** Faz a previsão da rede calculando os valores da camada oculta (usando a função sigmoide) e da saída. Em seguida, calcula o erro (*loss*) comparando o resultado obtido com o alvo esperado.
*   **Cálculo dos gradientes:** Aplica a técnica de *backpropagation* (regra da cadeia) para calcular as derivadas analíticas. Isso determina a contribuição de cada peso no erro total.
*   **Descida de gradiente:** Atualiza os pesos, subtraindo os gradientes multiplicados pela taxa de aprendizado (`1e-4`) para iterativamente minimizar o erro.

## Saída Esperada

A execução deste código imprimirá 2000 linhas no console. Cada linha exibirá o número da iteração (de `0` a `1999`) acompanhado do valor da função de perda (*loss*) daquele momento. Como o objetivo é aprender com os dados, o comportamento esperado é que o valor de *loss* comece alto e diminua progressivamente ao longo das iterações.
