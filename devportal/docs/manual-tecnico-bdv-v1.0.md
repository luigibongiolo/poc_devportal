![Descrição: CNseg_simpleshorizontal.JPG]<br>**Manual Técnico – BDV v2**

**BDV - Base de Dados de Veículos**

Manual Técnico do Produto

Versão **1.0**

Julho/2019


![Descrição: CNseg_simpleshorizontal.JPG]

1. # **Informações gerais sobre o produto**
   1. ## **Nome**
      Base de Dados de Veículos
   1. ## **Endereço do arquivo WSDL**
      ` `<http://bdv.cnseg.org.br/consultabvs/service.asmx?wsdl> 
   1. ## **Métodos**
      A tabela a seguir apresenta as consultas disponíveis para consumo e o nome da operação na interface do serviço.

      |Descrição da Consulta|Nome da Operação|
      | :-: | :-: |
      |Consulta por Chassi|ConsultaChassi|
      |Consulta por Placa|ConsultaPlaca|
      |Consulta por Motor|ConsultaMotor|
      |Consulta por Caixa de Câmbio|ConsultaCxCambio|
      |Consulta por Renavam|ConsultaRenavam|
      |Base de Agregados|ConsultaMotorRenavam|
	  
1. # **Informações detalhadas do serviço**
   1. ## **Acesso webservice**
      O protocolo de comunicação com o webservice é o SOAP 1.1. Esse protocolo aceita apenas requisições POST.
   1. ### **Parâmetros de entrada das consultas**
      1. ### **Consulta por Chassi (ConsultaChassi)**

         |Parâmetro|Tipo|Tamanho|Obrigatório|Observações|
         | :-: | :-: | :-: | :-: | :-: |
         |IdUsuario|Varchar|255|Sim|Informar Login do Usuário|
         |Senha|Varchar|255|Sim|Informar Senha do Usuário|
         |Chassi|Varchar|21|Sim|Informar Chassi para consulta|
		 
      1. ### **Consulta por Placa (ConsultaPlaca)**
	  
         |Parâmetro|Tipo|Tamanho|Obrigatório|Observações|
         | :-: | :-: | :-: | :-: | :-: |
         |IdUsuario|Varchar|255|Sim|Informar Login do Usuário|
         |Senha|Varchar|255|Sim|Informar Senha do Usuário|
         |Placa|Varchar|7|Sim|Informar Placa para consulta|
		 
      1. ### **Consulta por Motor (ConsultaMotor)**

         |Parâmetro|Tipo|Tamanho|Obrigatório|Observações|
         | :-: | :-: | :-: | :-: | :-: |
         |IdUsuario|Varchar|255|Sim|Informar Login do Usuário|
         |Senha|Varchar|255|Sim|Informar Senha do Usuário|
         |Motor|Varchar|21|Sim|Informar Motor para consulta|
		 
      1. ### **Consulta por CxCambio (ConsultaCxCambio)**

         |Parâmetro|Tipo|Tamanho|Obrigatório|Observações|
         | :-: | :-: | :-: | :-: | :-: |
         |IdUsuario|Varchar|255|Sim|Informar Login do Usuário|
         |Senha|Varchar|255|Sim|Informar Senha do Usuário|
         |CxCambio|Varchar|21|Sim|Informar Caixa de Câmbio para consulta|
		 
      1. ### **Consulta por Renavam (ConsultaRenavam)**

         |Parâmetro|Tipo|Tamanho|Obrigatório|Observações|
         | :-: | :-: | :-: | :-: | :-: |
         |IdUsuario|Varchar|255|Sim|Informar Login do Usuário|
         |Senha|Varchar|255|Sim|Informar Senha do Usuário|
         |Renavam|Varchar|21|Sim|Informar Renavam para consulta|
		 
      1. ### **Base de Agregados (ConsultaMotorRenavam)**

         |Parâmetro|Tipo|Tamanho|Obrigatório|Observações|
         | :-: | :-: | :-: | :-: | :-: |
         |IdUsuario|Varchar|255|Sim|Informar Login do Usuário|
         |Senha|Varchar|255|Sim|Informar Senha do Usuário|
         |Placa|Char|7|Não\*|Informar Placa para consulta|
         |Chassi|Char|21|Não\*|Informar Chassi para consulta|

         \*Campos não são obrigatórios, mas ao menos um deles deve ser preenchido.
		 
		 1. ## **Informações sobre o retorno das consultas**
		 Esta seção apresenta estruturas e exemplos dos retornos de cada consulta.
		 
		 1. ### **Retornos Gerais:**

         |Retorno|Descrição|
         | :-: | :-: |
         |Usuário ou Senha Inválido|Indica que o usuário e/ou a senha informada são inválidos|
         |Parâmetro inválido|Indica que um ou mais campos estão nulos ou inválidos. O parâmetro “Placa” deve conter 7 caracteres no formato “AAA9999”. O parâmetro “Chassi” deve conter, no máximo, 21 caracteres|
         |Não há retorno para esta consulta|Indica que não foi encontrado nenhum registro para os campos informados|
         |Sua consulta não foi realizada, entre em contato com o suporte|Indica que ocorreu um erro inesperado e é preciso entrar em contato com o suporte|
         |Cliente não possui permissão para o método|Indica que o usuário não tem permissão para realizar a consulta ao método|
         |Acesso não permitido para o IP|Indica que a consulta foi realizada a partir de um IP não cadastrado para a empresa do usuário|
         |Cliente não possui crédito disponível|Indica que a consulta não pode ser realizada, pois não há crédito suficiente|
         |Cliente já utilizou todas as consultas do Contrato de Experiência de Uso para esse método|Indica que o contrato da empresa é de Experiência de Uso e a quantidade máxima de consultas permitidas já foi atingida.|
         |Contrato inativo ou fora do período de vigência|Indica que a empresa não possui nenhum contrato ativo e/ou vigente para o produto.|
         |Método inválido|Indica que esta consulta não está disponível.|
         |Produto inválido|Indica que esta consulta não está disponível.|
         |Produto em desenvolvimento|Indica que esta consulta não está disponível.|
         |Produto indisponível, tente novamente mais tarde|Indica que o produto está indisponível e nenhuma consulta poderá ser realizada.|
         
