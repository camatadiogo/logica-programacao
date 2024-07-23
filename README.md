# Calculadora Simples em Python

Esta é uma calculadora simples em Python que permite ao usuário inserir dois números e escolher entre várias operações matemáticas básicas. O programa continuará executando até que o usuário escolha sair.

## Funcionalidades

- Solicitação de dois números do usuário.
- Validação das entradas para garantir que são números válidos.
- Conversão das entradas para o tipo `float`.
- Exibição de um menu de operações matemáticas disponíveis.
- Execução da operação escolhida pelo usuário.
- Pergunta ao usuário se deseja realizar outra operação ou sair.

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

---

## Como Usar

1. **Siga as instruções:**
   - Insira o primeiro número e pressione Enter.
   - Insira o segundo número e pressione Enter.
   - Escolha uma operação digitando o número correspondente e pressione Enter.
   - Veja o resultado da operação.
   - Escolha se deseja realizar outra operação ou sair do programa.

## Código Explicado

Aqui está uma explicação detalhada do código:

### Loop Principal

O loop principal do programa permite que ele continue executando até que o usuário escolha sair.

```python
while True:
```

### Entrada de Dados

O programa solicita que o usuário insira dois números. 

```python
num1 = input('Digite o primeiro número: ')
num2 = input('Digite o segundo número: ')
```

### Validação de Entrada

Verifica se as entradas são números válidos, considerando tanto ponto (`.`) quanto vírgula (`,`) como separadores decimais, e converte as entradas para o tipo `float`.

```python
if (num1.replace('.', '', 1).isdigit() or num1.replace(',', '', 1).isdigit()) and (num2.replace('.', '', 1).isdigit() or num2.replace(',', '', 1).isdigit()):
    num1 = float(num1.replace(',', '.'))
    num2 = float(num2.replace(',', '.'))
else:
    print('Por favor, insira valores númericos válidos.')
    continue
```

### Exibição do Menu de Operações

O programa exibe um menu com as operações disponíveis que o usuário pode escolher.

```python
print('\nEscolha uma operação:')
print('1. Soma')
print('2. Subtração')
print('3. Multiplicação')
print('4. Potenciação')
print('5. Divisão')
print('6. Sair')
operacao = input('\nDigite o número da operação desejada: ')
```

### Execução da Operação

Com base na escolha do usuário, o programa executa a operação correspondente e exibe o resultado.

```python
if operacao == '1':
    resultado = num1 + num2
    print(f'\nResultado da soma {resultado}\n')
elif operacao == '2':
    resultado = num1 - num2
    print(f'\nResultado da subtração {resultado}\n')
elif operacao == '3':
    resultado = num1 * num2
    print(f'\nResultado da multiplicação {resultado}\n')
elif operacao == '4':
    resultado = num1 ** num2
    print(f'\nResultado da potenciação {resultado}\n')
elif operacao == '5':
    if num2 != 0:
        resultado = num1 / num2
        print(f'\nResultado da divisão {resultado}\n')
    else:
        print('Não é possivel dividir por zero.')
elif operacao == '6':
    print('Fechando programa.')
    break
else:
    print('Operação inválida. Por favor, tente novamente.')
```

### Repetição ou Saída do Programa

Após cada operação, o programa pergunta se o usuário deseja realizar outra operação ou sair. Se o usuário optar por sair, o loop principal é interrompido, encerrando o programa.

```python
while True:
    exit = input('Você deseja realizar outra operação? (S/N): ').upper()
    if exit in ['S', 'N']:
        break
    else:
        print('Entrada inválida! Por favor, insira "S" para sim ou "N" para não.\n')

if exit == 'N':
    break
```

### Considerações Adicionais:

- Certifique-se de ter permissões adequadas para executar comandos `sudo` no sistema, pois o script pode solicitar privilégios administrativos para atualizar e instalar pacotes.
- Se houver erros durante a execução do script `calculadora.sh`, verifique as mensagens de erro no terminal para resolver problemas relacionados à instalação do Python 3 ou outras dependências.

Seguindo esses passos, você será capaz de executar o script `calculadora.sh` com sucesso em um ambiente Unix-like.

## Contribuições

Sinta-se à vontade para contribuir com melhorias para este projeto. Faça um fork do repositório, crie uma nova branch para suas alterações e envie um pull request.

---

Essa explicação no README deve ajudar os usuários a entenderem como o código funciona e como usá-lo.
