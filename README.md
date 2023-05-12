# Integrantes
Abdul Malik de Barros RA00306190
Ana Carolina Zhang RA00297689
Carlos Eduardo de Oliveira RA00297792
Eduardo Furlani Rodrigues RA00297677

# 1.Conceito

O protocolo SOAP é uma tecnologia amplamente utilizada em sistemas distribuídos e faz parte da arquitetura orientada a serviços (SOA). A
utilização de tecnologias baseadas em XML, como WSDL e XSD, permite a estruturação e validação dos dados trocados entre os aplicativos,
garantindo a integridade e confiabilidade da comunicação. As tecnologias usadas são: SOAP: Protocolo de comunicação baseado em XML
utilizado para troca de informações entre aplicativos. XML: Linguagem de marcação utilizada para estruturar dados em documentos. WSDL:
Linguagem utilizada para descrever serviços web, especificando como acessar e utilizar esses serviços. Com base na biblioteca usada, o Zeep,
como não possui middleware por padrão, porém, criamos "Transport" com um tempo limite (timeout) de 10 segundos, valendo ressaltar que o
middleware é responsável por controlar a comunicação entre o usuário e o servidor.

# 2.Prática

O SOAP é um protocolo de transferência de dados e o Selenium é uma ferramenta de automação de testes em navegadores. No entanto, usamos
o Selenium para interagir com a interface do usuário do WebService, isto é, usamos o Selenium para navegar até a página do serviço da Web e
preencher os campos do formulário

# Descrição POC

Este código é um exemplo de como utilizar o Selenium e o Zeep para obter informações de um país por meio de um serviço da Web SOAP.

A biblioteca Selenium é usada para automatizar interações com um navegador da Web. Neste código, a página da Web contendo o formulário é carregada usando o Selenium. Em seguida, o campo do país é preenchido com o valor "US" e o botão de pesquisa é clicado para obter informações sobre os Estados Unidos.

O Zeep é uma biblioteca Python para trabalhar com serviços da Web SOAP. Neste código, ele é usado para chamar a função FullCountryInfo do serviço da Web, passando "US" como parâmetro. O resultado é armazenado na variável "result" e impresso no console.

Ao usar SOAP, é necessário especificar a URL do WSDL do serviço da Web, que contém a descrição dos métodos disponíveis e dos parâmetros esperados.

No geral, este código é uma prova de conceito (POC) de como combinar o Selenium e o Zeep para automatizar a interação com um formulário da Web e chamar um serviço da Web SOAP para obter informações sobre um país.

# Referências bibliográficas

https://www.redhat.com/pt-br/topics/integration/whats-the-difference-between-soap-rest#:~:text=SOAP%20%C3%A9%20um%20protocolo%20padr%C3%A3o,tempo%20de%20carregamento%20das%20p%C3%A1ginas

https://blog.tecnospeed.com.br/rest-x-soap/#:~:text=%C3%89%20mais%20usado%20quando%20se,por%20meio%20de%20diferentes%20interfaces