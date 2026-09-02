# API de Livros

# 📚 API de Gerenciamento de Livros

Este projeto é um trabalho escolar desenvolvido com o objetivo de construir uma **API RESTful funcional para a gestão de um catálogo de livros**, culminando na criação de uma interface web para consumo dos dados. 

O projeto está dividido em etapas para garantir uma evolução estruturada do aprendizado, cobrindo desde a lógica de back-end até a integração com o front-end.

---

## 🛠️ Tecnologias Utilizadas

A arquitetura da aplicação foi desenhada separando claramente as responsabilidades de cada componente tecnológica:

* **Python**: Linguagem de programação base da aplicação.
* **FastAPI**: Framework moderno e rápido para a criação das rotas da API.
* **Uvicorn**: Servidor ASGI que executará a aplicação Python.
* **SQLAlchemy**: Biblioteca ORM para a comunicação abstrata entre a aplicação e o banco de dados.
* **PyMySQL**: Driver Python necessário para realizar a conexão direta com o MySQL.
* **Pydantic Settings**: Gestão, leitura e validação das configurações de ambiente.
* **MySQL**: Sistema de gestão de banco de dados relacional para armazenamento seguro das informações.

> 💡 **Divisão de Responsabilidades:** O **FastAPI** recebe as requisições HTTP do utilizador, o **SQLAlchemy** traduz e organiza o acesso aos dados, e o **MySQL** armazena fisicamente as informações.

---

## 📋 Especificação dos Dados (Modelo)

Inicialmente, cada livro registado na base de dados possuirá a seguinte estrutura de atributos:

* `id`: Identificador numérico único (Chave Primária).
* `titulo`: O título do livro (Texto).
* `autor`: O nome do autor da obra (Texto).
* `ano_publicacao`: O ano em que o livro foi publicado (Inteiro).
* `disponivel`: Indicador boleano se o livro está disponível para empréstimo (Verdadeiro/Falso).

---

## 🚀 Rotas e Operações da API

A API disponibilizará as operações padrão de um CRUD (Create, Read, Update, Delete) através das seguintes rotas:

| Método | Rota | Objetivo |
| :--- | :--- | :--- |
| `POST` | `/livros` | Criar e registar um novo livro |
| `GET` | `/livros` | Listar todos os livros cadastrados |
| `GET` | `/livros/{id}` | Consultar os detalhes de um livro específico por ID |
| `PUT` | `/livros/{id}` | Atualizar as informações de um livro existente |
| `DELETE` | `/livros/{id}` | Excluir um livro do sistema |

### 🌐 Interface do Utilizador (Parte 4)
Na fase final do projeto (Parte 4), será construída uma **interface web utilizando HTML, CSS e JavaScript puro**. Esta interface será executada no navegador e consumirá as rotas listadas acima através de requisições assíncronas (`fetch`).

---

## 🎓 Padrão Didático Adotado

Para facilitar o acompanhamento e a correção académica, o código das Partes 2 e 3 foi escrito seguindo diretrizes estritas de **clareza e simplicidade**, evitando padrões ocultos ou avançados de programação:

* **Funções Explícitas:** Uso exclusivo de funções nomeadas com `def`.
* **Legibilidade:** Variáveis com nomes completos, intuitivos e claros.
* **Fluxo Passo a Passo:** Estruturas de repetição e decisão (`if`, `for`, `try/except`) detalhadas de forma linear.
* **SQLAlchemy Direto:** Consultas escritas de forma explícita para que se entenda o que é pedido ao banco de dados.
* **Sem Atalhos:** Proibido o uso de funções `lambda`, funções anónimas ou compreensões de listas complexas.

O grande objetivo pedagógico deste trabalho é permitir a compreensão total do fluxo: **Receber o dado ➡️ Validar ➡️ Processar no Banco ➡️ Responder ao Utilizador.**

---

## 🛠️ Como Executar o Projeto (Breve Resumo)

*(Nota: Pode personalizar esta secção com os comandos exatos do seu projeto mais tarde)*

1. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
2. Configure as variáveis de ambiente para a ligação ao MySQL.
3. Inicie o servidor Uvicorn:
   ```bash
   uvicorn main:app --reload
   ```