1. ### **Parâmetros de retorno: caso de sucesso**
   Informações detalhadas sobre os parâmetros de retorno para consultas ao BDV realizadas com sucesso.
   1. #### **Estrutura dos Dados**

      |Nome do Campo|Tipo|Tamanho|Descrição do Campo|
      | :-: | :-: | :-: | :-: |
      |CodRetorno|Char|3|<p>000-Sem informação</p><p>019-Veículo Cadastrado e com sinalização de </p><p>alarme</p><p>048-Veículo cadastrado e com ocorrência de </p><p>roubo/furto</p>|
      |Mensagem|Char|50|Mensagem do Código de Retorno|
      |DataEmplacamento|Char|8|Data de Emplacamento DD/MM/AAAA|
      |Chassi|Char|21||
      |Placa|Char|7||
      |TipoDocFaturado|Char|1|<p>1-Pessoa Física</p><p>2-Pessoa Jurídica</p><p>3-Outros</p>|
      |IdentFaturado|Char|14||
      |UfFaturado|Char|2||
      |TipoDocProprietario|Char|1|<p>0 – Sem informações</p><p>1 - CPF Proprietário</p><p>2 - CNPJ</p><p>3 - CPF Cônjuge</p><p>4 - CPF do responsável </p><p>5 - Não obrigatório</p>|
      |UfJurisdicao|Char|2||
      |CodMunicipio|Char|4||
      |NomeMunicipio|Char|50||
      |AnoFabricacao|Char|4||
      |AnoModelo|Char|4||
      |CodMarcaModelo|Char|6||
      |NomeMarcaModelo|Char|50||
      |CodTipoVeiculo|Char|2||
      |NomeTipoVeiculo|Char|50||
      |CodEspecieVeiculo|Char|2|<p>1-Passageiro</p><p>2-Carga</p><p>3-Misto</p><p>4-Corrida</p><p>5-Tração</p><p>6-Especial</p><p>7-Coleção</p>|
      |NomeEspecieVeiculo|Char|50||
      |CodTipoCarroceria|Char|3||
      |NomeTipocarroceria|Char|50||
      |NumCarroceria|Char|21||
      |CodCor|Char|2||
      |NomeCor|Char|50||
      |CodCombustivel|Char|2||
      |NomeCombustivel|Char|50||
      |Potencia|Char|3||
      |NumCilindradas|Char|4||
      |NumLugares|Char|3||
      |CapacidadeCarga|Char|5||
      |PBTVeiculo|Char|5|Peso Bruto Total do Veículo|
      |CMTVeiculo|Char|5|Capacidade Máxima de Tração do Veículo|
      |Procedencia|Char|1|<p>1 – Nacional</p><p>2 – Estrangeiro</p>|
      |CodSituacaoChassi|Char|1|<p>N – Normal</p><p>R – Remarcado</p>|
      |NumCxCambio|Char|21||
      |NumEixos|Char|2||
      |NumEixoTras|Char|21||
      |NumTerceiroEixo|Char|21||
      |NumMotor|Char|21||
      |TipoMontagem|Char|1|<p>1 – Completa</p><p>2 – Incompleta</p>|
      |TipoDocImportador|Char|1|<p>0 – Sem informação</p><p>1 – CPF</p><p>2 – CNPJ</p>|
      |NumIdentImportador|Char|14||
      |NumDI|Char|10|Número da Declaração de Importação|
      |DataRegistroDI|Char|8||
      |CodSRF|Char|7|Código da Secretaria da Receita Federal|
      |DataUltimaAtualizacao|Char|8||
      |CodRestricao1|Char|2|<p>00 – Sem Restrição</p><p>01 – Arrendamento </p><p>02 – Reserva de Domínio </p><p>03 – Alienação Fiduciária</p><p>04 – Restrição Judicial </p><p>05 – Restrição Administrativa</p><p>06 – Restrição pata Roubo/Furto </p><p>07 – Restrição Ben. Tributário </p><p>08 – Baixa Alienação p/ord Jud </p><p>09 – Penhor de Veículo</p>|
      |NomeRestricao1|Char|50||
      |CodRestricao2|Char|2|<p>00 – Sem Restrição</p><p>01 – Arrendamento </p><p>02 – Reserva de Domínio </p><p>03 – Alienação Fiduciária</p><p>04 – Restrição Judicial </p><p>05 – Restrição Administrativa</p><p>06 – Restrição pata Roubo/Furto </p><p>07 – Restrição Ben. Tributário </p><p>08 – Baixa Alienação p/ord Jud </p><p>09 – Penhor de Veículo</p>|
      |NomeRestricao2|Char|50||
      |CodRestricao3|Char|2|<p>00 – Sem Restrição</p><p>01 – Arrendamento </p><p>02 – Reserva de Domínio </p><p>03 – Alienação Fiduciária</p><p>04 – Restrição Judicial </p><p>05 – Restrição Administrativa</p><p>06 – Restrição pata Roubo/Furto </p><p>07 – Restrição Ben. Tributário </p><p>08 – Baixa Alienação p/ord Jud </p><p>09 – Penhor de Veículo</p>|
      |NomeRestricao3|Char|50||
      |CodRestricao4|Char|2|<p>00 – Sem Restrição</p><p>01 – Arrendamento </p><p>02 – Reserva de Domínio </p><p>03 – Alienação Fiduciária</p><p>04 – Restrição Judicial </p><p>05 – Restrição Administrativa</p><p>06 – Restrição pata Roubo/Furto </p><p>07 – Restrição Ben. Tributário </p><p>08 – Baixa Alienação p/ord Jud </p><p>09 – Penhor de Veículo</p>|
      |NomeRestricao4|Char|50||
      |DataLimiteRestTrib|Char|8||
      |CodSituacaoVeículo|Char|1|<p>S – Em circulação </p><p>N – Baixado</p>|
      |Renavam|Char|21||
      |**Identificação da Consulta**||||
      |Protocolo|Char|20|Número de protocolo da consulta|
      |Saldo|Decimal|13,2|Saldo só deve ser considerado para contratos Pré-pago|
	  
