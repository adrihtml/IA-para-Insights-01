# IA-para-Insights-01
Esse repositório é pra quem quer melhorar a extração de dados de forma inteligente. Usei uma IA preditiva pra analisar os bancos de dados e gerar insights que ajudam na criação e priorização de leads.  Além disso, o projeto identifica leads com alta chance de conversão, ajudando a planejar um remarketing mais assertivo. 

Cada variável pode ser adaptada conforme sua necessidade. As variavéis inseridas são exemplos que funcionam para as planilhas que utilizo e serve de exemplo para adaptação.

Foi utilizada a biblioteca *sklearn* e *seaborn* para a predição aos dados. 
Além das funções: 

    sklearn.model_selection import train_test_split
    sklearn.linear_model import LogisticRegression
    sklearn.metrics import classification_report
    
Foi incluido também as funções de limpeza e organização de linhas, parecido com o sistema binário da máquina, para ajudar na predição:

    def ler_dados_txt(caminho_txt):
    try:
        dados = []
        with open(caminho_txt, 'r') as file:
            for linha in file:
                partes = linha.split()  
                if len(partes) >= 2:  
                    telefone = partes[1]  
                    link = partes[-1]     
                    dados.append([telefone, link])



     dados["Respondeu"] = dados["Link"].apply(lambda x: 1 if x != '/' else 0)  
     # 1 = Respondeu
     0 = Não respondeu
     dados_modelo = dados[["Telefone", "Link", "Respondeu"]]

O modelo faz o treinamento, então á cada run, a probabilidade de acerto aumenta. Recomendo fazer a utilização até alcançar pelo menos 90% de acerto nas respostas, para sim aplicar os resultados nos seus projetos ou para decisões mais estratégicas:

    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)


Enfim, ele plota os gráficos dos dados resultantes do run. 
Pode ser personalizado os gráficos da forma que preferir, como por exemplo fazer um gráfico de pizza ou de barras. 
**Fica á seu critério!**

Por fim, agradeço a leitura dos pontos citados. Espero que você esteja claro como usar.

Fico à disposição em qualquer dúvida referente a este relatório. Você pode falar comigo pelo e-mail: adri.bill.cam@gmail.com

