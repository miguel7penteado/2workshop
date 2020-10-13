# Segundo Seminário de DataScience IBGE USP
### *Videoconferência IBGE USP 14 de outubro de 2020* 

# AGENDA

## SIDRA

### Exercício 1
### Exercício 2
### Exercício 3
### Exercício 4

## API SIDRA

### Exercício 1

* [Acesso ao SIDRA http://sidra.ibge.gov.br](http://sidra.ibge.gov.br)
* [Descrever os metadados da API](http://api.sidra.ibge.gov.br/)
* [Consultar a API SIDRA](https://apisidra.ibge.gov.br/values/)

```bash
# Testar o XML
curl -H "Accept: application/xml" -X GET https://apisidra.ibge.gov.br/values/t/202/n102/3518800032/p/2010

# Testar o JSON
curl -H "Accept: application/json" -X GET https://apisidra.ibge.gov.br/values/t/202/n102/3518800032/p/2010

# Testar o Texto Puro
curl -H "Accept: text/plain" -X GET https://apisidra.ibge.gov.br/values/t/202/n102/3518800032/p/2010
```

#### Exercício 1 utilizando a biblioteca `sidrar` obviamente em R

```R
install.packages("sidrar");
library(sidrar);
minha_tabela <- get_sidra(api = "/t/202/n102/3518800032/p/2010");
describe(minha_tabela);
names(minha_tabela);
str(minha_tabela);
minha_tabela
```
#### Exercício 1 utilizando a biblioteca `sidrapy` obviamente em python

linux
```bash
export PATH="${PATH}:$(python3 -m site --user-base)/bin"
export PYTHONPATH="${PYTHONPATH}:$(python3 -m site --user-base)/lib/python3.8"
pip3 install --user --upgrade sidrapy
```

```python
import sidrapy

minha_tabela = sidrapy.get_table(table_code="202", territorial_level="102", ibge_territorial_code="3518800032", period="2010")
minha_tabela.info()
minha_tabela.V
minha_tabela['V']
minha_tabela

```


### Exercício 2
### Exercício 3
### Exercício 4


## ACESSO FTP E GEOFTP

```bash

```
