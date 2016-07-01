# backend-portal-transparencia
Recomendações técnicas para o *back-end* de um "Portal da Transparência" de um município brasileiro. Detalhamento das recomendações no município de São Paulo, onde [houve recentemente consulta pública e previsão de licitação](http://www.prefeitura.sp.gov.br/cidade/secretarias/controladoria_geral/noticias/?p=217291).

# Introdução

A obrigatoriedade da publicação dos dados contábeis teve a sua origem nas Leis Complementares [nº 101 de 2000](http://www.lexml.gov.br/urn/urn:lex:br:federal:lei.complementar:2000-05-04;101) ("Lei de Responsabilidade Fiscal")   e [nº 131 de 2009](http://www.lexml.gov.br/urn/urn:lex:br:federal:lei.complementar:2009-05-27;131), depois reforçadas com a [Lei do Acesso à formação em 2011](http://www.lexml.gov.br/urn/urn:lex:br:federal:lei:2011-11-18;12527) (LAI).

Para responder à pergunta "Quais os requisitos obrigatórios (por lei) do *Portal da Transparência* de um município?" teríamos que recorrer às leis federais citadas, aos [decretos adicionais](http://www.portaldatransparencia.gov.br/sobre/Legislacao.asp) e ainda às demais normas que incidem sobre o município, o que foge ao escopo da deste projeto: precisamos apenas de um resumo desses requisitos oriundos das obrigações. Na concepção de um *Portal da Transparência* há que se levar em conta também os "[requisitos do cidadão](http://cafehacker.prefeitura.sp.gov.br/tag/portal-da-transparencia/)", e de orgãos de fiscalização tais como a Controladorias Gerais dos Municípios (CGMs). 

Para tanto, o ponto de partida mais simples é um resumo onde também se expressam os conceitos básicos envolvidos:

> O governo municipal precisa ser ***transparente*** quanto aos seus ***atos*** e as suas ***contas***. Transparente no sentido de "*publicar* para todo mundo ver" e também "para poder ser *auditado* por todos".

Cada um dos termos desse resumo informal pode ser detalhado abaixo e ainda complementado por links aos conceitos formais na Wikidata:

* **Transparência** hoje significa publicar dados oficiais simultaneamente nas entidades competentes de [depósito legal](https://www.wikidata.org/wiki/Q384840) (onde os dados adquirem valor de [prova jurídica](https://www.wikidata.org/wiki/Q176763)) e de amplo *acesso público à informação*, que, no cumprimento da LAI, se traduz em *publicar de forma organizada na Internet* e em [formatos abertos](http://5stardata.info/pt-BR/). Por fim o requisito de "poder ser [auditado](https://www.wikidata.org/wiki/Q181487)" requer também que haja *consistência* entre os diversos itens de dados, metadados ou conteúdos publicados.

* **Atos**: a publicidade dos atos fica parcialmente resolvida com o [Diário Oficial](https://www.wikidata.org/wiki/Q2065227) tradicional (papel e/ou PDF). Cada *ato* precisaria ser também ser também publicado como documento isolado na Internet, na forma de "separata", em formato aberto (ex. HTML com semântica de blocos marcados), e com identificador único oficial ([ePING](http://eping.governoeletronico.gov.br/) recomenda identificação por [URN LEX](https://www.wikidata.org/wiki/Q6537508) com resolução oficial no [Portal LexML](http://www.lexml.gov.br/)). <br/>*Exemplos*. Na Capital de SP a imprensa oficial se encarrega apenas do papel e do PDF *online*, quem resolve o segundo problema é [Diário Livre](http://devcolab.each.usp.br/do), ainda assim sem identificadores transparentes nem garantia de interoperabilidade. Em Campinas, por outro lado, não se publica mais em papel, e há publicação simultânea do Diário inteiro em PDF e das separatas em HTML, tendo havido também a preocupação em se publicar [boa parte dos *metadados* no LexML](http://www.lexml.gov.br/busca/search?f1-tipoDocumento=Legisla%C3%A7%C3%A3o;f2-localidade=Munic%C3%ADpios::Campinas%C2%A0-%C2%A0SP).

* **Contas**: são de diversos tipos, todas podem ser expressas em planilhas, idealmente fornecidas como [CSV do *tabular-data-model*](https://www.w3.org/TR/tabular-data-model/)... Apesar das normas de contabilidade, não há padrão ou respeito ao bom senso na publicação desses dados. Ainda assim a maioria das autoridades prestadoras de contas forencem ao menos uma indicação do "a fazer/fazendo/feito" na forma de valores relativos a ["planejado/empenhado/liquidado", como ilustrado pelo Cuidando](https://cuidando.vc/?/despesa/2016/2016.37.10.4.122.3024.33909200.90.92.0.2574). O problema grave, que se constata em qualquer auditoria, é a ausência de vínculo da *conta* com o *ato* que lhe deu origem. Perde-se a semântica e a rastreabilidade das contas &ndash; por exemplo sem uma coluna de "ID do Contrato" nas planilhas.
 
## Objetivo
Especificar a [arquitetura](https://www.wikidata.org/wiki/Q846636) geral e os padrões a serem respeitados por um sistema de software *online* que implemente o *Portal da Transparência* de um município, detalhando aspectos do [back-end](https://www.wikidata.org/wiki/Q14773417) deste sistema.

Especificar também, em mais detalhe, alguns casos, tais como o do município de São Paulo.

## Casos de requisitos detalhados
* [Requisitos do novo "Portal de Transparência" da capital de SP](docs/caseReqs-saoPaulo.md). Antigo em http://transparencia.prefeitura.sp.gov.br

* ...

# RECOMENDAÇÕES GERAIS

As recomendações foram divididas em RFCs: aquelas que foram votadas como pertinentes e relevantes, foram revisadas e publicadas como parte deste projeto:

* [RFC 01 - Padrões <i>data-interchange</i> recomendados](docs/rfc01.md)
* [RFC 02 - Modelo de referência para um Portal da Transparência do Município](docs/rfc02.md) 
* ... outros requisitos ...
 
## Recomendações específicas
Municípios com recomendações mais específicas:

* ... Recomendações para o back-end do Portal de Transparência do município de São Paulo ...
* ... outros municípios ...


-----

# Referências informais

Portais de contextualização e ilustração das práticas correntes:
* Portal da Transparência do poder executivo federal: http://www.portaltransparencia.gov.br/
* Portal da Transparência do poder executivo  estadual de SP: http://www.portaltransparencia.gov.br/
* Portal da Transparência do poder executivo municipal da capital de SP: http://transparencia.prefeitura.sp.gov.br
* ...

Avaliações realizadas sobre os portais existentes
* GODI: http://index.okfn.org/place/brazil/
* ... 


Iniciativas de formalização de requisitos de portais da transparência do Brasil

Ferramentas mais utilizadas nos portais da transparência:
* [CKAN](http://www.ckan.org) - plataforma de software para publicação de dados abertos.
* LexML - padrão brasileiro e portal para publicação de dados legislativos e jurídicos.
* 

Recursos de apoio:
* padrões a serem respeitados pelos portais: ePING, W3C.
* Transparência nas normas http://www.lexml.gov.br/
* Diários oficiais: http://www.imprensaoficial.com.br/ etc.
* ...


## Licença

O conteúdo deste projeto em si está licenciado sob a [licença Creative Commons Attribution 4.0] (http://creativecommons.org/licenses/by/4.0/), e o código-fonte subjacente e eventuais algoritmos licenciados sob a [licença MIT] (http://opensource.org/licenses/mit-license.php).

