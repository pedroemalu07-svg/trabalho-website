# trabalho-website
## Passo 3: Simulação de Bugs e Correções

Neste passo, simulamos um ciclo de desenvolvimento onde um código com bugs foi gerado e, em seguida, corrigido com o auxílio de um LLM.

### 1. Criação do Código com Bugs (`codigo-com-bugs.html`)

A Pessoa B introduziu intencionalmente 4 problemas comuns de CSS:
1.  **Seletor CSS Inválido:** Um seletor com vírgula (`.classe, h2`) em vez de um seletor de descendência (`.classe h2`).
2.  **Layout Flexbox Incorreto:** `divs` que deveriam ser empilhadas apareceram lado a lado porque faltava a propriedade `flex-direction: column`.
3.  **`width` em Elemento Inline:** Tentativa de aplicar largura a um `<span>`, que foi ignorada.
4.  **`margin-top` em Elemento Inline:** Tentativa de aplicar margem superior a um `<span>`, que também foi ignorada.

### 2. Correção via LLM (`correcoes.html`)

A Pessoa A utilizou o "Prompt 7" para solicitar que o LLM encontrasse e corrigisse os bugs.

### 3. Validação

O arquivo `correcoes.html` foi aberto no navegador e as correções foram validadas com sucesso:
- **Seletor:** O título `<h2>` foi estilizado corretamente, sem afetar outros elementos.
- **Layout Flexbox:** Os cards agora estão empilhados verticalmente como esperado.
- **Elemento `<span>`:** O LLM alterou o `<span>` para `display: block`, o que resolveu os problemas de `width` e `margin-top`, fazendo com que o elemento se comportasse como um bloco. A correção foi eficaz e bem comentada.

O processo foi concluído com sucesso.
 
papéis (quem fez o quê):passo 1 e 2-Pedro Henrique, passo 3 e 4-Lucas Simoes

LLMs e versões:Gemini e Perplexity

instruções para abrir os arquivos.-todos os codigos estarao na pasta meu-projeto-div-span e o  prompt-log.md e o comparativo-llms.md estao na pasta docstrabalho
