# backend-portal-transparencia
Recomendações técnicas gerais para o *back-end* de um "Portal da Transparência" de um município brasileiro, elaboradas colaborativamente por um coletivo de cidadãos interessados e conhecedores do tema; e recomendações detalhadas para o município de São Paulo, onde [houve recentemente consulta pública e previsão de licitação](http://www.prefeitura.sp.gov.br/cidade/secretarias/controladoria_geral/noticias/?p=217291).

# Introdução

A obrigatoriedade da publicação dos dados contábeis teve a sua origem nas Leis Complementares [nº 101 de 2000](http://www.lexml.gov.br/urn/urn:lex:br:federal:lei.complementar:2000-05-04;101) ("Lei de Responsabilidade Fiscal")   e [nº 131 de 2009](http://www.lexml.gov.br/urn/urn:lex:br:federal:lei.complementar:2009-05-27;131), depois reforçadas com a [Lei do Acesso à informação em 2011](http://www.lexml.gov.br/urn/urn:lex:br:federal:lei:2011-11-18;12527) (LAI).

Para responder à pergunta «&#160;Quais os requisitos obrigatórios (por lei) do *Portal da Transparência* de um município?&#160;» seria necessário revisar todas as obrigações expressas pelas leis federais citadas, pelos [decretos adicionais](http://www.portaldatransparencia.gov.br/sobre/Legislacao.asp) e ainda pelas demais normas que incidem sobre os municípios, o que foge ao escopo da deste projeto: estamos supondo que tais elementos já se encontram consolidados em outras iniciativas, cabendo a esta apenas indicá-las e resumir.

Além dos requisitos obrigatórios, há uma série de "requisitos voluntários" já consagrados na concepção de um *Portal da Transparência*, a serem também levados em conta:

* "requisitos das prefeituras" expressos na estrutura que se repete na maior parte dos portais,
* "[requisitos do cidadão](http://cafehacker.prefeitura.sp.gov.br/tag/portal-da-transparencia/)" obtidos dos mais diversos levantamentos,
* requisitos dos orgãos de fiscalização, tais como a Controladorias Gerais dos Municípios (CGMs).

As recomendações [da presente iniciativa](https://github.com/CPT-PC/backend-portal-transparencia) levam em conta todos esses requisitos, obrigatórios e voluntários.

## Conceitos básicos
Apesar da complexidade do tema, há como se expressar e discutir o assunto com base alguns conceitos norteadores e uma visão geral dos Portais da Transparência aparentemente consensual. O ponto de partida mais simples, para se resgatar tais conceitos e consensos, é um resumo das definições acrescido de links para os conceitos mais específicos:

> O governo municipal precisa ser ***transparente*** quanto aos seus ***atos*** e as suas ***contas***. Transparente no sentido de "*publicar* para todo mundo ver" e também "para poder ser *auditado* por todos".

Cada um dos termos desse resumo informal pode ser detalhado abaixo e ainda complementado por links aos conceitos formais na Wikidata:

* **Transparência** hoje significa publicar dados oficiais simultaneamente nas entidades competentes de [depósito legal](https://www.wikidata.org/wiki/Q384840) (onde os dados adquirem valor de [prova jurídica](https://www.wikidata.org/wiki/Q176763)) e de amplo *acesso público à informação*, que, no cumprimento da LAI, se traduz em *[publicar na Internet](https://www.wikidata.org/wiki/Q1153191) organizadamente* e em [formatos abertos](http://5stardata.info/pt-BR/). Por fim o requisito de "poder ser [auditado](https://www.wikidata.org/wiki/Q181487)" requer também que haja *consistência* entre os diversos itens de dados, metadados ou conteúdos publicados.

* **Atos**: a publicidade dos atos fica parcialmente resolvida com o [Diário Oficial](https://www.wikidata.org/wiki/Q2065227) tradicional (papel e/ou PDF). Cada *ato* precisaria ser também ser também publicado como documento isolado na Internet, na forma de "separata", em formato aberto (ex. HTML com semântica de blocos marcados), e com identificador único oficial ([ePING](http://eping.governoeletronico.gov.br/) recomenda identificação por [URN LEX](https://www.wikidata.org/wiki/Q6537508) com resolução oficial no [Portal LexML](http://www.lexml.gov.br/)). <br/>''Atos típicos'': leis, decretos, portarias, avisos de concurso, informes de contratações ou parcerias, licitações, termos de referência, contratos, extratos de contrato, adendos de contrato. <br/>*Exemplos*. Na Capital de SP a imprensa oficial se encarrega apenas do papel e do PDF *online*, quem resolve o segundo problema é [Diário Livre](http://devcolab.each.usp.br/do), ainda assim sem identificadores transparentes nem garantia de interoperabilidade. Em Campinas, por outro lado, não se publica mais em papel, e há publicação simultânea do Diário inteiro em PDF e das separatas em HTML, tendo havido também a preocupação em se publicar [boa parte dos *metadados* no LexML](http://www.lexml.gov.br/busca/search?f1-tipoDocumento=Legisla%C3%A7%C3%A3o;f2-localidade=Munic%C3%ADpios::Campinas%C2%A0-%C2%A0SP).

* **Contas**: são de diversos tipos, todas podem ser expressas em planilhas, idealmente fornecidas como [CSV do *tabular-data-model*](https://www.w3.org/TR/tabular-data-model/)... Apesar das normas de contabilidade, não há padrão ou respeito ao bom senso na publicação desses dados. Ainda assim a maioria das autoridades prestadoras de contas forencem ao menos uma indicação do "a&#160;fazer/fazendo/feito" na forma de valores relativos a ["planejado/empenhado/liquidado", como ilustrado pelo Cuidando](https://cuidando.vc/?/despesa/2016/2016.37.10.4.122.3024.33909200.90.92.0.2574). O problema grave, que se constata em qualquer auditoria, é a ausência de vínculo da *conta* com o *ato* que lhe deu origem. Perde-se a semântica e a rastreabilidade das contas &ndash; por exemplo sem uma coluna de "ID do Contrato" nas planilhas.

## Objetivo
Especificar a [arquitetura](https://www.wikidata.org/wiki/Q846636) geral e os padrões a serem respeitados por um sistema de software *online* que implemente o *Portal da Transparência* de um município, detalhando aspectos do [back-end](https://www.wikidata.org/wiki/Q14773417) deste sistema.

Especificar também, em mais detalhe, alguns casos, tais como o do município de São Paulo.

## Casos com requisitos mais detalhados
* [Requisitos do novo "Portal de Transparência" da capital de SP](docs/caseReqs-saoPaulo.md)

* ...

# RECOMENDAÇÕES GERAIS

As recomendações foram divididas em RFCs: aquelas que foram votadas como pertinentes e relevantes, foram revisadas e publicadas como parte deste projeto:

* [RFC 01 - Padrões <i>data-interchange</i> recomendados](docs/rfc01.md)
* [RFC 02 - Modelo de referência para um Portal da Transparência do Município](docs/rfc02.md)
* ... outros requisitos ...

Todas as RFCs fazem use de termos e conceitos adotados especificamente para o contexto deste projetos, sendo descritos na documento (apelidado de RFC 00) das [Predefinições deste projeto](docs/predefinicoes.md).

## Recomendações específicas
Municípios com recomendações mais específicas:

* ... Recomendações para o back-end do Portal de Transparência do município de São Paulo ...
* ... outros municípios ...


-----
PS: [referências informais na Wiki](https://github.com/CPT-PC/backend-portal-transparencia/wiki/REFER%C3%8ANCIAS-INFORMAIS).

## Licença

O conteúdo deste projeto em si está licenciado sob a [licença Creative Commons Attribution 4.0] (http://creativecommons.org/licenses/by/4.0/), e o código-fonte subjacente e eventuais algoritmos licenciados sob a [licença MIT] (http://opensource.org/licenses/mit-license.php).
