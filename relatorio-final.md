#relatorio final-dupla Pedro henrique e Lucas Simoes
## O que aprendemos 
Ao finalizar um trabalho como este, aprende-se a diferença prática e visual entre as propriedades display: block, inline e inline-block do CSS. Fica claro como LLMs podem ser usados como ferramentas eficientes para gerar código base, experimentar variações e, principalmente, para identificar e depurar bugs de layout. O processo também reforça a importância de um fluxo de trabalho estruturado e da validação visual para garantir que o código funcione como esperado, simulando um ciclo de desenvolvimento colaborativo.
## diferenças de LLMs
A principal diferença é o propósito: o primeiro código é uma aplicação prática de um layout de cards, enquanto o segundo é um material didático.

O primeiro usa textos genéricos apenas para compor o visual. Já o segundo possui um conteúdo explicativo que ensina sobre as próprias tags <div> e <span>. O uso do <span> reflete isso: o primeiro agrupa ícone e texto, enquanto o segundo o usa para destacar palavras em uma frase. Em suma, um é um componente pronto e o outro é uma aula

## erros comuns e correçoes
1. Erro Conceitual: Não Entender Por Que width e height Não Funcionam
Erro Comum: Aplicar width, height ou margin-top/bottom a um elemento <span> (ou outra tag inline) e não ver nenhuma mudança visual. Isso acontece porque, por padrão, elementos inline não aceitam dimensões verticais; eles apenas ocupam o espaço do seu conteúdo.

Correção: Este é o ponto central do seu experimento. A correção é mudar a propriedade display do elemento.

Use display: block; para que ele se comporte como uma <div> (ocupa a largura toda e aceita dimensões).

Use display: inline-block; para o "melhor dos dois mundos": ele permite definir width e height, mas permanece na mesma linha que outros elementos.

2. Erro de Conexão: O CSS Não Funciona
Erro Comum: Escrever o código CSS corretamente, mas ele não ser aplicado à página HTML. A causa quase sempre é um erro no link entre os arquivos. Nos seus exemplos, um código usava <link rel="stylesheet" href="styles.css" /> e o outro <link rel="stylesheet" href="style.css">.

Correção: Sempre verifique se o nome do arquivo no atributo href do HTML é exatamente igual ao nome do seu arquivo CSS. Qualquer letra diferente, plural (styles vs style) ou erro de digitação quebrará a conexão.