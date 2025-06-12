# EVE – Assistente Virtual IA para Windows

## Visão Geral

A EVE é uma Inteligência Artificial Assistente Virtual projetada para sistemas operacionais Windows, desenvolvida principalmente em Python 3.11. Seu objetivo é simplificar a interação do usuário com o computador através de comandos de voz e texto, automatizando tarefas, gerenciando arquivos, integrando-se a serviços externos e oferecendo uma experiência personalizada e contextual. A EVE busca ser uma ferramenta eficiente e intuitiva para aumentar a produtividade e a acessibilidade no ambiente Windows.

## Tecnologias Base

*   **Python 3.11:** Linguagem de programação principal.
*   **Reconhecimento de Fala (STT):** Utiliza `Vosk` para processamento offline e pode integrar-se a APIs de nuvem (ex: Google Cloud Speech-to-Text) para maior acurácia.
*   **Síntese de Fala (TTS):** Emprega `pyttsx3` para geração de voz offline, aproveitando os motores de fala do Windows.
*   **Processamento de Linguagem Natural (PLN):** Baseado em `spaCy` para reconhecimento de intenção, extração de entidades e gerenciamento de diálogo.
*   **Interface Gráfica (GUI):** Desenvolvida com `PySide6` (Qt for Python), garantindo uma interface moderna e responsiva.
*   **Interação com Windows:** Utiliza `pywin32` e `psutil` para controle direto do sistema operacional.
*   **Gerenciamento de Dependências:** `Poetry` para um gerenciamento robusto e determinístico.

## Como Iniciar

Siga estas instruções para configurar e executar a EVE em seu ambiente de desenvolvimento local.

### Pré-requisitos

*   Python 3.10 instalado (verifique com `python --version`)
*   Git instalado
*   Poetry (recomendado para gerenciamento de dependências) ou pip

### Instalação

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/MurilloSanttos/eve-virtual-assistant.git
    cd eve-virtual-assistant
    ```

2.  **Instale as dependências:**

    **Usando Poetry (Recomendado):**
    ```bash
    poetry install
    ```
    Isso criará um ambiente virtual e instalará todas as dependências definidas em `pyproject.toml`.

    **Usando pip:**
    ```bash
    python -m venv .venv
    .venv\Scripts\activate # No Windows CMD/PowerShell
    # ou source .venv/bin/activate # No Git Bash/WSL
    pip install -r requirements.txt
    ```

3.  **Baixe os modelos de linguagem para spaCy (se usar pip):**
    ```bash
    # Se você instalou spaCy via pip, baixe um modelo de português
    python -m spacy download pt_core_news_sm
    ```

### Executando a EVE

**Com Poetry:**
```bash
poetry run python src/main.py
```

**Com ambiente virtual padrão (pip):**
```bash
.venv\Scripts\activate # Ative o ambiente virtual
python src/main.py
```

## Contribuição

Agradecemos seu interesse em contribuir com o projeto EVE! Siga estas diretrizes:

1. **Fork** o repositório e **clone** seu fork.
2. Crie uma **branch de feature** a partir da branch `develop` (ex: `git checkout -b feature/minha-nova-funcionalidade develop`).
3. Faça suas alterações e **commits** com mensagens claras e descritivas.
*   **Padrão de Mensagem de Commit**: `tipo(escopo): descrição breve` (ex: `feat(nlu): adicionar reconhecimento de nova intenção`). Tipos comuns: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`.
4. Certifique-se de que seus testes passem e adicione novos testes para suas alterações, se aplicável.
5. Execute o linter (`flake8`) e o formatador (`black`) antes de commitar:
```bash
poetry run flake8 src/ tests/
poetry run black src/ tests/
```
6. Envie suas alterações para o seu fork.
7. Abra um **Pull Request (PR)** da sua branch de feature para a branch `develop` do repositório principal.
8. Descreva detalhadamente suas alterações no PR e aguarde a revisão do código.

## Licença

Este projeto está licenciado sob a **Licença MIT**. Veja o arquivo `LICENSE` para mais detalhes.

## Contato

Para dúvidas, sugestões ou colaborações, entre em contato com a equipe do projeto:

*   **Email: muriilloosanttos@gmail.com**
*   **GitHub Issues: https://github.com/MurilloSanttos/eve-virtual-assistant/issues**
