# PAA-LISTA2

Repositório contendo a lista de exercícios (arquivo principal `lista2.tex`) da disciplina "Projeto e Análise de Algoritmos" em LaTeX.

### Estrutura
- `lista2.tex` — arquivo fonte LaTeX com todas as questões e respostas.
- `.gitignore` — ignora artefatos de build do LaTeX (logs, aux, pdf, etc.).

### Pré-requisitos
- Distribuição TeX instalada (TeX Live ou MiKTeX) no Windows.
- (Opcional) VS Code com extensão LaTeX Workshop.
- Ferramentas de linha de comando: `pdflatex` e/ou `latexmk`.

### Como compilar (linha de comando)
Abra o terminal integrado do VS Code (Ctrl+`) ou PowerShell/CMD no diretório do projeto (`c:\dev\PAA-LISTA2`) e execute uma das opções:

- Usando latexmk (recomendado):
```powershell
latexmk -pdf lista2.tex
```

- Usando pdflatex (duas vezes para referências e índices):
```powershell
pdflatex -interaction=nonstopmode -synctex=1 lista2.tex
pdflatex -interaction=nonstopmode -synctex=1 lista2.tex
```

O PDF gerado será `lista2.pdf` no mesmo diretório.

### Como compilar (VS Code + LaTeX Workshop)
1. Abra a pasta do projeto em VS Code.
2. Abra `lista2.tex`.
3. Use o botão de build da extensão LaTeX Workshop ou o comando da paleta: "LaTeX Workshop: Build (or Build with recipe)".
4. Visualize o PDF com o visualizador incorporado da extensão.

### Limpeza de arquivos de build
Para remover artefatos gerados (aux, log, etc.), use:
```powershell
latexmk -c
```
ou apague manualmente arquivos com extensões listadas em `.gitignore`.

### Observações
- Garanta que `pdflatex`/`latexmk` estejam no PATH.
- Se ocorrerem erros de pacote, instale-os via MiKTeX/TeX Live package manager.