1. ### <a name="_toc14263450"></a>**Exemplos de retorno: caso de sucesso**
   Exemplos de XML de retorno para consultas realizadas com sucesso.
   1. #### <a name="_toc14263451"></a>**Exemplo A**

      O exemplo de retorno A se aplica aos métodos:

- Consulta por Chassi (ConsultaChassi)
- Consulta por Placa (ConsultaPlaca)
- Consulta por Motor (ConsultaMotor)
- Consulta por Caixa de Câmbio (ConsultaCxCambio)
- Consulta por Renavam (ConsultaRenavam)

<Consulta>

`	`<BVS>

`		`<CodRetorno>000 </CodRetorno>

`		`<Mensagem>Sem informacao </Mensagem>

`		`<DataEmplacamento>20080222 </DataEmplacamento>

`		`<Chassi>XXXXXXXXXXXXXXXXXXXXX </Chassi>

`		`<Placa>XXX0000 </Placa>

`		`<TipoDocFaturado>2 </TipoDocFaturado>

`		`<IdentFaturado>11111111111111 </IdentFaturado>

`		`<UfFaturado>RJ </UfFaturado>

`		`<TipoDocProprietario>1 </TipoDocProprietario>

`		`<UfJurisdicao>RJ </UfJurisdicao>

`		`<CodMunicipio>6001 </CodMunicipio>

`		`<NomeMunicipio>RIO DE JANEIRO </NomeMunicipio>

`		`<AnoFabricacao>2008 </AnoFabricacao>

`		`<AnoModelo>2008 </AnoModelo>

`		`<CodMarcaModelo>149542 </CodMarcaModelo>

`		`<NomeMarcaModelo>GM/CLASSIC SPIRIT </NomeMarcaModelo>

`		`<CodTipoVeiculo>06 </CodTipoVeiculo>

`		`<NomeTipoVeiculo>Automovel </NomeTipoVeiculo>

`		`<CodEspecieVeiculo>01 </CodEspecieVeiculo>

`		`<NomeEspecieVeiculo>PASSAGEIRO </NomeEspecieVeiculo>

`		`<CodTipoCarroceria>999 </CodTipoCarroceria>

`		`<NomeTipoCarroceria>N\_O APLICAVEL </NomeTipoCarroceria>

`		`<NumCarroceria />

`		`<CodCor>11 </CodCor>

`		`<NomeCor>PRETA </NomeCor>

`		`<CodCombustivel>16 </CodCombustivel>

`		`<NomeCombustivel>ALCOOL/GASOLINA </NomeCombustivel>

`		`<Potencia>072 </Potencia>

