# fila_sus_sc
EDA on public health data from Brazil.

# Verificando se houve alguma melhora após o Hacking Health

Após a apresentação da Larissa Lautert, no Pyladies (https://www.sympla.com.br/6-pyladies-floripa---digitro__319770) que relatou como a lista de espera do SUS de SC poderia diminuir consideravelmente cas fossem eliminados registros duplicado. Fiquei curioso se foi feito alguma coisa quase 8 meses após a apresentação destes dados.

Dados da apresentação da Larissa: https://github.com/llautert/hacking-health-sc-2017

Ao baixar os dados do site https://listadeespera.saude.sc.gov.br/consulta/completa.html, verifiquei o seguinte:

* Não achei API para facilitar o trabalho (que novidade...)
* A maneira mais rápida foi baixar separando por central de regulação, demorou cerca de 3 horas e baixou quase 750 mil solicitações de procedimento na lista de espera. Mas não havia uma coluna identificando a cidade de origem.
* Modifiquei o crawler para baixar e identificar cada município já que não havia este registro. Demorou cerca de 12h e retornou apenas pouco mais de 300 mil solicitações. Concluí que (a não ser que eu tenha feito alguma barbeiragem) mais da metade das solicitações não tinham a denominação da cidade.
* Portanto os dados desta análise não puderam ser separado por município (até eu descobrir uma maneira de fazer isso).
