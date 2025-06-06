📦 Função de Cálculo de Valor Total de Vendas
Este módulo Python fornece uma função calcular_valor() que realiza o cálculo do valor total de uma compra de produtos, levando em consideração:

Quantidade de itens

Moeda de conversão (Real, Dólar ou Euro)

Descontos ou acréscimos aplicáveis

🚀 Objetivo
Facilitar o cálculo de vendas em diferentes moedas, aplicando corretamente regras de negócio como desconto ou acréscimo (mutuamente exclusivos), para apoiar a equipe de desenvolvimento na implementação de funcionalidades de interface gráfica e integração com banco de dados em sistemas comerciais.

🧮 Regras de Negócio Implementadas
O valor total é obtido multiplicando o valor unitário do produto pela quantidade.

É possível aplicar desconto ou acréscimo, mas não ambos simultaneamente.

A moeda padrão é o Real (BRL), mas é possível converter o valor final para:

Dólar (USD): 1 USD = R$ 5,00

Euro (EUR): 1 EUR = R$ 5,70

📌 Parâmetros da Função
python
Copiar
Editar
calcular_valor(valor_prod, qtde, moeda="real", **kwargs)
Parâmetro	Tipo	Obrigatório	Descrição
valor_prod	float	Sim	Valor unitário do produto em Reais
qtde	int	Sim	Quantidade de produtos
moeda	str	Não	Moeda para o resultado final: 'real', 'dolar', 'euro'
desconto	float	Não	Percentual de desconto sobre o valor bruto
acrescimo	float	Não	Percentual de acréscimo sobre o valor bruto

⚠️ Importante: Utilize apenas desconto ou acréscimo, nunca os dois ao mesmo tempo.

💡 Exemplo de Uso
python
Copiar
Editar
valor_a_pagar = calcular_valor(valor_prod=32, qtde=5, desconto=5)
print(f"O valor final da conta é {valor_a_pagar}")
Saída esperada:

cpp
Copiar
Editar
O valor final da conta é 152.0
❌ Tratamento de Erros
Caso a moeda informada não seja uma das esperadas (real, dolar, euro), a função retorna 0 e exibe uma mensagem:

nginx
Copiar
Editar
Moeda não cadastrada!
🛠️ Possíveis Melhorias Futuras
Validação automática para impedir entrada simultânea de desconto e acréscimo

Suporte para taxas de câmbio dinâmicas via API

Lançamento de exceções personalizadas ao invés de prints

Integração com camada de input/output e persistência de dados

📄 Licença
Este código é parte de um projeto interno da consultoria de software e está sob uso restrito do cliente do setor automotivo. Para fins educacionais ou de extensão, consulte sua liderança de equipe.
