```markdown
# Autoencoders vs Variational Autoencoders

Este repositório reúne o código, os slides e o relatório desenvolvidos para o trabalho da disciplina de Redes Neurais (NES), cujo objetivo foi comparar o comportamento de um Autoencoder clássico com um Variational Autoencoder (VAE) utilizando o dataset Fashion-MNIST. Todo o material busca apresentar, de forma clara e prática, como cada modelo lida com reconstrução, compressão e estruturação do espaço latente.

## Objetivos do Projeto

- Implementar um Autoencoder denso com espaço latente de 32 dimensões.
- Implementar um Variational Autoencoder (VAE) com latente 2D para permitir visualização direta.
- Comparar a qualidade das reconstruções entre AE e VAE.
- Visualizar o espaço latente aprendido pelo VAE, incluindo geração de imagens amostradas.
- Produzir um relatório técnico (duas páginas) e slides explicativos em LaTeX/Beamer.
- Consolidar o estudo de modelos gerativos simples e prepará-lo como base para arquiteturas mais avançadas.

## Estrutura do Repositório



├── autoenconder.ipynb          # Notebook com todo o código do projeto
├── autoenconderslides.pdf      # Slides da apresentação
├── relatorioautoenconders.pdf  # Relatório final em prosa
├── enunciado (1).pdf           # Enunciado original do trabalho
├── README.md                   # Este arquivo
├── LICENSE                     # Licença MIT
└── .gitignore



## Descrição do Código

O notebook organiza todo o processo em etapas:

1. **Importações e preparação**
   - NumPy, Matplotlib, TensorFlow/Keras e SciPy.
   - Configuração de seeds para reprodutibilidade.

2. **Carregamento e pré-processamento do dataset**
   - Fashion-MNIST normalizado em [0,1].
   - Achatamento das imagens para redes densas.
   - Separação dos tensores para AE e VAE.

3. **Autoencoder**
   - Encoder: 784 → 256 → 32.
   - Decoder simétrico.
   - Perda: binary crossentropy.
   - Reconstruções mais nítidas e boa fidelidade visual.

4. **Variational Autoencoder**
   - Encoder produz z_mean e z_log_var.
   - Sampling via reparametrização.
   - Perda total = reconstrução + divergência KL.
   - Latente 2D para visualização e geração.
   - Reconstruções mais suaves, porém com latente organizado.

5. **Visualizações**
   - Reconstruções AE e VAE.
   - Geração de amostras via grid no latente (VAE).
   - Scatter 2D das classes no espaço latente.

6. **Resultados principais**
   - AE reconstrói melhor.
   - VAE organiza o latente e permite geração.
   - O trade-off entre fidelidade e capacidade generativa fica evidente.

## Slides

O arquivo PDF apresenta:

- Resumo geral dos modelos.
- Estrutura do código.
- Imagens de reconstrução do AE e do VAE.
- Visualização do espaço latente.
- Comparações diretas e análise das diferenças.
- Limitações observadas e propostas de melhorias futuras.

## Relatório

O relatório sintetiza toda a análise em duas páginas, cobrindo:

- Motivação das escolhas do modelo.
- Explicação conceitual do AE e do VAE.
- Interpretação crítica dos resultados.
- Limitações das arquiteturas densas.
- Recomendações de trabalhos futuros, como Conv-AE, Conv-VAE, β-VAE, VAE-GAN e métricas perceptuais.

## Como Reproduzir

1. Baixar o repositório ou clonar via:
```

git clone [https://github.com/oalmirsergio/Autoencoders-vs-VAE.git](https://github.com/oalmirsergio/Autoencoders-vs-VAE.git)

```
2. Abrir o notebook no Google Colab ou ambiente local com TensorFlow.
3. Executar sequencialmente cada célula.
4. Gerar novamente as imagens e visualizações, se desejado.

## Referências

- Kingma, D. P.; Welling, M. "Auto-Encoding Variational Bayes" (2014).
- Goodfellow, I.; Bengio, Y.; Courville, A. "Deep Learning". MIT Press, 2016.
- Dataset: Fashion-MNIST — Xiao, Han; Rasul, Kashif; Vollgraf, Roland.
- Documentação oficial do TensorFlow/Keras.

## Contato

almirsergio.a@gmail.com
```
