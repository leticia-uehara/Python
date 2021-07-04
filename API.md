<h1> API <h1/>
  
<h2>1º Instalar o request <h2/>
  !pip install requests
  
 <h2> 2º Passo importar o request <h2/>
  import requests
  
 <h2> Adicionar a url da API <h2/>
  url = 'https://open.er-api.com/v6/latest/USD'
   
 <h2> Criar a variável request <h2/>
  req = requests.get(url)
   
 <h2> Motrar se a request existe <h2/>
  print(req.status_code)
   
  <h2> Ver os dados <h2/>
    dados = req.json()
    print(dados)
    
  <h2> Continuar o programinha <h2/>
    1. Solicitação da cotação em reais:
      valor_reais = float(input('Insira o valor em reais (da conversão): \n'))
    2. Criar a variável cotação:
      cotacao = dados['rates']['BRL']
    3. Mostrar o valor obtido:
      print(f'O valor de R$ {valor_reais} é de equivalente a {(valor_reais/cotacao):.2f} dólares')
