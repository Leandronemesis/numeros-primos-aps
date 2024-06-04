// Javascript
// turma 963R
// Leandro Antonio Castro da Silva
// 2024101220

// Função para verificar se um número é primo
function isPrime(num) {
    if (num <= 1) return false;
    if (num <= 3) return true;
    if (num % 2 === 0 || num % 3 === 0) return false;
    for (let i = 5; i * i <= num; i += 6) {
      if (num % i === 0 || num % (i + 2) === 0) return false;
    }
    return true;
}

// Função para encontrar os 10 maiores números primos a partir de um número fornecido pelo usuário
function findLargestPrimes() {
    const userNumber = parseInt(prompt("Por favor, insira um número:"));
    if (isNaN(userNumber)) {
        console.log("Entrada inválida. Por favor, insira um número válido.");
        return;
    }

    let count = 0;
    let num = userNumber;
    const primes = [];

    while (count < 10) {
        if (isPrime(num)) {
            primes.push(num);
            count++;
        }
        num++;
    }

    console.log("Os 10 maiores números primos a partir de " + userNumber + " são:");
    console.log(primes.join(", "));
}

// Chama a função findLargestPrimes para executar o programa
// findLargestPrimes();
// Explicação do Código
// Função isPrime(num):
// Verifica se o número num é menor ou igual a 1, caso em que não é primo.
// Verifica se o número num é 2 ou 3, que são primos.
// Elimina múltiplos de 2 e 3.
// Usa um loop para verificar divisibilidade por números de 5 até a raiz quadrada de num, com incremento de 6 (verificando i e i + 2), // // para otimizar a verificação.
// Função findLargestPrimes():

// Solicita ao usuário um número usando prompt.
// Verifica se a entrada do usuário é um número válido.
// Usa um loop while para encontrar os 10 maiores números primos a partir do número fornecido.
// Armazena os números primos encontrados em um array primes.
// Incrementa o número (num) a ser verificado após cada iteração.
// Quando encontra 10 números primos, exibe-os no console.
// Como Executar o Código
// Para executar o código, você pode:
// Copiar o código para um arquivo .html.
// Abrir o arquivo HTML no seu navegador.
// Aqui está um exemplo de como o arquivo HTML pode ser configurado:

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Encontre os 10 Maiores Números Primos</title>
</head>
<body>
    <script>
        // Insira o código JavaScript aqui
        // ...
    </script>
</body>
</html>
// Substitua o comentário // ... pelo código JavaScript fornecido. Abra o arquivo HTML no navegador e uma caixa de diálogo aparecerá para // você inserir um número. Os 10 maiores números primos a partir desse número serão exibidos no console do navegador (pressione F12 para // abrir o console).