`		`<NumCilindradas>1000 </NumCilindradas>

`		`<NumLugares>005 </NumLugares>

`		`<CapacidadeCarga>00000 </CapacidadeCarga>

`		`<PBTVeiculo>00000 </PBTVeiculo>

`		`<CMTVeiculo>00200 </CMTVeiculo>

`		`<Procedencia>1 </Procedencia>

`		`<CodSituacaoChassi>N </CodSituacaoChassi>

`		`<NumCxCambio>X111111111 </NumCxCambio>

`		`<NumEixos>00 </NumEixos>

`		`<NumEixoTras />

`		`<NumTerceiroEixo />

`		`<NumMotor>X11111111 </NumMotor>

`		`<TipoMontagem>1 </TipoMontagem>

`		`<TipoDocImportador />

`		`<NumIdentImportador />

`		`<NumDI>0000000000 </NumDI>

`		`<DataRegistroDI>00000000 </DataRegistroDI>

`		`<CodSRF>0000000 </CodSRF>

`		`<DataUltimaAtualizacao>20110124 </DataUltimaAtualizacao>

`		`<CodRestricao1>00 </CodRestricao1>

`		`<NomeRestricao1>SEM RESTRICAO </NomeRestricao1>

`		`<CodRestricao2>00 </CodRestricao2>

`		`<NomeRestricao2>SEM RESTRICAO </NomeRestricao2>

`		`<CodRestricao3>00 </CodRestricao3>

`		`<NomeRestricao3>SEM RESTRICAO </NomeRestricao3>

`		`<CodRestricao4>00 </CodRestricao4>

`		`<NomeRestricao4>SEM RESTRICAO </NomeRestricao4>

`		`<DataLimiteRestTrib>00000000 </DataLimiteRestTrib>

`		`<CodSituacaoVeiculo>S </CodSituacaoVeiculo>

`		`<Renavam>11111111111 </Renavam>

`		`<saldo>0 </saldo>

`		`<protocolo>20141021155306000097 </protocolo>

`	`</BVS>

</Consulta>
1. #### <a name="_toc14263452"></a>**Exemplo B**
   O exemplo de retorno B se aplica ao método:

- Base de Agregados (ConsultaMotorRenavam)

<Consulta>

`	`<BVS>

`		`<CodRetorno>000 </CodRetorno>

`		`<Mensagem>Sem informacao </Mensagem>

`		`<Placa>XXX9999 </Placa>

`		`<Chassi>XXXXXXXXXXXXXXXXXXXXX </Chassi>

`		`<NumMotor>X11111111 </NumMotor>

`		`<NumCxCambio>X111111111 </NumCxCambio>

`		`<Renavam>11111111111 </Renavam>

`		`<UfJurisdicao>RJ </UfJurisdicao>

`		`<saldo>99 </saldo>

`		`<protocolo>20141021162904000104 </protocolo>

`	`</BVS>

</Consulta>

1. ### **Informações de retorno: caso de erro**
   Informações detalhadas de retorno para consultas realizadas com erro.
   cd 
   1. #### **Parâmetros de retorno: caso de erro**

|Retorno|
| :-: |
|Usuário ou Senha Inválido|
|Parâmetro inválido|
|Não há retorno para esta consulta|
|Sua consulta não foi realizada, entre em contato com o suporte|
|Cliente não possui permissão para o método|
|Acesso não permitido para o IP|
|Cliente não possui crédito disponível|
|Cliente já utilizou todas as consultas do Contrato de Experiência de Uso para esse método|
|Contrato inativo ou fora do período de vigência|
|Método inválido|
|Produto inválido|
|Produto em desenvolvimento|
|Produto indisponível, tente novamente mais tarde|

1. #### <a name="_toc14263455"></a>**Exemplo de retorno: caso de erro**
   <?xml version="1.0" encoding="UTF-8"?>

   <consulta>

   `	`<BVS>

   `		`<retorno>Parametro invalido</retorno>

   `		`<saldo>0,00</saldo>

   `		`<protocolo>20140724155545000014</protocolo>

   `	`</BVS>

   </consulta>

