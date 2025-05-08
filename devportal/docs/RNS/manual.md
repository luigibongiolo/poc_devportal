# Documentação da API SOAP - RNS Auto V6


## Visão Geral
Esta é a documentação para a API SOAP do projeto X. Ela utiliza o protocolo SOAP 1.2 e está hospedada em `https://example.com/soap`.

## Métodos de consulta

### `todosRamosPorCpf`
ADICIONAR INFO
 
 **Endpoint**
- **WSDL**: `https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6`

 **Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição          |
|-----------------|------------|-------------|--------------------|
| cdSeguradora    | String     | Não         | Código da seguradora |
| subCodigo       | String     | Não         | Subcódigo          |
| cdUsuario       | String     | Não         | Código do usuário  |
| dvUsuario       | String     | Não         | DV do usuário      |
| senha           | String     | Não         | Senha de acesso    |
| cpf             | String     | Não         | CPF para consulta  |

**SOAP Envelope**

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">
<soapenv:Header/>
    <soapenv:Body>
        <rns:todosRamosPorCpf>
            <!--Optional:-->
            <rns:cdSeguradora>?</rns:cdSeguradora>
            <!--Optional:-->
            <rns:subCodigo>?</rns:subCodigo>
            <!--Optional:-->
            <rns:cdUsuario>?</rns:cdUsuario>
            <!--Optional:-->
            <rns:dvUsuario>?</rns:dvUsuario>
            <!--Optional:-->
            <rns:senha>?</rns:senha>
            <!--Optional:-->
            <rns:cpf>?</rns:cpf>
        </rns:todosRamosPorCpf>
    </soapenv:Body>
</soapenv:Envelope>
```
 
**WSA**
- mustUnderstand: `NONE`
- version: `200508`
- action: `http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/todosRamosPorCpf`

### `verificaCadastroSeguradora`
ADICIONAR INFO

 **Endpoint**
- **WSDL**: `https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6`

 **Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição          |
|-----------------|------------|-------------|--------------------|
| cdSeguradora    | String     | Não         | Código da seguradora |
| subCodigo       | String     | Não         | Subcódigo          |
| cdUsuario       | String     | Não         | Código do usuário  |
| dvUsuario       | String     | Não         | DV do usuário      |
| senha           | String     | Não         | Senha de acesso    |

 **SOAP Envelope**
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">
   <soapenv:Header/>
   <soapenv:Body>
      <rns:verificaCadastroSeguradora>
         <!--Optional:-->
         <rns:cdSeguradora>?</rns:cdSeguradora>
         <!--Optional:-->
         <rns:subCodigo>?</rns:subCodigo>
         <!--Optional:-->
         <rns:cdUsuario>?</rns:cdUsuario>
         <!--Optional:-->
         <rns:dvUsuario>?</rns:dvUsuario>
         <!--Optional:-->
         <rns:senha>?</rns:senha>
      </rns:verificaCadastroSeguradora>
   </soapenv:Body>
</soapenv:Envelope>
```

 **WSA**

- mustUnderstand: `NONE`
- version: `200508`
- action: `http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/verificaCadastroSeguradora`

### `porPlaca`

**Endpoint**
- WSDL: `https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6`


 **Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição          |
|-----------------|------------|-------------|--------------------|
| cdSeguradora    | String     | Não         | Código da seguradora |
| subCodigo       | String     | Não         | Subcódigo          |
| cdUsuario       | String     | Não         | Código do usuário  |
| dvUsuario       | String     | Não         | DV do usuário      |
| senha           | String     | Não         | Senha de acesso    |
| uf              | String     | Não         | UF do veículo      |
| placa           | String     | Não         | Placa do veículo    |


**SOAP Envelope**
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">
   <soapenv:Header/>
   <soapenv:Body>
      <rns:porPlaca>
         <!--Optional:-->
         <rns:cdSeguradora>?</rns:cdSeguradora>
         <!--Optional:-->
         <rns:subCodigo>?</rns:subCodigo>
         <!--Optional:-->
         <rns:cdUsuario>?</rns:cdUsuario>
         <!--Optional:-->
         <rns:dvUsuario>?</rns:dvUsuario>
         <!--Optional:-->
         <rns:senha>?</rns:senha>
         <!--Optional:-->
         <rns:uf>?</rns:uf>
         <!--Optional:-->
         <rns:placa>?</rns:placa>
      </rns:porPlaca>
   </soapenv:Body>
</soapenv:Envelope>
```

**WSA**

- mustUnderstand: `NONE`
- version: `200508`
- action: `http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/porPlaca`

### `porOficina`

**Endpoint**  
- WSDL: https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6

  **Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição          |
|-----------------|------------|-------------|--------------------|
| cdSeguradora    | String     | Não         | Código da seguradora |
| subCodigo       | String     | Não         | Subcódigo          |
| cdUsuario       | String     | Não         | Código do usuário  |
| dvUsuario       | String     | Não         | DV do usuário      |
| senha           | String     | Não         | Senha de acesso    |
| CpfCnpj         | String     | Não         | CPF ou CPNJ da oficina |

**SOAP Envelope**  
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">  
   <soapenv:Header/>  
   <soapenv:Body>  
      <rns:porOficina>  
         <!--Optional:-->  
         <rns:cdSeguradora>?</rns:cdSeguradora>  
         <!--Optional:-->  
         <rns:subCodigo>?</rns:subCodigo>  
         <!--Optional:-->  
         <rns:cdUsuario>?</rns:cdUsuario>  
         <!--Optional:-->  
         <rns:dvUsuario>?</rns:dvUsuario>  
         <!--Optional:-->  
         <rns:senha>?</rns:senha>  
         <!--Optional:-->  
         <rns:cpfCnpj>?</rns:cpfCnpj>  
      </rns:porOficina>  
   </soapenv:Body>  
</soapenv:Envelope>  
```

