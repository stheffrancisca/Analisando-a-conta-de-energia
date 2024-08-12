# Analisando-a-conta-de-energia
Analisando a conta de energia.


### Você está analisando a conta de energia de um pequeno escritório e precisa saber:
1. Qual o valor total da conta de energia em cada mês do ano
2. Qual o valor total da conta de energia no ano

Considere as listas dadas como os 12 meses do ano, tanto para bandeiras quanto para consumo. O valor da conta é dado por: consumo * multiplicador_bandeira * preco_kwh

bandeiras_tarifarias = ["vermelha", "vermelha", "amarela", "amarela", "verde", "verde", "verde", "verde", "verde", "amarela", "amarela", "amarela"]
consumo_kwh = [400, 350, 325, 350, 200, 220, 250, 290, 360, 290, 300, 300]
preco_kwh = 1.3
multiplicador = {"vermelha": 2, "amarela": 1.3, "verde": 1}
precos_meses = []
for i, bandeira in enumerate(bandeiras_tarifarias):
    preco = multiplicador[bandeira] * preco_kwh * consumo_kwh[i]
    precos_meses.append(preco)

print(precos_meses)
print("Total Ano:", sum(precos_meses))