[Descrição: CNseg_simpleshorizontal.JPG]: data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/2wBDAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/wAARCAA0AHQDASIAAhEBAxEB/8QAHQABAAEEAwEAAAAAAAAAAAAAAAkBBwgKBAUGAv/EAC8QAAEEAgIBBAEEAQMFAAAAAAMBAgQFBgcACBEJEhMhFBUWIjFRGCORMjNCUnH/xAAZAQACAwEAAAAAAAAAAAAAAAAABgUICQf/xAAkEQACAwEAAgMAAwEBAQAAAAACAwEEBQYAEgcREwgUFSIhFv/aAAwDAQACEQMRAD8A3+OfBSMCN5SPaMY2ue971RrWtaiuc5zlVERqIiqqqqIiIqr9c8pnGd4lrfG7HLc1vIOP0FWJSy7CeZBDaq/9sIm/ZDyDO8MBGC15jPVGDY5VTkX1/wB37Xs5kV519674qcdhlOL5QrM3yOe6rHEgV8LwQ8eDHCY0Z1iUwoMY0gyOCklTkEijViqHR9thc5YrZT7a7PR6irBYnOVi/TU1npS1oKUkIL8FNJRLi3a/GqBQXs3/AJKIb+d4ne6Kra1q9N1fnMtqB2+jsBK8rJS1yVGx1g5GHNWLgZ/UrftaMZH1VPtEzaLuB3RsM2u7TXWtrQ8LCqySSFa3UAzgmyaVHIrDsAcase2nYVitH7FT8z2/I7yJWIvF6z99MgwGyrcT2vaS8gwQxAw2ZBYEfKuMXG9UGySeU9Xmn1MdPashkhxTxQI54SKMaBSPmw0j2GgZJIxMuhtvSMhBJfHfFh4Ley4BXterFNHyQUR2LSYj1T3snAu3w3MVHofx58ZHYv6dvbnJaxLObi+HYd8g/kBVZPlzXW72uT3NZJFTV1pEhlVPpw3SzqxVVHf0vM8slv8AJrY+RLff5uF1QaQWPSxm3a1nMw5zEtkhwf62oypWdTWEkAgEnYFpFbhn9spdN6dbK/jpj8RV43R6Xl5pMRBV9ClbRp7P99qljOzLstdyyqyw4gylkBXJcRWkJrj+UbIsOXGnxI02GcUqJLAGTGkge0gZEc42lCYJGKrCCKN7XjexVa5rkc1VRecnkbXRncUTDsOF1p3HnOIRNu63yK3xOjpw5VAt1t8WE8MzHYlbZjUceXIpY8suODqnuFbx41PHSVBG5fuSRFRU8ovlOaQc7vU+iyqujWNItNSh0KIWUWH5Wh+QFby739djBVdouIkWFFMEJhM/X1MTNA+iwL3OaljPuKfC4Nh591laxWRq50sKKmpR/sLWTqN5UC+u4YkDA4+p+4mIrxxxyc8g/HHHHDw8ccccPDxxxxw8PHHHHDw81Xe9Xbi135tK3oqSfIDrTCrOZVY/Xo4gR2syEYkWXfzI7kariySje2GwzEeCKjfLWke9OcL07tnQsE7aa9faPYOHmcS5wRTO8I0U66AKTWOe5fCNYSVX/jp9p7inE1E8uROSCd/vTis9iWdxunQFbGfmsxxrDMcDGSPAHlclf9w9vRFO8MMGQSF8klxJBY8e0OrjIZk0jlkQ5dbdUbUzHs3rXX1XiGU02VYvn+M5Dlse4o7SlmYdUYzewrWxnXoLGNFPXI8URY0UcpgnTCHYkf5WKruZyavKfKfM/wAgMHe2KV7dsaXXVW0tqnVsNy7eW+x+Da6zH9gzhp5THAdJ7BKotRMg2qiLDNPcnp/hvrf44dDhYmjn88nL4y0rQwb9qurXpa9avD0WGgUpPUK9rqSa9CuqRuOaK5BLymuvc4RfKeU/pftOeO2GtumBZmtA57bxMWyBadwvsrbT9Jl/gKPx5X5Ek/F7Ppf5+Ppeehm2ddUwyTbOfDgQ44/fImTZIIkYLGp/IhjnIMQmJ9qrnvRqJ58r9c8Jjm5NR5panx/Edm4DlF5HR6mp6DLqC4shoPyhHOgwLCRJ9g1RUI5Bq1n/AJKnNDLtin6zQfeRVfeW1CAKwpVkyYBD91gIxYbAifYfziZiYifM06Fa97f6NfPfcrZ7U2LJjWa6osVsE4G2wAJa1s9fUv0IYkZmPNLG4vZzbOZLkS5P6mk+RIPJUxElJOSQ8hTuMrkKkj50cRSo75Pk8u8+775Mz6c3qWT8gzvGusW77c9td5AwsDWeay/fIsZs2HHIdMayIyI58krognrXXB/JnqH4LApSPbJWIfu+Kl192d3nieOq0kCFse8HVw4Q3HewlpKSe2qhxo7XkMaNKmvrwRwMeVzxoJjFeqNWTf03unlf1jpbTvT26cHBrNlGVuu8Xv2J+p4lR2TP53E+EiPMzKL8CjDAqhMdLiRSqJ6fKV/jO3+PmD2OH8lblqvoMzOX5m1q0+x0bTPTHuoznPSY2DaYV5ZBqKxXdJfrXH3f7QmGwem/8kt7g934qwKTstep1nVVMi9xGbVVDN2nb00VXBNUEgVmE+jhr20QEptF+aPSXSiQ2QeOQqX3rZaTr7qRCptb5fcVMYyjdaSbWnqjkH5RGmSuJ+U8LSNVHjYc7HuaqeUaqqiX5236nmq9SUuncgs8GzK2q9y63pdm0z4JKwUmrprg7xNiT45TOQs6Og3vc2OVwiqiMa9PPu5dZPzD8avoaGovq6U52UVIb146+guqr/RsFVpGD2VAXYTYeBLB1YnKiY+yMRmJmhrvg/5VRoZmSzjr3+prhePPzwtZjbjf8ysFu+tldV421XVq7AYaLQpdMFAgsjiRiTLjlpZO48Tfpsu76E6ZJh37LJnUA1aUavsqhlcti1sd719jDvGiicwioojNeMiI5jkS1/UvtbinbjCcnzfE8dusah4tmJ8Nlw7wsQ0g8sFFR3yywvhucNI7gXgQo1/h6ECRV/i5vh0/3sj/AFaeJF9Jamhmv2KVQfcys5lZtdLri2CMplINt1x+/wBIkv1GRiY+5hD/APndv/Hvb85zxyM3Ur4l+6f5gNXVtJsPRRaozF8ONVWwf1CpEfyKDIS+onKrjlPc3z49zfP+PKeeFVE8eVRPP9eVRPP/AM5L+QvleOURUX7RUVP8ovnj3N/9m/8AKcPDyvHKeU/yn/KccPDyvIkvVfwTacPV9DvrTF5k1Bk2qpUp2TnxKwm1tkXDbNB/lSzfp5RElxaqaEB5QitMwUYpDuYghlc2W3nEnwIVpClV1jFBOgTo5ok2FKEM8WXFkjcGRGkgK14jAOJ7xlERrmEY5zHtVqqirnXc3X63ndTn7FixTHQRAqu1GGqzTtJYD6ltJrIDg69lSmfQmPuIkHtEFMw0cX1FnjOnyekrVq94s2xJuoW1g2rfpuWde7SeDBMJCzVa1XsQFAEQs9ZkYidC3OuzG4tlBbHz3aeaZVFH9sh3GRT5UNqon9pDU6R/Pj+1+JVVfKr5VV89Ppc2yMt3FrjF9PzbSHsm5y2oi4xYUxDDl1MpJY3muHkD9sh1cVDTJyl8xnxhvBIRwzK10x3ef0V8yPfWmxenDayfAtZZJllp67tQUzqs8kvvMTDr2xe2Ctcx73E/RrQ4HxRIrIMo6sHFfnv6a3poVfUOmTYezT1uVb7yGC0c+dEakiowmCdvuLQY8UiK4xvv2WVsiMdLe1WBRkdGo6mnN/xy6l/dV7HU2bLaOVbr3W7p33WW311mwyuqhYYwrQtcSxgpOVnTH7OYg/zE71dT/J/ja3x5YRx9aqvR2KVignnRzk1U5zrKfysu0qy1DUJCYZMjC/0C6f0ATK/2leSGpPT965axzGTtWViH7421bWB8gts6ziU/I7FuRWRHS7Owq48tFr6t5ZhjPC6JFaQLFaxhURqcjr9aPLLkljpTWY5xq7Grktjb2T2PUYHyWzK6pDIMn0N6VkeVIksR/lBucj1RPpeT6cj39QjpnM7ba4rR4hY1tRszCjTJuKSbhzxVFoCcIbLHH7OSERzwwTljxyBmjAf8aQFjnheNz05Zb5X5C9s/G27z3I59QLTmULYZSYTRRpqq6tS/foEQwChPRrockyZ9Q42erS+jIvKpfDnbUMP5T5/pu00rp1Eq0aRbFiXaFjJdcx7mdm6IiZMaS8yw9LQBX/qAX7qGJWMeZJaW0VqfVWr8awbDcNxyLQx6OCKUv6VAOW6OaKx0uxtpJQPJZSrAryHkHlPKpHEVP+jw1ITvVRwOguu0HVjW0SMKixy4xeixQcSlACCCsrbDO7GAgq+LHYOPHFGGXyEAhsE1GIxGo3658YVnPrQ6uoIWqIuhXZOGkjCpKbLrSw11cDFBisSNDc7IG5qBJccImjQUiwhtm/C1PyQqVHotzOxXWnuDtXcHRjPLPX65PZYLhmvm7yyOvyDEIsKky6tyl1tkrWxZFzClzwsYV0gZKaBMjlaqsA5z2uY1U7Rlv5C42ph1uF6XN/r9Fw7b+Zs44Va/+dX6CizSq1/zaxdqtTpIcVg0iNca/pIl/wBeoufBpp/Gfc3N+38icnqza5fv1Z2thbpXbUadjnLoZdq1LFKZTt3b1hIVluMrJWYZEh/x7laLUuzsu6pxuyHRPc8oyVJ8Rzaz1BdTFe2E8tlTzLIMOsKXyxaXLI7nWkITHqkHIv1SvIxsk5xR+x6BbRyrTXp/dptjYXWpZ5Fjm3LGRXjcB8kUR5cB1zHdZSAjRVeCvYV0oqL/AA9o/wCaoz3KmfHqR9OLfspreDlGtKsErdGAjcuOBSTCrT5LTSCK6fjBLGceJEC5HkJNrCTJQI4JSnYphsmG9+O3S/TXbzrT003fWE0tEl7luNpmyXGda395h1jEyjGzYvhVLNFImxsiLQs/KZV2wWxpVsEq/GiOZ4KNHrGZxXbc/wBzczCnVLl+e+POux+O62kgtDRq0ti7kWsrIJMzE2tfAmrZrUxlglcq16cxCy+/GvV7zgul+PqWqMYwdb0vybxW13HG6FgMzMu38Wjq09jZF0RMVMXoxs1rV84UQULdm9Ey0Yj7s5012tvnfWV4jlE/vPQV+Wrlqysi0LkFF+Aa2xyHYk99fTWMn8avspFlWtbJGOmDMLEa/wCI6CIIip3nZjurs3P+zt1ofCt3Y71p1thEqzrr3Y92Nhj2FnTsCyUxjfo5SSZpvxq2BHeFnwR5EuTIRWoPlif9JnajsLvPXuSVPTym6fVePX8C2zXKIeRVUavnPh2cSe+bVU1ZkNq/81rI5Y8UNRCixnpJeSSZ/wAbfN0+zXSbsBrDtBeb71doXEu1eusyLOn2GDX5KA86ns7gYHWoZlNf2dQ4zGzgNl09xSSpkoYyGhzYkdjVPMigz/lBPK5+YvO2Sz6nZVl7usouwnV6bAHG+o0XYl3aX1FFUan4jq08nRrDZYs31VTUJy2y56XxK/sNHVbp4Q6N7hbR89jtjh4yOT6ItwZnLTv0MFnIaDv8j9zxruzl2mVFMGvcfFwUsVcnqR38ziouN9ay2rnNRueFq/A8o2BhWyqZogpkMHFJMKJMhGcFjWyIlk21r5lcZ7PyYvwzo0h51eNzbY6Pzz1De09PsrsbhO4qbDcQwm3uIVPhdhEQldkJ6iubZ2VTDAGM8UONBjSQRG2E50gsiaj1ag2MV6ZO9bev+fbPw3fgNr9RdX9TW5fgQsLwKTjEWg/dBv1YNz+6JF0WntLIoK1CDxp8eOcofldHkuaL3M8phFq6i9SDqRr7bmjqnUGLprO1kZHkZ9yXmSYy/D8drpVSyJdX1TOj5E2eZs+BBFJi1E+nZOFYvc1wRKZ68lG43YUh4+p0NzudzmanP9U0beKWzi6dXoGav7YE74npxqhVzMn3rU7OvbbX9wW7RiZlkxFI3OIvH21vmqPx7z/WXOl49B0t6MLeyLfNKyBR0cc2Y5c453NbZ9bV6rh01WPQ2IzJiIVE+O1R3s7WW1XkZLjadjNkxMrkwhKeBUOWMBlLRH/FGo4LEUQ5EiQ9vu9zvcV3lyp4RHMVOreJ5vn2HZjdUVLOt4Ydh2NeSdGAV4TSgYviJyq1zWORV8SmK7wv8XOVq+HIvHH34wZvWPj7kX6NnTt3XYtRlizas2LFh7Dj2/VrzMiaRx6zJyU+0f8AsTMec5+Wlc9W+Su0r5tXKp0U71tVarVq161eusJWP4qrrWAJAC+x/MRH1n2iY+/N0bjjjnbvOAeOOOOHh44444eHjjjjh4eOOOOHh44444eHnSZLEHPxy/gFeUYptNZxCEC5GGYOTCOF7xPc17Wla16uG5zHo16IqtcieF1BLTW19kWx5OkrneO9p+uTX5oBKCTnMQ0V0RZqtSP8BKF8T4mNXwwf4vsZ4RWtRUReOOcc+Va9exZ5oHoS8GWLKGC5QMFiGnV/RJiYlBKZ9R7rKJA/qPaJ+o87r8OWrNan1bK1h9c1V6lhRoaxRreoLf5PWSyGQcv2L82DMGH3PqUfc+bQPWnrzqvQGn8Y15rnHmwqGOJ9sctiRlhaWdvaMESwtLOc8Q3SpspwxoQnxjajBDGxjBsa1HHHOuVkqRWrpQpaUpSpalKAVqUsAEQWtYRAAACIiADECIxEREREecStOdZtWLFhrXve9rXPcwmuc1hkTGNYckbGGUyRmZSRFMyUzMzPn//Z

