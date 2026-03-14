# 🚀 Projeto de Integração Contínua (CI) com Python e Docker

Este projeto demonstra a implementação de um fluxo de **CI (Continuous Integration)** completo. O objetivo é garantir que cada alteração no código seja testada automaticamente e transformada em uma imagem Docker pronta para uso.

## 🛠️ Tecnologias Utilizadas

*   **Linguagem:** [Python 3.13](https://www.python.org)
*   **Testes:** [Pytest](https://docs.pytest.org) para automação de testes unitários.
*   **Containerização:** [Docker](https://www.docker.com) para criar ambientes isolados e reprodutíveis.
*   **Automação (CI):** [GitHub Actions](https://github.com) para rodar a esteira de testes e deploy.
*   **Registro de Imagens:** [Docker Hub](https://hub.docker.com) para armazenar a imagem final.

## ⚙️ Como o Fluxo Funciona

Toda vez que um `git push` é realizado para este repositório, o GitHub Actions inicia automaticamente os seguintes passos:

1.  **Setup:** Cria um ambiente virtual com a versão correta do Python.
2.  **Instalação:** Instala todas as dependências necessárias.
3.  **Testes:** Executa o `pytest` para verificar se o código está funcionando como esperado.
4.  **Build & Push:** Se os testes passarem, o robô cria uma imagem Docker e a envia automaticamente para o meu Docker Hub.

## 📦 Como rodar o projeto

Se você tiver o Docker instalado, pode baixar e rodar a versão mais recente deste projeto diretamente do Docker Hub com o comando:

```bash
docker pull heloisaamaralmafra/ci-sum-python:latest
docker run heloisaamaralmafra/ci-sum-python
