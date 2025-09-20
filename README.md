# Futures Literacy

Este projeto foi reorganizado para facilitar a manutenção e organização do material das aulas.

## Estrutura de Arquivos

```
futures-literacy-class-notes/
│
├── src/
│   ├── main.tex               # Arquivo principal (compilar este)
│   │
│   ├── content/               # Todo o conteúdo do documento
│   │   ├── course-info.tex    # Informações do curso e introdução
│   │   ├── sintese-final.tex  # Síntese final e bibliografia
│   │   └── lessons/           # Aulas organizadas por capítulos
│   │       ├── aula01.tex     # Conteúdo da Aula 1
│   │       ├── aula02.tex     # Conteúdo da Aula 2
│   │       ├── aula03.tex     # Conteúdo da Aula 3 (para futuras aulas)
│   │       ├── aula04.tex     # Conteúdo da Aula 4 (para futuras aulas)
│   │       └── aula05.tex     # Conteúdo da Aula 5 (para futuras aulas)
│   │
│   ├── config/                # Configurações e formatação
│   │   └── preamble.tex       # Configurações, pacotes e estilos
│   │
│   └── assets/                # Recursos adicionais
│       ├── images/            # Imagens, diagramas e figuras
│       └── bibliography/      # Arquivos de bibliografia (.bib)
│
└── README.md                  # Este arquivo
```

## Como Usar

### Para compilar o PDF completo:

```bash
cd src
pdflatex main.tex
```

**Ou a partir da raiz do projeto:**

```bash
pdflatex ./src/main.tex
```

### Para editar conteúdo:

- **Informações gerais do curso**: Edite `src/content/course-info.tex`
- **Conteúdo de uma aula específica**: Edite o arquivo correspondente em `src/content/lessons/`
- **Configurações visuais**: Edite `src/config/preamble.tex`
- **Síntese e conclusões**: Edite `src/content/sintese-final.tex`
- **Imagens**: Adicione em `src/assets/images/`
- **Bibliografia**: Adicione arquivos .bib em `src/assets/bibliography/`

## Vantagens desta Estrutura

1. **Organização modular**: Cada tipo de conteúdo tem sua pasta específica
2. **Separação de responsabilidades**:
   - `config/` → formatação e configurações
   - `content/` → todo o conteúdo textual
   - `assets/` → recursos como imagens e bibliografia
3. **Manutenibilidade**: Mudanças podem ser feitas em arquivos específicos
4. **Reutilização**: As configurações podem ser reutilizadas em outros projetos
5. **Colaboração**: Múltiplas pessoas podem trabalhar em seções diferentes
6. **Versionamento**: Histórico de mudanças mais granular no Git
7. **Escalabilidade**: Fácil adicionar novas aulas, imagens ou referências

## Caixas Disponíveis

O documento inclui as seguintes caixas personalizadas:

- `\begin{slidecontent}` - Para conteúdo dos slides
- `\begin{professorquote}` - Para falas importantes do professor
- `\begin{keypoint}` - Para conceitos chave
- `\begin{thinkerquote}` - Para citações de pensadores e filósofos

## Comandos Personalizados

- `\destaque{texto}` - Destaca texto em azul
- `\sectionbreak` - Adiciona separador visual entre seções
- `\marginnota{texto}` - Adiciona nota na margem