<p id="isPasted">A Consulta em Lote armazena em arquivo &uacute;nico o resultado obtido de um montante de consultas feitas ao Portal de Servi&ccedil;os e Solu&ccedil;&otilde;es.&nbsp;</p>

<p>Tem o objetivo de disponibilizar resultado de consultas sequenciais feitas ao Portal de Servi&ccedil;os e Solu&ccedil;&otilde;es em arquivo consolidado.</p>

<p><strong>Informa&ccedil;&otilde;es detalhadas do M&oacute;dulo</strong></p>

<p>O M&oacute;dulo pode ser acessado seguindo os seguintes passos:&nbsp;</p>

<ul>
	<li>Efetuar login no Portal de Servi&ccedil;os e Solu&ccedil;&otilde;es&nbsp;</li>
	<li>Acessar a op&ccedil;&atilde;o de menu lateral &ldquo;Lote&rdquo;</li>
</ul>

<p>Caso o objetivo seja consultar o resultado de um Lote, seguir os seguintes passos:&nbsp;</p>

<ul>
	<li>Efetuar login no Portal de Servi&ccedil;os e Solu&ccedil;&otilde;es (caso ainda n&atilde;o esteja logado).&nbsp;</li>
	<li>Acessar a op&ccedil;&atilde;o de menu lateral &ldquo;Lote&rdquo;</li>
