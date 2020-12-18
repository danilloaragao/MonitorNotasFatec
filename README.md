# Monitor de notas - Fatec-SP

O monitor de notas é um "robô" programado em C# (console application) cujo objetivo é monitorar o lançamento das notas finais no [portal da faculdade](http://san.fatecsp.br/index.php).

O robô funciona para qualquer curso da FATEC-SP.

### Funcionamento
Ao executar o MonitorNotas.EXE, será solicitado o RA, a Senha de acesso do portal da faculdade e, opcionalmente, um e-mail para notificar o lançamento das notas.
Após preencher os dados solicitados, o robô irá acessar o portal da faculdade com o seu login e senha para coletar as notas atuais e mostrá-las na tela, e então entrará em stand-by.
A cada 30 minutos o robô acessa novamente o portal, se não houve nenhum lançamento novo de notas, o robô irá exibir a data e a hora de execução e a mensagem "Processado com sucesso - Sem atualizações".
Caso ele encontre alguma lançamento novo de notas, ele mostrará as notas na tela, caso o e-mail tenha sido preenchido, ele disparará um e-mail automaticamente com todas as notas que foram lançadas até o momento.
Caso ocorra alguma falha no processamento, o robô irá exibir a data e a hora de execução e a descrição do erro, e entrará em stand-by por mais 30 minutos.
Caso o RA ou a senha esteja incorreto, o robô irá informar em tela, e aguardará que qualquer tecla seja pressionada para que ele encerre a execução.

O robô não grava ou compartilha o RA e senha dos usuários, ele mantém essas informações em memória apenas enquanto está sendo executado, portanto, ao encerrar e executar novamente as informações serão solicitadas.
