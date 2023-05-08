# PROJETO-DINAMICA-DAS-M-QUINAS
Codigo em Python para efeito de comparação das forças e angulos c/ e s/ contrapeso
import matplotlib.pyplot as plt
import numpy as np

# Dados para o primeiro gráfico
angles1 = [0,55.56,111.11,166.67,222.22,277.78,333.33,355.56,388.89,416.67,444.44,500,555.56,611.11,666.67,720]
pressao1 = [0, 567.6681276, 594.0113689, 154.1732831, 533.5785392, 1268.099377, 2291.74424, 516.5261773, 760.4891098, 671.494616, 462.504895, 218.5351889, 60.01526993, 219.8306886, 184.2472509, 0]
torque1 = [1088.699299, 2250.180384, 2083.458874, 2182.849985, 2593.702072, 4190.451231, 16669.19295, 21780.11168, 5139.249217, 2627.530294, 1521.523751, 1110.416045, 730.3432717, 760.345312, 750.8305477, 1088.699299]

# Dados para o segundo gráfico
angles2 = [0, 55.56, 111.11, 166.67, 222.22, 277.78, 333.33, 355.56, 388.89, 416.67, 444.44, 500, 555.56, 611.11, 666.67, 720]
pressao2 = [0, 118.9089958, 28.29046674, 83.71493078, 131.1849221, 460.7372884, 1894.163833, 431.6570475, 366.0936958, 208.9009829, 323.2039033, 179.2888961, 209.7361618, 419.1116534, 235.443373, 0]
torque2 = [2510.749372, 470.6543513, 98.9925827, 1185.260066, 637.2670045, 1517.968605, 13775.53519, 18201.47362, 2473.557011, 816.1632756, 1060.029502, 910.4984225, 2552.296893, 1445.994936, 958.202963, 2510.749372]

# Convertendo os ângulos para radianos
angles1 = np.radians(angles1)
angles2 = np.radians(angles2)

# Criando a figura com duas subplots
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(12, 6))

# Plotando as curvas no primeiro subplot
ax1.plot(angles1, pressao1, label="pressao")

ax1.plot(angles1, torque1, label="torque")

#Definindo o título e os rótulos dos eixos do primeiro subplot
ax1.set_title("Gráfico com contrapeso na manivela")
ax1.set_xlabel("Ângulo (rad)")
ax1.set_ylabel("Força (N)")

#Adicionando legenda no primeiro subplot
ax1.legend()

#Plotando as curvas no segundo subplot
ax2.plot(angles2, pressao2, label="pressao")
ax2.plot(angles2, torque2, label="torque")

#Definindo o título e os rótulos dos eixos do segundo subplot
ax2.set_title("Gráfico Senoidal")
ax2.set_xlabel("Ângulo (rad)")
ax2.set_ylabel("Forças (N)")

#Adicionando legenda no segundo subplot
ax2.legend()

#Exibindo o gráfico
plt.show()