</ul>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/59790AB9A82D3BF83D0B0CFDD1FB4D9E"></p>



<p>Efetuar login no sistema acessando o seguinte endere&ccedil;o: <a href="https://portaldesolucoes.cnseg.org.br/"><strong>https://portaldesolucoes.cnseg.org.br/</strong></a></p>

<p><strong><img src="https://s3.amazonaws.com/movidesk-files/BDB340B3C742BD5F620D8462E3249601" class="fr-fic fr-dib"></strong></p>

<p>Selecionar a op&ccedil;&atilde;o &ldquo;Lote&rdquo;.</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/78065A1EBEF29020689FA7462682364A">Clique em &ldquo;Adicionar&rdquo;.</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/D2CC789C948F1D20A5ED33E78549820D"></p>

<p>Clique em &ldquo;Escolha o arquivo&rdquo;.<img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/856074648CEDE55C4CFD38B44FA30080"></p>

<p>Selecione o arquivo a ser importado e clique em &ldquo;Abrir&rdquo;.&nbsp;</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/3160B31ED5C8DE3A257DE6E7D7B9D13C"></p>

<p>Preencha o campo &ldquo;Qtd. Linhas&rdquo; com a quantidade de linhas presentes no arquivo e selecione o(s) par&acirc;metro(s) desejado(s) no campo &ldquo;Par&acirc;metros&rdquo;.</p>

