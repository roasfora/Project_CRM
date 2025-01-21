# Análise RFM - Aula 06 (CRM)

## Descrição
Este projeto tem como objetivo demonstrar o uso da **análise RFM** para segmentação de clientes com base em suas interações e transações. A análise RFM é uma técnica amplamente utilizada no gerenciamento de relacionamento com clientes (**CRM**) para identificar padrões de comportamento e criar estratégias de marketing direcionadas.

### Como funciona a análise RFM?
- **Recência (R):** Dias desde a última compra.
- **Frequência (F):** Número de transações realizadas.
- **Monetário (M):** Valor total gasto pelo cliente.

### Pontuações RFM:
- As métricas R, F e M são divididas em categorias de 1 a 5 (quintis):
  - Recência: 5 (mais recente) a 1 (menos recente).
  - Frequência: 5 (mais frequente) a 1 (menos frequente).
  - Monetário: 5 (maior valor gasto) a 1 (menor valor gasto).

### Segmentação:
Clientes são classificados em diferentes grupos, como:
- **Cliente Top:** Recente, frequente e de alto valor (RFM 555).
- **Recém-Ativo:** Alta recência.
- **Cliente Frequente:** Alta frequência.
- **Grande Gastador:** Alto valor monetário.
- **Cliente Comum:** Engajamento e gasto médios.

---

## Estrutura do Projeto
- **Carregamento dos Dados:** Importa e visualiza o dataset fornecido.
- **Preparação dos Dados:** Realiza o pré-processamento, incluindo tratamento de valores ausentes e criação de métricas adicionais.
- **Cálculo das Métricas RFM:** Gera os valores de Recência, Frequência e Monetário para cada cliente.
- **Atribuição de Pontuações:** Divide as métricas RFM em quintis e combina em um score RFM.
- **Segmentação de Clientes:** Classifica os clientes com base no score RFM.
- **Visualização dos Resultados:** Apresenta a distribuição dos segmentos em gráficos e exporta os dados processados.

---

## Pré-requisitos
- Python 3.x
- Bibliotecas utilizadas:
  - `pandas`
  - `matplotlib`
  - `datetime`

---

## Como Executar o Notebook
1. **Obter os Dados:**
   Certifique-se de que o arquivo `crm.csv` está disponível no mesmo diretório do notebook ou ajuste o caminho no código.

2. **Executar o Notebook:**
   - No Google Colab: Carregue o arquivo `.ipynb` e o dataset `crm.csv`.
   - No Jupyter Notebook ou VS Code: Abra o arquivo e execute as células sequencialmente.

3. **Exportar os Resultados:**
   Os resultados serão salvos no arquivo `rfm_resultados.csv`.

---

## Exemplos de Uso
1. **Análise dos Segmentos:**
   O código fornece a contagem de clientes em cada segmento:
   ```python
   print(rfm['Segmento'].value_counts())
