# VIM

- O Vim é um editor de texto avançado, altamente configurável e poderoso, muito usado no desenvolvimento e edição de scripts, código-fonte, e arquivos de configuração.

- Vim funciona em modo texto, com comandos e modos diferentes para editar, navegar, copiar, colar e muito mais.

---

## Modos principais do Vim:

- **Modo Normal**: modo padrão para navegar e executar comandos.
- **Modo Inserção**: para digitar texto (ativa com `i`).
- **Modo Visual**: para selecionar blocos de texto (ativa com `v`).
- **Modo Comando**: para executar comandos do Vim (ativa com `:`).

---

## Comandos básicos no modo Normal

| Comando  | Descrição                   |
| -------- | --------------------------- |
| `i`      | Entrar no modo inserção     |
| `Esc`    | Voltar para o modo normal   |
| `:w`     | Salvar arquivo              |
| `:q`     | Sair do Vim                 |
| `:wq`    | Salvar e sair               |
| `dd`     | Deletar a linha atual       |
| `yy`     | Copiar a linha atual        |
| `p`      | Colar após o cursor         |
| `/texto` | Procurar "texto" no arquivo |
| `u`      | Desfazer última alteração   |
| `Ctrl+r` | Refazer alteração desfeita  |

**NOTA :** Para um apredizado mais dinamico sugiro seguir o tutorial do próprio Vim, digitando no shell `vimtutor`

---

## Configurações úteis para melhorar o Vim (sem plugins)

Você pode criar ou editar o arquivo `~/.vimrc` e adicionar essas linhas para melhorar sua experiência:

```vim
" Ativa a numeração das linhas para facilitar a navegação
set number
set relativenumber

" Destaca a linha onde o cursor está para melhor localização visual
set cursorline

" Destaca as ocorrências da última busca automaticamente
set hlsearch

" Faz a busca ser case insensitive, a menos que use maiúsculas na busca
set ignorecase
set smartcase

" Mostra correspondência de parênteses quando você posiciona o cursor próximo
set showmatch

" Usa indentação automática baseada no arquivo
set autoindent
set smartindent
set tabstop=4       " Número de espaços que um TAB ocupa
set shiftwidth=4    " Número de espaços usados para indentação
set expandtab       " Usa espaços em vez de tabs

" Permite rolagem suave com o cursor no final do arquivo
set scrolloff=5

" Permite que o Vim use o clipboard do sistema para copiar e colar (se suportado). Para saber sua versão do vim tem suporte, dentro do vim, entre no modo normal e digite :echo has('clipboard') se a saída for 1, entao tem suporte, se for 0, nao tem suporte.
set clipboard=unnamedplus

" Permite remapear a combinaçao de tecla usada pelo vim para copiar, para a boa e velha combinaçao que todo mundo conhece Ctrl + C
vnoremap <C-c> "+y

```

---
