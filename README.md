# FiveM Client Dumper
**THIS PROJECT IS NOW UNMAINTAINED. THIS MEANS I WILL NOT UPDATE THE CODE, ANSWER TO ISSUE REPORTS OR OFFER ANY KIND OF SUPPORT.
HOWEVER, YOU STILL CAN FORK IT AND MODIFY THE CODE THE WAY YOU WANT. 
[LICENSE](https://github.com/marcodsl/FiveM-Client-Dumper/blob/master/LICENSE) STILL APPLIES.**

FiveM Client Dumper é uma aplicação que permite que o usuário obtenha os arquivos do lado do client de um servidor de FiveM.

## Como funciona?

Como descrito [aqui](https://docs.fivem.net/docs/scripting-manual/nui-development/full-screen-nui/#developer-tools), o
aplicativo do FiveM expõe as ferramentas de debugging do Chrome Embedded Framework em [127.0.0.1:13172](http://127.0.0.1:13172).
Dessa forma, o FiveM Client Dumper utiliza do [Chrome Devtools Protocol](https://chromedevtools.github.io/devtools-protocol/)
para executar chamadas [`fetch()`](https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API) que enviam os arquivos do client 
para um servidor HTTP local. Em seguida, os arquivos recebidos são salvos no disco.

## Como usar

1. Certifique-se de que a última versão do [JRE 64 bits](https://www.oracle.com/java/technologies/javase-jre8-downloads.html) está instalada.
2. Baixe o arquivo na página [RELEASES](https://github.com/marcodsl/FiveM-Client-Dumper/releases/tag/1.0-SNAPSHOT).
3. Abra o FiveM e entre no servidor cujo client-side deseja obter.
3. Execute ```java -jar fivem-client-dumper-1.0-SNAPSHAT-all.jar -a [Endereço IP]``` no sua CLI preferida.
5. Aguarde o fim da execução do programa.

#### Opções
* `-a`: endereço IP do servidor
* `-p`: porta do servidor (padrão: 30120)
* `-o`: pasta de saída dos arquivos (padrão: IP do servidor)

## Perguntas Frequentes

* **P:** Eu posso ser banido do FiveM por usar o FiveM Client Dumper? **R**: _Não. O FiveM Client Dumper não acessa
a memória do processo do FiveM diretamente, portanto não existem riscos de banimento._

## Licença

O código-fonte do FiveM Client Dumper está licenciado sobre a [GNU Affero General Public License v3.0](https://github.com/marcodsl/FiveM-Client-Dumper/blob/master/LICENSE)