# GeradorPython
#Gerador_de_orcamento
#Treinamento Python

print("Orçamento gerado com Sucesso!")
print("Semana do python na Prática!")

#Semana do python na Prática

#Entrada de Dados
input("Digite a descrição do projeto: ")
input("Digite o total de horas estimadas: ")
input("Digite o valor da hora trabalhada: ")
input("Digite o prazo estimado: ")

#Gravando Dados (variáveis)
projeto = input("Digite a descrição do projeto: ")
horas_estimadas = input("Digite o total de horas estimadas: ")
valor_hora = input("Digite o valor da hora trabalhada: ")
prazo = input("Digite o prazo estimado: ")

#Cálculos
valor_total = int(horas_estimadas) * int(valor_hora)
print(valor_total)

#Gerador PDF
!pip install fpdf

from fpdf import FPDF
from fpdf import FPDF
pdf = FPDF()
​
pdf.add_page()
pdf.set_font("Arial")
pdf.image("template.png", x=0, y=0)
​
pdf.text(115, 145, projeto)
pdf.text(115, 160, horas_estimadas)
pdf.text(115, 175, valor_hora)
pdf.text(115, 190, prazo)
pdf.text(115, 205, str(valor_total))
​
pdf.output("Orçamento.pdf")
print("Orçamento gerado com Sucesso!")

​
