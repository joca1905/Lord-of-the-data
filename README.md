# Lord of the data
Sua ferramenta para revisão sistemática de artigos científicos.
![Logo do programa](./imagens/data_of_data.jpg)
## 📘 Introdução

### O que é o software?

**Lord of the Data** é uma ferramenta desenvolvida para auxiliar no processo de revisão sistemática. Ela incrementa ferramentas que facilitam a seleção, extração e entendimento de artigos científicos, com um diferencial importante: o uso de modelos de **inteligência artificial** para sumarização e análise textual. Além disso, é um software **brasileiro**, com foco em acessibilidade e facilidade de uso.

### Público-alvo

Este software é destinado a **alunos, pesquisadores e entusiastas** interessados no processo de revisão sistemática.

### Requisitos do sistema

- **Sistema operacional:** Windows  
- **Memória RAM:** 8 GB  
- **Espaço em disco:** (a definir)  
- **Outros requisitos:** (a definir)  

---

## 📁 Baixando o projeto

1. Vá até esta página do GitHub.
2. Para fazer o código funcionar o usuário vai precisar de três arquivos que se encontram nesse repositório: `requeriments.txt`,  `data_of_data.ico` e `Lord_of_the_data.py`.
3. O software foi desenvolvido em Python, por isso, é necessário, caso o usuário não possua, instalar a linguagem de programação python. Entre as diversas maneiras nas quais se pode fazer isso, recomenda-mos duas: por prompt de comando ou usando o compilador Visual Studio Code (Vs code).
---

## Usando o CMD (Prompt de Comando):

### 🐍 Instalando o Python

1. Acesse o site oficial: https://www.python.org/downloads/
2. Clique no botão **Download Python 3.12.0** (versão utilizada nos testes).
3. **Importante:** durante a instalação, marque a opção **"Add Python to PATH"**.
4. Clique em **Install Now** e aguarde o fim da instalação.
5. Abra o menu Iniciar e digite: **cmd** → pressione Enter.
6. No terminal, vá até a pasta do projeto. Exemplo:

```bash
cd C:\Users\SeuUsuario\Downloads\pasta-do-projeto
```
7. Instale as bibliotecas necessárias com o comando:

```bash
pip install -r requirements.txt
```

### ▶️ Executando o programa
1. Ainda no terminal, digite:

```bash
python Lord-of_the_data.py
```

## Usando o Visual Studio Code (VS Code):

### 🧠 Instalando o Visual Studio Code

1. Acesse: https://code.visualstudio.com/
2. Clique em **Download for Windows**
3. Instale com as opções padrão
4. Após a instalação, abra o VS Code

### 🧩 Instale a extensão Python no VS Code

1. No VS Code, clique no ícone de quadradinhos no menu lateral esquerdo (Extensões)
2. Busque por **"Python"**
3. Instale a extensão oficial da Microsoft
4. Clique em File > Open Folder... e escolha a pasta do projeto que você extraiu.
5. O VS Code vai abrir todos os arquivos do projeto
6. Pressione `Ctrl + Shift + P` (ou `F1`) no VS Code
7. Digite e selecione: `Python: Select Interpreter`
8. Escolha o Python que você instalou (geralmente aparece como `Python 3.x.x`)
9. No Terminal integrado do VS Code, digite o seguinte comando:

```bash
pip install -r requirements.txt
```
10. Abra o arquivo principal do seu projeto (por exemplo, `Lord-of_the_data.py`).
11. Clique no botão Run (ícone de play) no canto superior direito ou pressione `F5` para rodar o código.
   
## 🎯 Objetivos do programa

- **Automatizar a revisão sistemática**, facilitando a coleta, filtragem e organização de artigos científicos.
- **Fornecer ferramentas de análise e extração de dados**, identificando padrões e informações relevantes.
- **Garantir transparência e reprodutibilidade**, permitindo replicar metodologias de revisão.

---

## 🔧 Funcionalidades Principais

### Visão geral da interface

A interface é composta por sete menus:

- Home
- Configurações
- Revisão Sistemática
- Execução
- Sumarização
- Perguntas e Respostas
- Tradução

![Interface do Software](./imagens/Fig1rs.png)

---

### 🏠 Home

Apresentação do programa, incluindo:

- **Logo**: um mago simbolizando poder sobre dados.
- **Título e subtítulo**
- **Versão e autor**

---

### ⚙️ Configurações

Permite:

