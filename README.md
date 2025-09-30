## Uso dos Scripts

### bindetect.py

O script `bindetect.py` serve para extrair strings de arquivos `.bin` do jogo Galaxy On Fire 2. Ele suporta os seguintes tipos de arquivos binários: `names`, `stations`, `systems` e `agents`.

**Exemplo de uso:**

```python
from bindetect import detectStrings

# Para extrair nomes de um arquivo names_*.bin:
nomes = detectStrings('caminho/para/names_xxx.bin', 'names', 'list')

# Para extrair nomes das estações:
estacoes = detectStrings('caminho/para/stations.bin', 'stations', 'list')

# Para extrair nomes dos sistemas:
sistemas = detectStrings('caminho/para/systems.bin', 'systems', 'list')

# Para extrair nomes dos agentes:
agentes = detectStrings('caminho/para/agents.bin', 'agents', 'list')

# O parâmetro 'returnType' pode ser 'list' (retorna uma lista) ou 'string' (retorna tudo em uma única string separada por quebras de linha).
```

### langdetect.py

O script `langdetect.py` permite extrair e escrever strings em arquivos `.lang` do jogo.

**Extrair strings de um arquivo .lang:**

```python
from langdetect import extractLang

strings = extractLang('caminho/para/arquivo.lang')
# Retorna uma lista com todas as strings extraídas.
```

**Escrever uma lista de strings em um arquivo .lang:**

```python
from langdetect import writeLang

writeLang(lista_de_strings, 'caminho/para/novo_arquivo.lang')
# Salva as strings no formato correto do jogo.
```