**WSA**  

- mustUnderstand: NONE  
- version: 200508  
- action: http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/porOficina

### `porHistorico`

**Endpoint**  
- WSDL: https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6

 **Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição          |
|-----------------|------------|-------------|--------------------|
| cdSeguradora    | String     | Não         | Código da seguradora |
| subCodigo       | String     | Não         | Subcódigo          |
| cdUsuario       | String     | Não         | Código do usuário  |
| dvUsuario       | String     | Não         | DV do usuário      |
| senha           | String     | Não         | Senha de acesso    |
| cdChassi        | String     | Não         | Número do chassi do veículo |


**SOAP Envelope**  
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">  
   <soapenv:Header/>  
   <soapenv:Body>  
      <rns:porHistorico>  
         <!--Optional:-->  
         <rns:cdSeguradora>?</rns:cdSeguradora>  
         <!--Optional:-->  
         <rns:subCodigo>?</rns:subCodigo>  
         <!--Optional:-->  
         <rns:cdUsuario>?</rns:cdUsuario>  
         <!--Optional:-->  
         <rns:dvUsuario>?</rns:dvUsuario>  
         <!--Optional:-->  
         <rns:senha>?</rns:senha>  
         <!--Optional:-->  
         <rns:cdChassi>?</rns:cdChassi>  
      </rns:porHistorico>  
   </soapenv:Body>  
</soapenv:Envelope>  
```

**WSA**  

- mustUnderstand: NONE  
- version: 200508  
- action: http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/porHistorico


### `porDocumento`

**Endpoint**  
- WSDL: https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6

**Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição                   |
|-----------------|------------|-------------|-----------------------------|
| cdSeguradora    | String     | Não         | Código da seguradora        |
| subCodigo       | String     | Não         | Subcódigo                   |
| cdUsuario       | String     | Não         | Código do usuário           |
| dvUsuario       | String     | Não         | DV do usuário               |
| senha           | String     | Não         | Senha de acesso             |
| cpfCnpj         | String     | Não         | CPF ou CNPJ do documento    |

**SOAP Envelope**  
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">  
   <soapenv:Header/>  
   <soapenv:Body>  
      <rns:porDocumento>  
         <!--Optional:-->  
         <rns:cdSeguradora>?</rns:cdSeguradora>  
         <!--Optional:-->  
         <rns:subCodigo>?</rns:subCodigo>  
         <!--Optional:-->  
         <rns:cdUsuario>?</rns:cdUsuario>  
         <!--Optional:-->  
         <rns:dvUsuario>?</rns:dvUsuario>  
         <!--Optional:-->  
         <rns:senha>?</rns:senha>  
         <!--Optional:-->  
         <rns:cpfCnpj>?</rns:cpfCnpj>  
      </rns:porDocumento>  
   </soapenv:Body>  
</soapenv:Envelope>  
```

**WSA**

- mustUnderstand: NONE
- version: 200508
- action: http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/porDocumento

### `porComprador`

**Endpoint**  
- WSDL: https://rns-hmlg.cnseg.org.br/RegistroNacionalSinistroService/rnswebWSBloqSoapV6

**Parâmetros**

| Parâmetro       | Tipo       | Obrigatório | Descrição                   |
|-----------------|------------|-------------|-----------------------------|
| cdSeguradora    | String     | Não         | Código da seguradora        |
| subCodigo       | String     | Não         | Subcódigo                   |
| cdUsuario       | String     | Não         | Código do usuário           |
| dvUsuario       | String     | Não         | DV do usuário               |
| senha           | String     | Não         | Senha de acesso             |
| cpfCnpj         | String     | Não         | CPF ou CNPJ do comprador    |

**SOAP Envelope**  
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:rns="http://www.openuri.org/rnswebwsWebV2">  
   <soapenv:Header/>  
   <soapenv:Body>  
      <rns:porComprador>  
         <!--Optional:-->  
         <rns:cdSeguradora>?</rns:cdSeguradora>  
         <!--Optional:-->  
         <rns:subCodigo>?</rns:subCodigo>  
         <!--Optional:-->  
         <rns:cdUsuario>?</rns:cdUsuario>  
         <!--Optional:-->  
         <rns:dvUsuario>?</rns:dvUsuario>  
         <!--Optional:-->  
         <rns:senha>?</rns_nsec>  
         <!--Optional:-->  
         <rns:cpfCnpj>?</rns:cpfCnpj>  
      </rns:porComprador>  
   </soapenv:Body>  
</soapenv:Envelope>  
```

**WSA**

- mustUnderstand: NONE
- version: 200508
- action: http://www.openuri.org/rnswebwsWebV2/rnswebWSBloqHttpGet/porComprador