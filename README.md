# Visualizacao-de-Dados-de-Estoque-com-Matplotlib

import matplotlib.pyplot as plt
#Tendência de Estoque Diário
dias= [1,2,3,4,5,6,7,8]
estoque= [100,95,110,105,120,115,130,150]

plt.plot (dias, estoque, marker='.')
plt.title("Tendência de Estoque Diário")
plt.xlabel("Dias")
plt.ylabel("Estoque")
plt.yticks
plt.show()

#Comparação de Produtos
produtos=['Teclado', 'Mouse', 'Monitor', 'Webcam', 'Computador']
quantidades=[50,75,30,60,52]

plt.bar(produtos, quantidades, color= ['blue', 'green', 'red', 'yellow', 'purple'])
plt.title("Comparação de Produtos")
plt.xlabel("Produtos")
plt.ylabel("Quantidades")
plt.xticks(rotation=45, ha='right')
plt.tight_layout()
plt.show()

#Proporção de Categorias
#Valores total = 35000
#Eletronicos = 15000 = 42,85%, Vestuário = 8000 =  22,87%, Alimentos= 5000 = 14,28%, Eletrodomesticos = 7000 = 20%
categorias=['Eletrônicos', 'Vestuário', 'Alimentos', 'Eletrodomesticos']
valores=[42.85,22.87,14.28,20]
explode= (0.05, 0, 0, 0)

fig1, ax1 = plt.subplots()
ax1.pie(valores, 
        explode=explode, 
        labels=categorias,
        autopct='%1.1f%%',
        shadow=True,
        startangle=90,
        wedgeprops={"edgecolor":"black", 'linewidth':1, 'antialiased':True}
)
ax1.axis('equal')
plt.title("Proporção de Categorias")
plt.show()

#Preço vs Quantidade
preços=[50,120,300,80,20]
estoque=[80,25,10,70,150]
plt.figure(figsize=(10,6))
plt.scatter(preços, estoque, color='blue', alpha=0.7)
plt.title("Preço vs Quantidade")
plt.xlabel("Preço")
plt.ylabel("Quantidade")
plt.grid(True, linestyle='--', alpha=0.6)
plt.tight_layout()
plt.show()