<p>Repare que enquanto escolhe os par&acirc;metros, os mesmos s&atilde;o inclu&iacute;dos na linha do campo &ldquo;Par&acirc;metros&rdquo;. Ao terminar de selecion&aacute;-los, clique em &ldquo;Buscar M&eacute;todos&rdquo;.&nbsp;</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/1EA656D2C71D433439F91BA57A5428B0"></p>

<p>Repare que o &ldquo;RENAVAM BASE ESTADUAL&rdquo; aparece como Produto que se utiliza dos par&acirc;metros selecionados.&nbsp;</p>

<p>Clique na seta ao lado do produto &ldquo;RENAVAM BASE ESTADUAL&rdquo; e clique em &ldquo;Utilizar?&rdquo;.&nbsp;</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/B00809CB8F93A0056B1AAF746CC665BC"></p>

<p>Clique tamb&eacute;m em &ldquo;Enviar&rdquo;.&nbsp;</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/21B6E2FC8FE5DE8A7D6E4796C8705081"></p>

<p>O portal apresentar&aacute; a mensagem de concord&acirc;ncia por parte do usu&aacute;rio quanto &agrave; cobran&ccedil;a por esta consulta.&nbsp;</p>

<p>Clique em &ldquo;Sim&rdquo;.&nbsp;</p>

<p>Caso o arquivo esteja corretamente configurado, aparecer&aacute; uma mensagem no canto superior direito informando que o envio foi efetuado com sucesso e a consulta passar&aacute; a constar da grade de consultas, conforme tela abaixo, com o status &ldquo;A processar&rdquo;.&nbsp;</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/2D97F01ACD81A799DA51F114F09916F1"></p>

<p>Quando estiver sendo processada, a consulta passar&aacute; para o status &ldquo;Em Processamento&rdquo;.&nbsp;</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/2065A86C7C02C11EF4C27772F49D341A"></p>

<p>Ao t&eacute;rmino do processamento, o status ser&aacute; alterado para &ldquo;Processado&rdquo;.</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/CF89978951AFBE4E0979B577993B0643"></p>

<p>Clicando na seta que est&aacute; ao lado do nome da empresa, a grade de processamento &eacute; expandida e aparecem dois &iacute;cones para o download de arquivos nos formatos XML e Excel.</p>

<p><img class="fr-fic fr-dib" src="https://s3.amazonaws.com/movidesk-files/4C2E76ED121C793CB306D3925210F05A"></p>

<p>Observa&ccedil;&atilde;o: O download do resultado gerado &eacute; efetuado atrav&eacute;s de um arquivo compactado. Para descompact&aacute;-lo, pode ser utilizada qualquer ferramenta de extra&ccedil;&atilde;o de arquivos (WinZip, WinRar etc.).</p>
