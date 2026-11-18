# 🌍 Weather GPS Data Pipeline & API Automation

> Um pipeline de dados de ponta a ponta (End-to-End) que captura a geolocalização via frontend web, armazena os dados de forma ágil utilizando o ecossistema do Google Forms/Sheets e processa/consome dados meteorológicos em tempo real através de uma API em Python.

---

## 🚀 Sobre o Projeto
Este projeto foi desenvolvido com o objetivo de automatizar a recolha e análise de dados climáticos com base em localizações geográficas específicas. A aplicação integra tecnologias web modernas para recolha de coordenadas de GPS no browser com um script robusto em Python responsável pela limpeza de dados (data cleaning) e consumo da API meteorológica **Open-Meteo**.

---

## ⚙️ Arquitetura e Fluxo de Dados

1. **Frontend (GPS & Web):** Uma página web leve e responsiva (hospedada no GitHub Pages) que utiliza a API nativa de geolocalização do navegador.
2. **Armazenamento (Serverless):** Os dados de latitude, longitude e nome do local são enviados via requisições POST assíncronas diretamente para um formulário/planilha do Google.
3. **Pipeline de Dados & API (Python):** 
   - O script em Python lê a folha de cálculo utilizando **Pandas**.
   - Executa rotinas de **limpeza e tratamento de dados** (resolvendo inconsistências de formatação regional em strings de coordenadas).
   - Realiza requisições `GET` para consumir dados meteorológicos atualizados em tempo real.

---

## 🛠️ Tecnologias e Ferramentas

* **Linguagem:** Python 3.x
* **Manipulação de Dados:** Pandas
* **Requisições HTTP:** Requests
* **Frontend:** HTML5, CSS3, JavaScript (Fetch API / Geolocation API)
* **Infraestrutura / Hospedagem:** GitHub Pages, Google Forms / Google Sheets API
* **API Climática:** [Open-Meteo API](https://open-meteo.com/)

---

## 🔍 Desafios Técnicos & Soluções (Data Cleaning)
Durante a ingestão dos dados vindos da web, identificou-se que valores de coordenadas podiam apresentar inconsistências de formatação regional (ex: múltiplos pontos decimais ou separadores de milhares indesejados, como `-22.913.604`). 

O script foi blindado com tratativas de strings e blocos de segurança (`try-except`) para garantir que os dados sejam higienizados corretamente antes de serem convertidos para `float`, evitando quebra no fluxo de execução da API:

```python
# Exemplo do tratamento de coordenadas implementado no pipeline
lat_str = str(linha['Latitude']).replace(',', '.')
if lat_str.count('.') > 1:
    partes = lat_str.split('.')
    lat_str = partes[0] + '.' + ''.join(partes[1:])
lat = float(lat_str)

git clone [https://github.com/teu-utilizador/teu-repositorio.git](https://github.com/teu-utilizador/teu-repositorio.git)

pip install pandas requests

python pipeline_clima.py

Aqui tens um modelo de **README.md profissional e de alto nível** ("estilo portfólio de destaque") para colocares no teu repositório do GitHub. Ele resume exatamente a arquitetura e os desafios técnicos que superaste hoje no projeto!

Podes copiar o código abaixo, colar num arquivo chamado `README.md` no teu repositório e ajustar os links se necessário:

```markdown
# 🌍 Weather GPS Data Pipeline & API Automation

> Um pipeline de dados de ponta a ponta (End-to-End) que captura a geolocalização via frontend web, armazena os dados de forma ágil utilizando o ecossistema do Google Forms/Sheets e processa/consome dados meteorológicos em tempo real através de uma API em Python.

---

## 🚀 Sobre o Projeto
Este projeto foi desenvolvido com o objetivo de automatizar a recolha e análise de dados climáticos com base em localizações geográficas específicas. A aplicação integra tecnologias web modernas para recolha de coordenadas de GPS no browser com um script robusto em Python responsável pela limpeza de dados (data cleaning) e consumo da API meteorológica **Open-Meteo**.

---

## ⚙️ Arquitetura e Fluxo de Dados

1. **Frontend (GPS & Web):** Uma página web leve e responsiva (hospedada no GitHub Pages) que utiliza a API nativa de geolocalização do navegador.
2. **Armazenamento (Serverless):** Os dados de latitude, longitude e nome do local são enviados via requisições POST assíncronas diretamente para um formulário/planilha do Google.
3. **Pipeline de Dados & API (Python):** 
   - O script em Python lê a folha de cálculo utilizando **Pandas**.
   - Executa rotinas de **limpeza e tratamento de dados** (resolvendo inconsistências de formatação regional em strings de coordenadas).
   - Realiza requisições `GET` para consumir dados meteorológicos atualizados em tempo real.

---

## 🛠️ Tecnologias e Ferramentas

* **Linguagem:** Python 3.x
* **Manipulação de Dados:** Pandas
* **Requisições HTTP:** Requests
* **Frontend:** HTML5, CSS3, JavaScript (Fetch API / Geolocation API)
* **Infraestrutura / Hospedagem:** GitHub Pages, Google Forms / Google Sheets API
* **API Climática:** [Open-Meteo API](https://open-meteo.com/)

---

## 🔍 Desafios Técnicos & Soluções (Data Cleaning)
Durante a ingestão dos dados vindos da web, identificou-se que valores de coordenadas podiam apresentar inconsistências de formatação regional (ex: múltiplos pontos decimais ou separadores de milhares indesejados, como `-22.913.604`). 

O script foi blindado com tratativas de strings e blocos de segurança (`try-except`) para garantir que os dados sejam higienizados corretamente antes de serem convertidos para `float`, evitando quebra no fluxo de execução da API:

```python
# Exemplo do tratamento de coordenadas implementado no pipeline
lat_str = str(linha['Latitude']).replace(',', '.')
if lat_str.count('.') > 1:
    partes = lat_str.split('.')
    lat_str = partes[0] + '.' + ''.join(partes[1:])
lat = float(lat_str)

```

---

## 💻 Como Executar o Projeto

1. **Clone o repositório:**
```bash
git clone [https://github.com/teu-utilizador/teu-repositorio.git](https://github.com/teu-utilizador/teu-repositorio.git)

```


2. **Instale as dependências necessárias:**
```bash
pip install pandas requests

```


3. **Execute o script de automação no Jupyter Notebook ou IDE de sua preferência:**
```bash
python pipeline_clima.py

```



---

## 👨‍💻 Autor

Desenvolvido por **Rodrigo Cézar Amaral**

[LinkedIn](https://www.google.com/search?q=https://www.linkedin.com/in/rodrigocezaramaral) | [GitHub](https://www.google.com/search?q=https://github.com/DevSold)

```

```
