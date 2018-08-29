## Tutorial: configurando XDebug no Wamp :smiley:

Antes de começarmos, será necessário que você instale e configure o WampServer de acordo com a sua preferência.
Depois de configurado, faça o download do [xdebug](https://xdebug.org/download.php).

Salve o arquivo `.dll` dentro do diretório `diretorio/do/wamp/bin/php/php.versao.do.php/zend_ext/`

Com o download finalizado, abra o arquivo `php.ini` da versão do PHP que está ativa e insira o código abaixo:

```ini

[Xdebug]

zend_extension ="diretorio/do/wamp/bin/php/php.versao.do.php/zend_ext/arquivo_do_xdebug.dll"
xdebug.remote_autostart=On
xdebug.remote_enable=On
xdebug.remote_port=9001
xdebug.profiler_enable=On
xdebug.profiler_enable_trigger=On
xdebug.profiler_output_dir="diretorio/do/wamp64/tmp"
xdebug.profiler_output_name="cachegrind.out.%t.%p"
xdebug.show_local_vars=0
```

Após, reinicie os serviços do WampServer e verifique se a extensão está ativada.
Se tudo correu bem, basta configurar a IDE ou editor de código de sua prefência para realizar o debug.
