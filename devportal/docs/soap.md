
# Documentação da API SOAP

## Visão Geral
Esta é a documentação para a API SOAP do projeto X. Ela utiliza o protocolo SOAP 1.2 e está hospedada em `https://example.com/soap`.

## Endpoint
- **URL**: `https://example.com/soap/service`
- **WSDL**: `https://example.com/soap/service?wsdl`

## Métodos Disponíveis

### Método: `GetUser`
Recupera informações de um usuário pelo ID.

#### Parâmetros
| Nome   | Tipo   | Descrição          | Obrigatório |
|--------|--------|--------------------|-------------|
| userId | String | ID do usuário      | Sim         |

**Exemplo de Requisição SOAP**

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:urn="urn:example">
   <soapenv:Header/>
   <soapenv:Body>
      <urn:GetUser>
         <userId>12345</userId>
      </urn:GetUser>
   </soapenv:Body>
</soapenv:Envelope>
```

| Element        | Attributes          | Description                          |
|----------------|---------------------|--------------------------------------|
| `<person>`     | -                   | Container for person details         |
| `<name>`       | `type` (optional)   | The person's name                    |
| `<address>`    | -                   | Mailing address                      |