- **Salvar/carregar dados** da revisão
- Escolher o formato de saída (DOCX ou LaTeX)
- Alternar entre **modo claro e escuro**
- Selecionar tipo de citação (**ABNT ou Harvard**)

![Menu de Configuração](./imagens/Fig2rs.png)

---

### 📚 Revisão Sistemática

Coleta dados da revisão, como:

- Título, autores, objetivo
- Critérios de inclusão/exclusão
- Palavras-chave, strings de busca
- Informações sobre editoras e idioma

![Revisão Sistemática](./imagens/Fig3rs.png)

---

### ▶️ Execução

Importa arquivos `.ris` e `.bib` e extrai metadados automaticamente. Utiliza o modelo [distilbert-base-uncased-distilled-squad](https://huggingface.co/distilbert/distilbert-base-uncased-distilled-squad) para responder perguntas como:

- Qual é a principal contribuição deste estudo?
- Como e por que foi conduzido?
- Quais são os principais resultados?

O sistema mostra respostas com **porcentagem de confiança**, e permite ao usuário aceitar/rejeitar artigos com base em critérios definidos.

![Execução](./imagens/Fig4rs.png)  
![Resultado da Execução](./imagens/Fig9rs.png)  
![Janela de Seleção](./imagens/Fig8rs.png)

---

### 📝 Sumarização

Permite resumir textos usando o modelo [Falconsai/text_summarization](https://huggingface.co/Falconsai/text_summarization) (T5 Small), gerando resumos concisos com base no conteúdo inserido.

![Sumarização](./imagens/Fig5rs.png)

---

### ❓ Perguntas e Respostas

Responde perguntas personalizadas sobre textos inseridos, usando o mesmo modelo da etapa de execução.

![Perguntas e Respostas](./imagens/Fig6rs.png)

---

### 🌐 Tradução

Permite a tradução de textos de artigos para o idioma desejado (português, inglês e espanhol).

![Tradução](./imagens/Fig7rs.png) 

---

## 🧪 Status do Projeto

:construction: Em desenvolvimento.  
Sinta-se à vontade para abrir *issues* ou enviar *pull requests*!

---

## Modelos de IA utilizados

Este projeto utiliza modelos de linguagem e ferramentas acessadas por meio da biblioteca `transformers` da Hugging Face, todos sob licenças permissivas como Apache 2.0 e MIT.

- **Perguntas e Respostas:**  
  [`distilbert/distilbert-base-uncased-distilled-squad`](https://huggingface.co/distilbert/distilbert-base-uncased-distilled-squad)  
  Acessado via Hugging Face Transformers  
  Licença: [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0), que permite o uso, modificação e redistribuição, desde que a licença original seja incluída.

- **Sumarização de Texto:**  
  [`Falconsai/text_summarization`](https://huggingface.co/Falconsai/text_summarization)  
  Acessado via Hugging Face Transformers  
  Licença: [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0), que permite o uso, modificação e redistribuição, desde que a licença original seja incluída.

- **Tradução de Texto:**  
  [Argos Translate](https://github.com/argosopentech/argos-translate)  
  Modelos utilizados disponíveis em: [https://www.argosopentech.com/models/](https://www.argosopentech.com/models/)  
  Licença: [MIT](https://opensource.org/licenses/MIT), que permite uso, cópia, modificação, fusão, publicação, distribuição, sublicenciamento e/ou venda do software, desde que seja mantido o aviso de copyright.

### Observações

- Os modelos são utilizados **exclusivamente por meio da API da Hugging Face** ou bibliotecas licenciadas.
- **Nenhum peso de modelo é redistribuído neste repositório**. Os modelos são baixados dinamicamente no dispositivo do usuário, conforme necessário.
- Recomendamos que usuários consultem os repositórios originais para mais informações sobre licenciamento e termos de uso.

## 👨‍💻 Autores

**Joaquim Osterwald Frota Moura Filho** – (joaquim.eng1905@gmail.com)  
Desenvolvedor e pesquisador em inteligência artificial e revisão sistemática.

**Giovanni**

**George**

**Amora**

---

## 📄 Licença

Este projeto está licenciado sob a Licença Creative Commons Atribuição - Não Comercial 4.0 Internacional (CC BY-NC 4.0). Você pode copiar, modificar, distribuir e executar o material para fins não comerciais, desde que atribua a autoria. O uso comercial requer permissão explícita do autor.

Veja o arquivo [LICENSE](./LICENSE) para mais detalhes.
