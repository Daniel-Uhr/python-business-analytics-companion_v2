# Ambiente de execução

Conferido com CPython 3.11.5 em Windows de 64 bits e as versões registradas. `requirements.lock.txt` inclui os hashes dos pacotes verificados; `runtime-freeze.txt` registra o ambiente utilizado. `requirements.txt` lista as versões sem restringir os arquivos de instalação por plataforma. Esta conferência não certifica outros sistemas ou o ambiente do Google Colab.

Use uma interface Jupyter e selecione o kernel Python correspondente ao ambiente. Abra os notebooks do estudante com a pasta `pt-br` como diretório de trabalho. Preserve a estrutura completa de dados. Os blocos Python das páginas de resolução usam esse mesmo diretório; execute-os na ordem apresentada.

Para instalar as dependências em um novo ambiente isolado compatível, entre nesta pasta e use:

```text
python -m pip install --require-hashes -r requirements.lock.txt
```

Uma interface Jupyter compatível deve estar disponível ou ser instalada separadamente. O repositório não inclui os pacotes de instalação. Nenhuma instalação ou atualização foi necessária nesta conferência.
