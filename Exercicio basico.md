### 1. Calculadora de Média (Variáveis, Operadores, `if/else`)

**Objetivo:** Determinar se um aluno foi aprovado ou reprovado.

1. Declare três variáveis usando `const`: `nota1`, `nota2` e `nota3`, atribuindo valores de 0 a 10 a elas.
    
2. Calcule a `media` das notas e armazene-a em uma variável `let`.
    
3. Use um bloco `if/else` para:
    
    - Imprimir no console a mensagem "Parabéns, você foi Aprovado!" se a `media` for maior ou igual a 7.
        
    - Imprimir "Você está de Recuperação." se a `media` for maior ou igual a 5 e menor que 7.
        
    - Imprimir "Reprovado. Precisa estudar mais." se a `media` for menor que 5.

### 2. Conversor de Temperatura (`const`, Operadores Matemáticos)

**Objetivo:** Converter a temperatura de Celsius para Fahrenheit.

1. Declare uma `const` chamada `celsius` e atribua um valor (ex: 25).
    
2. Crie uma variável `let` chamada `fahrenheit`.
    
3. Atribua a `fahrenheit` o resultado da conversão, usando a fórmula: $F = C \times (9/5) + 32$.
    
4. Imprima no console o valor final de `fahrenheit`.

### 3. Validação de Idade (Ternário e Lógico `&&`)

**Objetivo:** Verificar se uma pessoa é maior de idade e está com o documento em dia.

1. Declare as variáveis `let idade = 20;` e `const documentoOK = true;`.
    
2. Crie uma variável `const statusEntrada`.
    
3. Use o **operador ternário** para definir o valor de `statusEntrada`:
    
    - A condição deve verificar se a `idade` é maior ou igual a 18 **E** se `documentoOK` é `true`.
        
    - Se a condição for verdadeira, atribua o valor `"Pode entrar."`.
        
    - Se for falsa, atribua o valor `"Entrada negada."`.
        
4. Imprima `statusEntrada`.

### 4. Controle de Semáforo (`switch`)

**Objetivo:** Simular o estado de um semáforo com base em uma cor.

1. Declare uma variável `const corSemaforo = "amarelo";`
    
2. Use uma estrutura `switch` com a variável `corSemaforo` para imprimir a ação correta:
    
    - `case "verde"`: Imprimir "Siga em frente."
        
    - `case "amarelo"`: Imprimir "Atenção! Reduza a velocidade."
        
    - `case "vermelho"`: Imprimir "Pare o carro imediatamente."
        
    - `default`: Imprimir "Cor inválida."

### 5. Cálculo de Desconto (Comparação de Tipos `===`)

**Objetivo:** Aplicar um desconto, mas somente se o código for um número inteiro.

1. Declare `let valorCompra = 300;`
    
2. Declare `const codigoPromocional = 10;` (Atenção: mude o tipo para string, por exemplo, `"10"`, para testar a falha).
    
3. Use um `if` para verificar se `codigoPromocional` é **igual em valor e tipo** a `10`.
    
4. Se for estritamente igual:
    
    - Calcule o `valorFinal` subtraindo 10% do `valorCompra`.
        
    - Imprima o `valorFinal`.
        
5. Se não for estritamente igual:
    
    - Imprima "Código inválido ou tipo incorreto. Preço cheio."
        
    - Imprima o `valorCompra`.

### 6. Sistema de Prioridade (Lógico `||` e `if/else`)

**Objetivo:** Dar prioridade de atendimento a idosos, gestantes ou pessoas com deficiência.

1. Declare as variáveis booleanas: `const idadeAvancada = false;`, `const gestante = false;`, `const pcd = true;`.
    
2. Use um `if/else` com o operador lógico `||` (OR) para verificar se **pelo menos uma** das condições de prioridade é `true`.
    
3. Se a condição for verdadeira, imprima: "Atendimento Prioritário - Dirija-se ao guichê especial."
    
4. Caso contrário, imprima: "Atendimento Normal - Aguarde na fila comum."

### 7. Verificação de Permissão (Curto-Circuito `&&`)

**Objetivo:** Exibir uma mensagem de edição somente se o usuário for administrador.

1. Declare `const usuarioAdmin = true;` (Mude para `false` para testar).
    
2. Declare `let mensagem = "Página Inicial";`
    
3. Use o operador de curto-circuito `&&` para alterar a `mensagem` para `"Página de Administração e Edição"` **somente se** `usuarioAdmin` for `true`.
    
    - _Dica: `usuarioAdmin && (mensagem = "...");`_
        
4. Imprima a `mensagem` final.

### 8. Definição do Tipo de Envio (Ternário Aninhado)

**Objetivo:** Determinar o custo do frete com base no peso e destino.

1. Declare as variáveis `const pesoKg = 5;` e `const destino = "capital";`.
    
2. Crie uma variável `const custoFrete`.
    
3. Use o **operador ternário aninhado** (um ternário dentro do outro) para definir o custo:
    
    - Se `destino` for `"capital"`:
        
        - Se `pesoKg` for menor ou igual a 10, o custo é 20.
            
        - Caso contrário, o custo é 35.
            
    - Se `destino` não for `"capital"`: o custo é 50.
        
4. Imprima: `O custo do frete é R$ ${custoFrete}.`

### 9. Classificação de Número (Múltiplos `else if`)

**Objetivo:** Classificar um número em um intervalo específico.

1. Declare uma variável `const numero = 42;`.
    
2. Use a estrutura `if/else if/else` para:
    
    - Se o `numero` for maior que 100: Imprimir "Número muito grande."
        
    - Se o `numero` for maior que 50: Imprimir "Número médio/grande."
        
    - Se o `numero` for maior que 10: Imprimir "Número pequeno/médio."
        
    - Caso contrário: Imprimir "Número muito pequeno."

### 10. Sistema de Pontuação (Combinação de Operadores e `let/const`)

**Objetivo:** Calcular a pontuação final e verificar se o bônus foi aplicado.

1. Declare `const pontosBase = 50;`
    
2. Declare `let multiplicador = 2;`
    
3. Declare `const ganhouBonus = true;`
    
4. Declare `let pontosFinais;`
    
5. Calcule os `pontosFinais` usando a fórmula: $pontosFinais = pontosBase \times multiplicador$.
    
6. Use um `if` simples com `ganhouBonus`:
    
    - Se `ganhouBonus` for `true`, adicione 100 pontos aos `pontosFinais` (Dica: use um operador de atribuição como `+=`).
    
7. Imprima: "Pontuação Base: ${pontosBase}" e "Pontuação Final: ${pontosFinais}".