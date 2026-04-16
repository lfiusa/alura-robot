# 🤖 Organo - Testes Automatizados com Robot Framework

Suite de testes E2E para a aplicação **Organo**, cobrindo o cadastro de colaboradores via formulário com dados gerados dinamicamente em pt_BR.

---

## 🗂️ Estrutura do Projeto

```
├── resources/
│   ├── main.robot                    # Importações globais
│   ├── shared/setup_teardown.robot   # Abertura e fechamento do navegador
│   └── pages/cadastro.robot          # Keywords e variáveis do formulário
├── tests/
│   ├── preenchimento_correto.robot   # Cenários com dados válidos
│   └── preenchimento_incorreto.robot # Cenários com campos obrigatórios vazios
```

---

## ✅ Casos de Teste

| Cenário | Descrição |
|---|---|
| Criação de 1 card | Preenche o formulário e verifica o card no time esperado |
| Múltiplos cards | Verifica criação de mais de um card no mesmo time |
| Card em cada time | Cria 1 card nos 7 times disponíveis (Programação, Front-End, Data Science, DevOps, UX e Design, Mobile, Inovação e Gestão) |
| Campos obrigatórios | Valida mensagens de erro ao submeter o formulário vazio |

---

## 🛠️ Tecnologias

- [Robot Framework](https://robotframework.org/)
- [SeleniumLibrary](https://robotframework.org/SeleniumLibrary/)
- [FakerLibrary](https://guykisel.github.io/robotframework-faker/) - locale pt_BR
- Python 3.x + Google Chrome

---

## 🚀 Como Executar

> A aplicação Organo deve estar rodando em `http://localhost:3000`

```bash
# Instalar dependências
pip install robotframework robotframework-seleniumlibrary robotframework-faker

# Executar todos os testes
robot tests/

# Executar uma suíte específica
robot tests/preenchimento_correto.robot
```

Os relatórios `log.html`, `report.html` e `output.xml` são gerados automaticamente na raiz do projeto.
