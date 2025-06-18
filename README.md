# Exemplos de LLM com LangChain e LangGraph

Este repositório reúne dois notebooks auto-explicativos que demonstram, em Python, como criar aplicações com modelos de linguagem (LLMs) usando as bibliotecas **LangChain** e **LangGraph**.

## Conteúdo

### `exemploslangchain.ipynb`

* carregamento de chave no `.env` (`python-dotenv`);
* criação de um `ChatOpenAI` e uso de `PromptTemplate`;
* montagem de uma `LLMChain` simples (“Qual é a capital da França?”);
* ideias de **memória de conversa** e cadeias mais complexas (map-reduce, refine);
* esboço de integração com *vector stores* (Faiss ou Chroma) para RAG.

### `exemploslanggraph.ipynb`

* definição de um esquema de estado com o campo `messages`;
* inclusão de um nó “chatbot” alimentado por um modelo (`AzureChatOpenAI` no exemplo);
* bordas condicionais para decidir se o diálogo continua ou termina;
* visualização do grafo e exemplo de expansão com ferramentas externas.

## Requisitos

Python ≥ 3.10. Instale as dependências principais:

    pip install python-dotenv jupyter \
                langchain-openai langchain-core langchain-community \
                langgraph

Para o caderno do LangGraph há comandos de upgrade dentro dele (`!pip install -U …`); execute-os quando aberto pela primeira vez.

## Configuração de credenciais

Crie um arquivo `.env` na raiz do projeto contendo:

    OPENAI_API_KEY=<sua-chave-aqui>

O `load_dotenv()` presente nos notebooks carrega a variável automaticamente.  
> O arquivo `.env` está listado no `.gitignore` para evitar exposições acidentais.

## Como usar

    # 1. clone o repositório e entre na pasta
    git clone https://github.com/ksassaki1/llm.git
    cd llm

    # 2. (opcional) crie um ambiente virtual, instale requisitos e adicione o .env

    # 3. inicie o Jupyter
    jupyter lab

Abra cada notebook, execute as células na ordem e experimente ajustar os prompts ou as regras do grafo.

## Licença

Distribuído sob a licença MIT — consulte o arquivo `LICENSE` para detalhes.

Desfrute dos exemplos e fique à vontade para abrir *issues* ou *pull requests* caso queira sugerir melhorias.
