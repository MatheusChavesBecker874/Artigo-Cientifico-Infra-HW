#Benchmark de IA Generativa com CPU e GPU

Este repositório contém os artefatos experimentais utilizados no artigo sobre o impacto da Computação de Alto Desempenho (HPC) no desenvolvimento de inteligências artificiais generativas e suas repercussões no mercado de tecnologia.

#Objetivo

O experimento tem como objetivo comparar o desempenho de um modelo generativo de linguagem executado em CPU e GPU, avaliando o impacto da aceleração por hardware na inferência de IA generativa.

#Modelo utilizado

O modelo utilizado foi o DistilGPT-2, disponibilizado pela biblioteca Hugging Face Transformers. A escolha desse modelo ocorreu por seu tamanho reduzido, permitindo execução em ambiente acessível, como o Google Colab.

#Metodologia

Foram definidos 10 prompts textuais fixos. Cada prompt foi executado 10 vezes em CPU e 10 vezes em GPU, totalizando 100 execuções por dispositivo.

Em cada execução, o modelo foi configurado para gerar até 50 novos tokens. As métricas coletadas foram:

tempo de geração;
tokens gerados por segundo;
média;
desvio-padrão;
intervalo de confiança de 95%.

#Resultados principais

A CPU apresentou tempo médio de geração de 1,9128 segundos, enquanto a GPU apresentou tempo médio de 0,2529 segundos.

Com isso, a GPU obteve ganho de 7,57 vezes em relação ao tempo médio e reduziu o tempo de geração em aproximadamente 86,78%.

Além disso, a CPU obteve média de 26,70 tokens por segundo, enquanto a GPU alcançou média de 184,17 tokens por segundo.

#Arquivos
benchmark_ia_hpc.ipynb: notebook com o código do experimento;
resultados_benchmark.csv: resultados individuais de cada execução;
resumo_benchmark.csv: resumo estatístico dos resultados;
grafico_tempo_cpu_gpu.png: gráfico de tempo médio;
grafico_tokens_cpu_gpu.png: gráfico de tokens por segundo.

#Como reproduzir
Abrir o notebook benchmark_ia_hpc.ipynb no Google Colab.
Ativar GPU em Ambiente de execução > Alterar tipo de ambiente de execução > Acelerador de hardware > GPU.
Executar todas as células do notebook.
Ao final, os arquivos CSV e os gráficos serão gerados automaticamente.
