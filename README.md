# Projeto-FOGUETE




#Inicio do Trabalho
from random import Random

#Definir objetivo do trabalho
#"O objetivo desta operação é realizar o lançamento do foguete de forma segura para todos os tripulantes,\npor meio da análise dos diferentes parâmetros e status operacionais do sistema da nave. Essa verificação\ninclui a avaliação de fatores como temperatura interna e externa, integridade estrutural, níveis de energia,\npressão dos tanques e funcionamento dos módulos críticos, garantindo que todas as condições estejam dentro\ndos limites seguros estabelecidos antes da autorização do lançamento.\n\n")
  #  determinando as variaves como 0 para depois deixar elas randomizadas:
temperatura_interna = 0
temperatura_externa = 0
integridade_estrutural = 0
energia = 0
pressao_tanque = 0
modulos_criticos = 0




#importando uma biblioteca (random) que basicamente traz numeros aleatorios
import random


#colocando a biblioteca random com o codigo 'randint' para deixar uma randomizaçao de numeros inteiros:

temperatura_interna = random.randint(10,30)
temperatura_externa = random.randint(-20,35)
energia = random.randint(50, 100)
pressao_tanque = random.randint(20,60)
integridade_estrutural = random.randint(0,1)
modulos_criticos = random.randint(0,1)

#declarando as variaveis da Margem para calcular o quanto de margem foi passado ou quanto falta para atingir o minimo necessario para o lançamento

temperatura_interm = 0
temperatura_externam = 0
energiam = 0
pressao_tanquem = 0
integridade_estruturalm = 0
modulos_criticosm = 0


#calculo da margem

temperatura_interm =  temperatura_interm - temperatura_interna
temperatura_externam = temperatura_externam - temperatura_externa
energiam = energiam - energia
pressao_tanquem = pressao_tanquem - pressao_tanque
integridade_estruturalm = integridade_estruturalm - integridade_estrutural
modulos_criticosm = modulos_criticosm - modulos_criticos


#esta parte do codigo a seguir verifica se o fogue esta pronto para decolagem se estiver com 1 pode decolar,
#se estiver com 0 nao esta apto para decolagem.



#esta parte do codigo mostra os parametros que a nave tem no momento de forma aleatoria!
print("verificando statos da nave...\n")

print("\n------------------ TELEMETRIA E ANÁLISE DO FOGUETE ------------------\n")

print("| Parâmetro                         | Status Atual | Status Mínimo | Margem |")
print("|-----------------------------------|--------------|---------------|--------|")

print(f"| Temperatura interna da nave       | {temperatura_interna:^12} | {'10°C':^13} | {temperatura_interm:^6} |")
print(f"| Temperatura externa da nave       | {temperatura_externa:^12} | {'-10°C':^13} | {temperatura_externam:^6} |")
print(f"| Energia total da nave             | {energia:^12} | {'60%':^13} | {energiam:^6} |")
print(f"| Pressão do tanque da nave         | {pressao_tanque:^12} | {'40':^13} | {pressao_tanquem:^6} |")
print(f"| Integridade estrutural da nave    | {integridade_estrutural:^12} | {'1':^13} | {integridade_estruturalm:^6} |")
print(f"| Módulos críticos da nave          | {modulos_criticos:^12} | {'1':^13} | {modulos_criticosm:^6} |")

print("\n---------------------------------------------------------------------\n")



#logica Booleana onde define se os status do foguete estao todos aptos para ser lançado!
#caso um dos elementos esteja a baixo do necessario, o lançamento não vai acontecer


if (18 <= temperatura_interna <= 30 and
    -10 <= temperatura_externa <= 35 and
    60 <= energia <= 100 and
    40 <= pressao_tanque <=60 and
    integridade_estrutural <= 1 and
    modulos_criticos <= 1):
    print("""    Integridade estrutural do foguete = OK     ⠀                          ⣀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀    Modulo Critico do foguete = OK                                       ⢸⣿⣿⣶⣦⣄⠀⢀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀    Temperatura interna = OK                                            ⢈⣿⣿⣿⣿⣿⣿⣾⡄⠀⠀⠀⠀⣼⣿⣦⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀   Temperatura externa = OK                                             ⠙⢿⣿⣿⡟⠛⠛⠿⡄⠀⠀⢰⣿⣿⣿⣿⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀   Pressão do tanque = OK                                                   ⠙⢿⣧⠀⠀⠀⠀⠀⣠⣿⣿⣿⣿⣿⣿⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀Energia = OK                                                             ⠉⠂⠀⢀⣴⣿⣿⣌⠛⠿⣿⣿⣿⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀                                                                             ⢀⣠⣼⠻⣿⣿⣿⣷⣤⡈⠻⡟⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀   --------------------------------------------                           ⢠⣴⣶⣿⣿⣿⣿⣦⡘⢿⣿⣿⣿⣿⣦⣄⢸⣦⣄⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀ |  O FOGUETE ESTA PRONTO PARA DECOLAGEM!  |                               ⠙⢿⣿⣿⣿⣿⣿⣿⣄⠙⣿⣿⣿⣿⣿⣿⠿⠛⠂⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀ --------------------------------------------                               ⠀⠙⠿⠿⠿⠿⠿⠛⠓⠈⠻⣿⡿⠋⠀⢴⠆⠉⠉⣀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀                                                                            ⠀⠀⠈⠻⣿⡿⠁⢼⠇⠀⠰⡷⠄⠉⢁⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀                                                                               ⠈⠃⢰⡄⠀⠿⠂⣠⣶⣿⣿⣇⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀                                                                                  ⠈⠀⠲⠀⢰⣿⣿⣿⣿⣿⣆⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀                                                                                  ⠀⠉⠛⠿⣿⣿⣿⣿⡀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀                                                                                  ⠀⠀⠀⠈⠉⠛⠃""")




else: #OK significa pronto N/G significa No Good.
    print("""
    Integridade estrutural do foguete = N/G
    Modulo Critico do foguete = N/G
    Temperatura interna = N/G
    Temperatura externa = N/G
    Pressão do tanque =N/G
    Energia = N/G
    ------------------------------------------------
    |  O FOGUETE NÃO ESTA APTO PARA DECOLAR!  |
    ------------------------------------------------
    """)







