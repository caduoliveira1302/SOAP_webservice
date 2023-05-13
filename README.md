# Integrantes
Abdul Malik de Barros RA00306190

Ana Carolina Zhang RA00297689

Carlos Eduardo de Oliveira RA00297792

Eduardo Furlani Rodrigues RA00297677

# Conceito

O protocolo SOAP é uma tecnologia amplamente utilizada em sistemas distribuídos e faz parte da arquitetura orientada a serviços (SOA). A
utilização de tecnologias baseadas em XML, como WSDL e XSD, permite a estruturação e validação dos dados trocados entre os aplicativos,
garantindo a integridade e confiabilidade da comunicação. As tecnologias usadas são: SOAP: Protocolo de comunicação baseado em XML
utilizado para troca de informações entre aplicativos. XML: Linguagem de marcação utilizada para estruturar dados em documentos. WSDL:
Linguagem utilizada para descrever serviços web, especificando como acessar e utilizar esses serviços. Com base na biblioteca usada, o Zeep,
como não possui middleware por padrão, porém, criamos "Transport" com um tempo limite (timeout) de 10 segundos, valendo ressaltar que o
middleware é responsável por controlar a comunicação entre o usuário e o servidor.

# Descrição POC

No primeiro código ("using a soap webservice") é um exemplo de como utilizar o Zeep, uma biblioteca Python para trabalhar com serviços web SOAP, para obter informações detalhadas sobre países.

Primeiramente, o código lê um arquivo JSON chamado "info.json" contendo uma lista de códigos ISO de países. Em seguida, os códigos ISO são convertidos em um DataFrame do Pandas.

Depois disso, o código configura o Zeep para se comunicar com o serviço web SOAP fornecido pela URL. O Zeep é configurado com um middleware de transporte com um tempo limite de 10 segundos.

Em seguida, o código chama o método "FullCountryInfo" do serviço web SOAP para cada código ISO de país na coluna "sISOCode" do DataFrame. O resultado de cada chamada é adicionado a uma lista chamada "country_list".

Depois de obter as informações detalhadas de todos os países, o código utiliza o helper "serialize_object" do Zeep para converter a lista de objetos "tCountryInfo" retornada pelo serviço web em um dicionário Python. O dicionário é então convertido em um DataFrame do Pandas para que as informações possam ser facilmente analisadas e manipuladas.

Finalmente, o código imprime as primeiras linhas do DataFrame para que possamos ver algumas das informações que foram coletadas.

Já no segundo código ("SOAP API request"), é uma implementação de uma requisição de serviço SOAP utilizando a biblioteca Requests e ElementTree do Python. O objetivo dessa requisição é converter uma temperatura em graus Celsius para Fahrenheit usando um serviço disponibilizado no site W3Schools.

A função soap_api_request recebe como parâmetro a temperatura em graus Celsius a ser convertida para Fahrenheit. Em seguida, é construídauma mensagem SOAP, que contém as informações necessárias para realizar a conversão. Essa mensagem é enviada para a URL do serviçousando o método HTTP POST, com o cabeçalho definido como Content-Type: text/xml; charset=utf-8.

A resposta do serviço é recebida como uma string, que é então analisada com o módulo ElementTree para extrair o resultado da conversão, que éretornado em graus Fahrenheit como uma string formatada na função.

# Referências bibliográficas

https://www.redhat.com/pt-br/topics/integration/whats-the-difference-between-soap-rest#:~:text=SOAP%20%C3%A9%20um%20protocolo%20padr%C3%A3o,tempo%20de%20carregamento%20das%20p%C3%A1ginas

https://blog.tecnospeed.com.br/rest-x-soap/#:~:text=%C3%89%20mais%20usado%20quando%20se,por%20meio%20de%20diferentes%20interfaces
