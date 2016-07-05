---
type: recomendação
vers: 0.1
vers_status: RASCUNHO
endorsed_n: 2
endorsed_status: waiting
layout: page
issue: 1
---

&#160; (série "[Request For Comments](https://en.wikipedia.org/wiki/Request_for_Comments) **desta iniciativa**)

#RFC 01 - Padrões *data-interchange* recomendados

Recomendação dos padrões a serem adotados no intercâmbio de dados entre módulos, na exposição de dados e na exposição de conteúdos de um Portal da Pransparência Municipal. 
Discussões desta RFC em [*issue-1*](https://github.com/CPT-PC/backend-portal-transparencia/issues/1), votos na [planilha aberta de votações](https://docs.google.com/spreadsheets/d/1hOSJ4OlYaha4b6c4bUE-hemDUQvEhSHESCRh7zRNZWI/edit#gid=1450924500).

## Conceitos consensuais

* arquitetura [SOA (service-oriented architecture)](https://www.wikidata.org/wiki/Q220644) e modularização com camadas. [2 votos]
* [REST](https://www.wikidata.org/wiki/Q749568) na comunicação HTTP entre módulos.  [2 votos] 

## Padrões fortemente recomendados

Subconjunto [ePING](http://eping.governoeletronico.gov.br/) somado a alguns padrões W3c recentes como o *tabular-data-model*, ou detalhes de protocolo, como JSON-RPC.

Padrão | Nota | Votos
------ | -----| -----
[HTML5](http://www.w3.org/TR/html5) | na publicação de conteúdos | 2 
[XHTML5](https://www.w3.org/TR/html5/the-xhtml-syntax.html#the-xhtml-syntax) | na representação interna de conteúdos | 2 
Semântica/[RDFa](http://www.w3.org/TR/rdfa-primer) | Marcação semântica de (X)HTML5 | 1
Semântica/[JSON-LD](https://www.json-ld.org) | expressão semântica em pacotes de dados| 1 
Semântica/ vocabulários | Em ordem de precedência: [schemaOrg](http://schema.org/)  [1 voto]; [Wikidata](https://www.wikidata.org) [1 voto];  ordem de mais recomendados do [LOV](http://lov.okfn.org/) [1 voto]. | -
dados abertos / CSV | Conforme fixado pela [RFC 4180](https://tools.ietf.org/html/rfc4180) e pela recente [W3C tabular-data-model](https://www.w3.org/TR/tabular-data-model/) | 1 
[JSON RPC](http://www.jsonrpc.org/specification) | no empacotamento dos dados intercambiados.  | 2
[UTF-8](https://en.wikipedia.org/wiki/UTF-8) | não se usa mais ASCII,  Windows-1252 ou ISO 8859-1. Qualquer JSON, CSV, XML, HTML ou TXT deve ser codificado em UTF8. | 1 voto

# Outros padrões recomendados

* Identificação única (transparente) de documentos legislativos e jurídicos através de [URN LEX](https://pt.wikipedia.org/wiki/Lex_(URN)), que faz parte do ePING e do [LexML](http://projeto.lexml.gov.br/). [1 voto]
      
* Acesso em massa: ver [*issue*#9](https://github.com/CPT-PC/backend-portal-transparencia/issues/9) 
* ... 

