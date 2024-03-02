# PowerShell
<a name="under-construction" href="https://github.com/mateusdn"><img src="uc.png" /></a>



## PowerShell - Tópicos
* [Introdução](#Introdução)
  * [PowerShell CLI](#PowerShell-CLI)
  * [PowerShell ISE](#PowerShell-ISE)
  * [Command-Lets](#Command-Lets)
  * [Functions](#Functions)
  * [Alias](#Alias)
  * [Redirecionadores](#Redirecionadores)
  * [Saídas](#Saídas)
  * [Where-Object](#Where-Object)
  * [Módulos](#Módulos)
* [Scripts no PowerShell](#Scripts-no-PowerShell)
  * [Variáveis](#Variáveis)
  * [Arrays](#Arrays)
  * [Operadores de Comparação](#Operadores-de-Comparação)
  * [Operadores Aritméticos e Lógicos](#Operadores-Aritméticos-e-Lógicos)
  * [Operadores de Atribuição](#Operadores-de-Atribuição)
  * [Select-String](#Select-String)
  * [Expressões Regulares - Regex](#Expressões-Regulares---Regex)
  * [If.. Else](#If..-Else)
  * [Loops](#Loops)
  * [Criando Funções](#Criando-Funções)
  * [Workflows](#Workflows)
  * [Jobs](#Jobs)
  * [Scheduled Jobs](#Scheduled-Jobs)
  * [New-Object (WScript.Shell)](#New-Object-(WScript.Shell))


## Introdução

* O PowerShell é uma linguagem de script e ambiente de shell para automação e gerenciamento de sistemas operacionais Windows. Com uma ampla gama de cmdlets, permite a manipulação eficaz de dados e é essencial para administradores de sistemas e profissionais de TI, sendo utilizado para automação, configuração de servidores, criação de scripts personalizados e diversas outras tarefas relacionadas à administração de sistemas Windows.

* Ele oferece duas interfaces distintas para os usuários: o PowerShell CLI (Command-Line Interface) e o PowerShell ISE (Integrated Scripting Environment).

## PowerShell CLI
* Interface de linha de comando para a execução direta de comandos e scripts.
* Adequado para tarefas rápidas e simples.
* Não possui recursos avançados de edição ou depuração interativa.
* É eficiente para usuários familiarizados com ambientes de linha de comando.


## PowerShell ISE
* Ambiente integrado de desenvolvimento para criação e edição de scripts.
* Oferece recursos avançados, como destaque de sintaxe, depuração interativa e autocompletar.
* Facilita o desenvolvimento e a manutenção de scripts mais complexos.
* Permite dividir a tela para facilitar a visualização e edição simultânea de scripts.
* Mais adequado para usuários que necessitam de uma experiência de desenvolvimento mais robusta e amigável.


## Command-Lets

* São pequenos blocos de construção de comandos no PowerShell. Eles são cmdlets nativos, scripts ou funções escritos em PowerShell. Cada cmdlet é projetado para realizar uma tarefa específica e pode ser encadeado ou combinado com outros cmdlets para realizar operações mais complexas. Cmdlets têm nomes verbais que descrevem a ação que realizam (por exemplo, Get-Process, Stop-Service, New-Item). Eles são fundamentais para a funcionalidade e flexibilidade do PowerShell, permitindo automação e administração eficientes do sistema operacional e outros produtos Microsoft.

## Functions

* As funções são blocos de código reutilizáveis que podem ser definidos para realizar tarefas específicas. Elas ajudam a modularizar o código, promovendo a reutilização e a organização. Ao criar uma função, você encapsula um conjunto de comandos em um único bloco nomeado, permitindo que esses comandos sejam chamados e executados sempre que necessário. Aqui estão alguns conceitos-chave sobre funções no PowerShell:

## Alias

* Alias é um apelido ou atalho para um cmdlet, função, script ou comando. Os aliases são usados para fornecer formas mais curtas e convenientes de chamar comandos frequentemente utilizados, facilitando a digitação e a execução rápida de tarefas.

## Redirecionadores

* Redirecionadores são operadores que controlam o fluxo de entrada e saída de dados durante a execução de comandos. Eles permitem que você direcione a saída de um comando para um arquivo, um dispositivo ou até mesmo para outro comando:
  
*   | Operador | Descrição |
    | --- | --- |
    | `pipeline` | Passa a saída para o comando subsequente para processamento. |
    | `>` | Redireciona a saída para o arquivo especificado. Se o arquivo já existe, o conteúdo atual será substituído. |
    | `>>` | Redireciona a saída para o arquivo especificado. Se o arquivo já existe, o novo conteúdo será anexado ao conteúdo atual. |
    | `2>` | Redireciona a saída de erro para o arquivo especificado. Se o arquivo já existe, o conteúdo atual será substituído. |
    | `2>>` | Redireciona a saída de erro para o arquivo especificado. Se o arquivo já existe, o novo conteúdo será anexado ao conteúdo atual. |
    | `2>&1` | Redireciona a saída de erro para a saída padrão. |

##  Saídas

*   | Operador | Descrição |
    | --- | --- |
    | `Out-Default` | Envie a saída para o formatador padrão e o cmdlet de saída padrão.  |
    | `Out-File` | Envie a saída para um arquivo. |
    | `Out-GridView` | Envie a saída para uma tabela interativa em uma janela separada. |
    | `Out-Host` | Envie a saída para a linha de comando. |
    | `Out-Null` | Apaga saída, em vez de enviá-lo para o console. |
    | `Out-Printer` | Envie a saída para uma impressora |
    | `Out-String` | Envie a saída para uma série de strings. |

## Where-Object

* Filtra objetos de uma coleção com base em uma condição.
  * A estrutura para o cmdlet Where-Object é:
  * `{_.Campo Operador Valor}` 
*   | Operador | Descrição |
    | --- | --- |
    | `-lt` | Menor que.  |
    | `-le` | Menor ou Igual. |
    | `-gt` | Maior que. |
    | `-ge` | Maior ou Igual. |
    | `-eq` | Igual. |
    | `-ne` | Não Igual. |
    | `-like` | Usa wildcards para comparar padrões. |


## Módulos

* Módulos são pacotes de funcionalidades reutilizáveis que podem ser carregados dinamicamente para adicionar cmdlets, funções, variáveis, e outros recursos ao ambiente de execução do PowerShell. Eles ajudam na modularização e na organização do código, permitindo a distribuição e o compartilhamento de funcionalidades específicas. Os módulos facilitam a extensão das capacidades do PowerShell e promovem a reusabilidade do código.

# Scripts no PowerShell

## Variáveis

* As variáveis são utilizadas para armazenar e manipular dados durante a execução de scripts ou comandos. Elas são contêineres nomeados que mantêm valores ou referências a objetos. As variáveis são fundamentais para armazenar informações temporárias, resultados de cálculos, strings, arrays e outros tipos de dados.
* Exemplo: `$nomeDaVariavel = "Valor"`

## Arrays

* Arrays são estruturas de dados que permitem armazenar e organizar coleções de valores. Um array é uma sequência ordenada de elementos, e cada elemento pode ser acessado individualmente por meio de um índice.
* Exemplo: `$meuArray = @(1, 2, 3, 4, 5) ou $outroArray = 1, 2, 3, 4, 5`

## HashTables

* São estruturas de dados que permitem associar pares de chave-valor. Elas são usadas para armazenar informações de maneira eficiente e proporcionam um método rápido de pesquisa e recuperação de dados com base em uma chave única.
* Exemplo: `$minhaHashtable = @{
    Nome = "João"
    Idade = 25
    Cidade = "Exemplo"}`

## Operadores de Comparação

*   | Operador | Descrição | Exemplo | Significado e Saída | 
    | --- | --- | --- | --- |
    | `-lt` | Menor que.  | $a -lt $b | A é menor que B? Booleano |
    | `-le` | Menor ou Igual. | $a le $b | A for menor ou igual a B? Booleano |
    | `-gt` | Maior que. | $a -gt $b | A é maior que B? Booleano |
    | `-ge` | Maior ou Igual. | $a -ge $b | A é maior ou igual a B? Booleano |
    | `-eq` | Igual. | $a -eq $b | A é igual a B? Booleano |
    | `-ne` | Não Igual. | $a -ne $b | A não é igual a B? Booleano |
    | `-like` | Como. | $a -like $b | A inclui um valor como B? Booleano|
    | `-notlike` | Não Como.  | $a -notlike $b | A não inclui um valor como B? Booleano |
    | `-contains` | Contém. | $a -cotains $b | A está contido em B? Booleano |
    | `-notcontains` | Não Contém. | $a -notcontains $b | A não está contido em B? Booleano |
    | `-match` | Coincide. | $a -match $b | A conincide com B? Booleano |
    | `-notmatch` | Não Coincide. | $a -notmatch $b | A não coincide com B? Booleano |
    | `-replace` | Substitui. | $a -replace ,$b,c$ | Se A possui strings de B substitua por C |

## Operadores Aritméticos e Lógicos

*   | Operador | Descrição | Exemplo | Significado e Saída | 
    | --- | --- | --- | --- |
    | `+` | Adição. | 2 + 2 | Retorna a soma. |
    | `/` | Divisão. | 4 / 2 | Retorna o quociente. |
    | `%` | Módulo. | 5 % 2 | Retorna o resto da divisão. |
    | `*` | Multiplicação. | 7 * 8 | Retorna o produto. |
    | `-` | Subtração. | 7 - 5 | Retorna a subtração. |
    | `-` | Negação. | -7 | Transforma o valor em negativo. |



  *   | Operador | Descrição | Exemplo | Significado e Saída | 
      | --- | --- | --- | --- |
      | `and` | Operador lógico AND. | $a -and $b | Verdade (1) se ambas as variáveis de entrada forem verdade. |
      | `or` | Operador lógico OR. | $a -or $b | Verdade (1) se e somente se pelo menos uma das variáveis de entrada for verdade. |
      | `not` | Operador lógico NOT. | $a -not $b | Negação (Inverso) da variável atua. |
      | `xor` | Operador lógico XOR. | $a -xor $b | Verdade (1) quando as variáveis assumirem valores diferentes entre si. |

## Operadores de Atribuição

*   | Operador | Descrição | Exemplo | Significado e Saída | 
    | --- | --- | --- | --- |
    | `=` | Atribui/Define/Compara valor  | $a = 2 | $a = 2|
    | `+=` | Adiciona um valor | $a += $b | $a = $a + $b |
    | `-=` | Subtrai um determinado valor | $a -= $b | $a = $a - $b |
    | `*=` | Multiplica | $a *= $b | $a = $a * $b |
    | `/=` | Divide o valor | $a /= $b | $a = $a / $b|
    | `%=` | Resultado da operação Modulo | $a %= $b | $a = $a % $b|
    | `++` | Incrementa em mais 1 | $a++ | $a = $a + 1 |
    | `--` | Decresce em menos 1 | $a-- | $a = $a - 1 |

## Select-String

* É usado para pesquisar cadeias de caracteres (strings) em arquivos de texto ou dados de entrada. Ele permite que você procure padrões de texto em arquivos ou em uma saída de comando, podendo também fornecer informações sobre as correspondências encontradas.
* Exemplo: `Select-String -Path <caminho_do_arquivo> -Pattern <padrão>`

## Expressões Regulares - Regex

* São padrões de texto utilizados para realizar correspondências complexas e manipulações de strings. No PowerShell, as expressões regulares são amplamente utilizadas para realizar buscas, extração de informações e substituição de texto em strings.
  * \d - numérico [0-9]
  * \w - alpha numérico [a-zA-Z0-9_]
  * \s - caractere de espaço em branco
  * . - Qualquer caractere exceto nova linha
  * () - Sub-expression
  * \ - Próximo caractere

## If.. Else.

* São estruturas de controle de fluxo que permitem a execução condicional de comandos ou blocos de código. A estrutura básica do if e else no PowerShell é semelhante a muitas outras linguagens de programação.
* Exemplo: `if (condição) {
     Bloco de código a ser executado se a condição for verdadeira
} else {
     Bloco de código a ser executado se a condição não for verdadeira
}`

## Loops

* São estruturas de controle de fluxo que permitem executar um bloco de código repetidamente enquanto uma condição específica for verdadeira.
* Exemplos:
  * For
  * ForEach
  * While 

## Criando Funções

* Criar funções é uma maneira eficaz de modularizar o código, facilitando a reutilização e a organização de tarefas específicas.
* Exemplo: `function Nome-Da-Funcao {
     Bloco de código da função
     Pode incluir parâmetros, lógica de execução, etc.
}
`

## Workflows

* É uma construção que permite a execução de script ou comandos em um ambiente distribuído e paralelo. Workflow é utilizado para automação de tarefas que precisam ser executadas em várias máquinas ou em paralelo em uma única máquina. Ele é particularmente útil para processos longos ou tarefas que podem ser divididas e executadas simultaneamente.

* Características principais:
  * Parallel Execution (Execução Paralela): As atividades dentro de um workflow podem ser executadas em paralelo, aproveitando o poder do processamento paralelo.
  * Persistência e Retomada: Os workflows podem ser interrompidos e retomados a partir do ponto em que foram interrompidos, mesmo após uma reinicialização do sistema ou falha.
  * Stateful Operations (Operações com Estado): Os workflows podem manter o estado durante a execução, permitindo que as variáveis e valores persistam entre diferentes execuções.
  * Remoting Automático: Os workflows podem ser executados automaticamente remotamente em máquinas diferentes.
  * Suporte a Transações: Os workflows suportam transações, o que significa que você pode executar operações atômicas dentro deles.
  * Sintaxe Específica: A definição de workflows usa uma sintaxe específica, como workflow e foreach -parallel, para indicar as partes que podem ser executadas simultaneamente.

## Jobs

* Permitem a execução de comandos em Background no computador local ou remoto.

* Exemplos:
  * `Start-Job` - Inicia um trabalho.
  * `Get-Job` - Exibe os trabalhos associados a sessão atual.
  * `Wait-Job` - Aguarda pelo trabalho até que esteja pronto.
  * `Receive-Job` - Exibe o resultado de um trabalho em background.
  * `Stop-Job` - Para um trabalho.
  * `Remove-Job` - Remove um trabalho.

## Scheduled Jobs

* Trabalhos agendados são extremamente úteis quando você tem tarefas que são executadas com maior frequência ou com recorrência e principalmente quando sao atividade de longa duração
  * `Get-Command -Module PSScheduledJob | Sort-Object Noun`
 
## New-Object (WScript.Shell)

* A expressão New-Object (WScript.Shell) no PowerShell é utilizada para criar uma nova instância do objeto WScript.Shell. Esse objeto pertence à biblioteca de automação Windows Script Host (WSH), que é um conjunto de tecnologias de automação da Microsoft para scripts em sistemas Windows. O objeto WScript.Shell fornece métodos para interagir com o ambiente do sistema operacional, como executar programas, acessar o registro do Windows e manipular atalhos.
  * Exemplo: `$wshell.Popup("teste")`
  




















## Get-Content

  * `Get-Content` Obtém o conteúdo de um arquivo.

## ForEach-Object

  * `ForEach-Object` Executa um bloco de script para cada objeto de entrada.

## Out-File

  * `Out-File` É utilizado para redirecionar a saída de um comando ou script para um arquivo específico.

## Test-NetConnection

  * `Test-NetConnection` É utilizado para testar a conectividade de rede para um host específico.

## ConvertTo-Json

  * `ConvertTo-Json` Converte objetos em formato JSON.

## Get-Date

  * `Get-Date` Retorna a data e hora atuais.

## Start-Sleep

  * `Start-Sleep` Pausa a execução de um script ou comando pelo tempo especificado.

## Write-Host

  * `Write-Host` Exibe texto ou variáveis no console.

## Get-Command

  * `Get-Command` Lista todos os comandos disponíveis no ambiente.

## Get-Help

  * `Get-Help` Fornece informações de ajuda sobre outros comandos.


## Test-Path

  * `Test-Path` Verifica se um caminho (arquivo ou diretório) existe.


## Get-ExecutionPolicy

  * `Get-ExecutionPolicy` Retorna a política de execução atual do sistema.


## Get-Credential

  * `Get-Credential` Solicita ao usuário credenciais (nome de usuário e senha) para uso em operações subsequentes.


## Invoke-Command

  * `Invoke-Command` Executa comandos em computadores remotos.


## Enter-PSSession

  * `Enter-PSSession`  Inicia uma sessão interativa remota com um computador.

## Get-Member

  * `Get-Member`  Exibe as propriedades e métodos disponíveis para um objeto.

## Get-Process

  * `Get-Process`  Lista os processos em execução no sistema.

## Get-WindowsDriver

  * `Get-WindowsDriver`  Exibe informações sobre os drivers instalados no sistema operacional Windows.

## Export-WindowsDriver

  * `Export-WindowsDriver`  Exporta os drivers do Windows para um diretório específico.

## Start-MpScan

  * `Start-MpScan` É usado para iniciar uma verificação de antivírus no Windows Defender (Microsoft Defender Antivirus). Ele aciona uma verificação manual no sistema em busca de malware e ameaças de segurança.


