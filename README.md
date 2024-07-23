Este código é uma calculadora simples que permite ao usuário serir dois números, escolher uma operação matemática (soma, subtração, multiplicação, potenciação ou divisão) e exibir o resultado. O programa continua rodando até que o usuário escolha sair.

Para executar o arquivo `calculadora.sh`, é necessário ter um ambiente Unix-like com Bash (Bourne Again Shell) instalado. Abaixo segue informações das ações necessárias para que ele funcione corretamente.

### Pré-requisitos:

1. **Sistema Operacional:**
   - O script `calculadora.sh` foi projetado para ser executado em sistemas operacionais baseados em Unix, como Linux ou macOS. No Windows, é possível executar scripts Bash usando o subsistema Windows para Linux (WSL) ou outras ferramentas que suportam a execução de scripts Bash.

2. **Permissões:**
   - Antes de executar o script, certifique-se de que o arquivo `calculadora.sh` tenha permissões de execução adequadas. Se necessário, você pode conceder permissões de execução com o comando:
     ```bash
     chmod +x calculadora.sh
     ```
3. **Python 3:**
   - O script Python `calculadora.py` requer Python 3 instalado no sistema. Caso você não tenha o Python 3 instalado ele será instalando quando executar o script `calculadora.sh`.

### Executando o `calculadora.sh`:

Para executar o script `calculadora.sh`, siga estes passos:

1. **Abra um Terminal:**
   - Abra um terminal no seu sistema operacional. No Linux ou macOS, você pode usar o Terminal integrado. No Windows com WSL, utilize o terminal do WSL.

2. **Navegue até o Diretório:**
   - Use o comando `cd` para navegar até o diretório onde o arquivo `calculadora.sh` está localizado. Por exemplo:
     ```bash
     cd /caminho/para/o/diretorio
     ```

3. **Conceda Permissões (se necessário):**
   - Se ainda não tiver concedido permissões de execução ao script, execute:
     ```bash
     chmod +x calculadora.sh
     ```

4. **Execute o Script:**
   - Agora, execute o script `calculadora.sh` usando:
     ```bash
     ./calculadora.sh
     ```
     Isso iniciará a execução do script Bash. Ele primeiro atualizará os pacotes do sistema e, em seguida, tentará instalar o Python 3 se ainda não estiver instalado.

5. **Siga as Instruções:**
   - Após a instalação do Python 3 (se necessário), o script Python `calculadora.py` será executado automaticamente. Siga as instruções no terminal para usar a calculadora e realizar operações matemáticas.

### Considerações Adicionais:

- Certifique-se de ter permissões adequadas para executar comandos `sudo` no sistema, pois o script pode solicitar privilégios administrativos para atualizar e instalar pacotes.
- Se houver erros durante a execução do script `calculadora.sh`, verifique as mensagens de erro no terminal para resolver problemas relacionados à instalação do Python 3 ou outras dependências.

Seguindo esses passos, você será capaz de executar o script `calculadora.sh` com sucesso em um ambiente Unix-like.
