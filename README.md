# 🖥️ Node.js CLI — FS, Path & OS

Aplicação de linha de comando em Node.js utilizando **ES Modules** que agrupa exercícios práticos dos módulos nativos `fs`, `path` e `os`.

---

## 📋 Pré-requisitos

- Node.js **v14+** (ES Modules requerem v14 ou superior)
- Recomendado: Node.js v18+

---

## 🚀 Como rodar

```bash
# Clone o repositório
git clone https://github.com/VBubols/NODE_OS_PATH_FS.git

# Entre na pasta
cd NODE_OS_PATH_FS

# Rode o programa
node main.js
```

---

## 🗂️ Estrutura de pastas

```
├── main.js                        # Entrada principal — menu interativo
│
├── FileSystem/
│   ├── main.js                    # Re-exporta todas as funções de FS
│   ├── Ex01/leitorLog.js          # Leitor de logs
│   ├── Ex02/geradorRelatório.js   # Gerador de relatórios
│   ├── Ex03/organizadorArquivos.js# Organizador de arquivos
│   └── Ex04/contadorPalavras.js   # Contador de palavras
│
├── Path/
│   ├── main.js                    # Re-exporta todas as funções de Path
│   ├── Ex05/normalizadorCaminhos.js # Normalizador de caminhos
│   ├── Ex06/estruturarProjetos.js   # Criador de estrutura de projeto
│   └── Ex07/validarExtensoes.js     # Validador de extensões
│
├── OS/
│   ├── main.js                    # Re-exporta todas as funções de OS
│   ├── Ex08/monitor.js            # Monitor do sistema
│   ├── Ex09/ambiente.js           # Relatório do ambiente
│   └── Ex10/compararAmbientes.js  # Comparador de ambientes
│
└── CLI_backup_automatizado/
    └── backup_auto.js             # Backup automático de arquivos .txt
```

---

## 📦 Módulos utilizados

| Módulo | Uso |
|--------|-----|
| `fs/promises` | Leitura, escrita, cópia e organização de arquivos |
| `node:path` | Manipulação e normalização de caminhos |
| `node:os` | Informações do sistema operacional |
| `node:readline` | Interface interativa no terminal |

---

## 🗃️ Funcionalidades

### FileSystem (`fs`)
| # | Função | Descrição |
|---|--------|-----------|
| 1 | Leitor de logs | Lê um arquivo `.txt` e conta o número de linhas |
| 2 | Gerador de relatórios | Gera um relatório em JSON com dados do ambiente |
| 3 | Organizador de arquivos | Move arquivos `.txt` para uma pasta separada |
| 4 | Contador de palavras | Conta as palavras de um arquivo de texto |

### Path
| # | Função | Descrição |
|---|--------|-----------|
| 5 | Normalizador de caminhos | Normaliza caminhos com `path.normalize` |
| 6 | Criador de estrutura de projeto | Cria uma estrutura de pastas de projeto |
| 7 | Validador de extensões | Valida as extensões dos arquivos em uma pasta |

### OS
| # | Função | Descrição |
|---|--------|-----------|
| 8 | Monitor do sistema | Exibe plataforma, arquitetura, memória e processador |
| 9 | Relatório do ambiente | Gera um relatório `.txt` com informações do sistema |
| 10 | Comparador de ambientes | Identifica o sistema operacional em uso |

---

## 🔧 CLI Backup Automatizado

Utilitário independente que:
- Detecta o diretório do usuário com `os.homedir()`
- Cria uma pasta `backup` no diretório home caso não exista
- Copia todos os arquivos `.txt` da pasta `origem` para o backup
- Gera um relatório com data, quantidade de arquivos copiados e tamanho total

```bash
node CLI_backup_automatizado/backup_auto.js
```

---

## 📝 Observações

- O arquivo `relatorio.txt` gerado pelo programa é ignorado pelo `.gitignore` pois é um arquivo de saída dinâmica.
- Todos os caminhos de arquivo usam `import.meta.url` para garantir portabilidade entre sistemas operacionais.
