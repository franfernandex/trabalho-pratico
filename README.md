- Descrição do Projeto

Este repositório contém a solução para o problema de otimização de rotas de ônibus, cujo objetivo é minimizar a maior distância entre dois pontos consecutivos no percurso. O algoritmo desenvolvido lê um arquivo com uma instância de teste e retorna um arquivo salvo com o resultado do melhor tour encontrado, além dos resultados da execução (melhor solução, pior solução, valor médio das soluções e tempo médio de execução).

Foi aplicado um algoritmo heurístico de vizinho mais próximo com um fator de aleatoriedade (alpha) para introduzir variação na busca por caminhos. Iniciando de um ponto de origem (ponto 0), a cada iteração é escolhido o vizinho mais próximo do último ponto inserido no tour e, ao mesmo tempo, o mais próximo do vértice inicial, ponderando esses critérios pelo fator alpha, um parâmetro randômico entre 0 e 0,5. Quando todos os pontos são visitados, a busca retorna ao ponto inicial.

Após a geração da solução, é calculada a distância máxima entre dois pontos consecutivos do percurso, definindo a qualidade da solução, sendo a melhor aquela com a menor distância máxima.

- Estrutura de Arquivos

main.py: Implementação principal do algoritmo.

instances/: Diretório contendo as instâncias de teste.

results/: Diretório para armazenar os arquivos de saída.

README.md: Instruções para execução.

- Execução

python3 main.py

Executando o código, é necessário informar primeiro o nome do arquivo da instância e logo após o nome do arquivo que será salvo o melhor tour encontrado pela execução do algoritmo.

Ex: 

Digite o nome da instancia a ser executada:

01.ins

Digite o nome do arquivo a ser salvo o melhor tour encontrado:

resultado.txt