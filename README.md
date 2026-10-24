# PROJETO INTEGRADOR — CIÊNCIA DE DADOS

##  Tema do Projeto
### Saúde Mental no Trabalho no Setor de Tecnologia

---

##  Descrição do Projeto

Este projeto integrador tem como foco a engenharia, tratamento e preparação de dados relacionados à saúde mental no ambiente corporativo da área de tecnologia. Com o aumento da pressão por entregas ágeis e a constante necessidade de atualização profissional, distúrbios psicológicos (como estresse crônico e ansiedade) tornaram-se tópicos críticos de gestão.

A proposta consiste em extrair dados reais de pesquisas globais e aplicar técnicas rigorosas de limpeza, normalização e tradução, transformando dados brutos em um conjunto de dados estruturado e confiável para fins analíticos.

---

##  Objetivos da Análise

*  **Padrões:** Preparar a base para identificação de sintomas recorrentes de ordem psicológica na área de TI.
*  **Impacto:** Estruturar dados que correlacionem o bem-estar dos colaboradores com a produtividade no ambiente de trabalho.
*  **Cruzamento de Dados:** Permitir a análise de fatores demográficos (idade, país) confrontados com o suporte organizacional oferecido pelas empresas.
*  **Prontidão para BI:** Disponibilizar um arquivo final otimizado para a alimentação direta de relatórios e dashboards em ferramentas de Data Viz.

---

##  Base de Dados

Os dados foram coletados a partir de um mapeamento global disponibilizado publicamente:
👉 [Acessar Dataset Original (Mental Health in Tech Survey) no Kaggle](https://www.kaggle.com/code/chaitanya99/mental-health-in-tech-survey-eda)

O dataset original reúne respostas de questionários aplicados a profissionais de tecnologia, abordando histórico pessoal de saúde mental, facilidade de acesso a tratamentos médicos e a percepção dos funcionários sobre o suporte psicológico oferecido por seus empregadores.

---

##  Processamento de Dados (ETL)

A pipeline de processamento foi construída no **Google Colab** utilizando a linguagem **Python** e a biblioteca **Pandas**:

1. **Extração:** Carga e leitura estruturada do arquivo bruto (`survey.csv`).
2. **Transformação:**
   * **Localização:** Tradução completa de cabeçalhos (colunas) e registros textuais para o português.
   * **Normalização:** Conversão de respostas booleanas (ex: de `"Yes"/"No"` para `"Sim"/"Não"`).
   * **Tratamento de Nulos:** Substituição de valores ausentes ou vazios por rótulos padronizados (`"S/N"` ou `"Sem Informações"`).
   * **Sanitização:** Limpeza de outliers e dados impossíveis (valores incoerentes de idade ou localizações geográficas inválidas).
   * **Redução de Dimensionalidade:** Remoção de colunas com textos livres irrelevantes (como caixas de comentários abertos).
3. **Carga:** Salvamento e exportação do arquivo limpo e otimizado no formato `survey_Dados_Tratados.csv`.

---

##  Estrutura do Projeto

```text
├── Projeto_Integrador_Ciencia_de_dados.ipynb  # Notebook Python com os scripts de ETL
├── survey.csv                                 # Base de dados bruta (Kaggle)
├── survey_Dados_Tratados.csv                  # Base de dados final limpa e localizada
├── LICENSE                                    # Licença de uso do repositório
└── README.md                                  # Documentação do projeto
```

---

##  Resultado Obtido

O projeto entregou com sucesso um ecossistema de dados totalmente higienizado e traduzido para a língua portuguesa. A eliminação de ruídos e dados espúrios garante que qualquer análise descritiva posterior ou modelo estatístico preditivo construído sobre essa base tratada possua alto grau de precisão e fidelidade à realidade.

---

##  Referência

Trabalho desenvolvido como parte integrante das atividades práticas obrigatórias do **Projeto Integrador da Faculdade Senac**.
