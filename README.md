# PowerShell
<a name="under-construction" href="https://github.com/mateusdn"><img src="uc.png" /></a>



## PowerShell - Tópicos
* [Introdução](#Introdução)
* [PowerShell CLI](#PowerShell-CLI)
* [PowerShell ISE](#PowerShell-ISE)
* [Command-Lets](#Command-Lets)
* [Functions](#Functions)
* [Alias](#Alias)
* [Introdução](#Introdução)







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


