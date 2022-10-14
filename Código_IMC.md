# Python-Iniciante
Código fonte



from decimal import Decimal
from termcolor import colored

print ('Calcule seu IMC!')

nome_usuario= input('Digite seu nome: ')
peso_usuario= input ('Digite seu peso: ')
altura_usuario= input('Digite seu Altura:')

altura_usuario = float(Decimal(altura_usuario))
peso_usuario= float(Decimal(peso_usuario))


alt_multiplicada= altura_usuario * altura_usuario

imc_usuario = peso_usuario / alt_multiplicada
imc_usuario= float (imc_usuario)

print('')


print('')

if imc_usuario <= 18.5:
    print (f'Seu IMC é {imc_usuario: .2f} e você está abaixo do peso.')
elif imc_usuario >=18.6 and imc_usuario<= 24.9 :
    print (f'Seu IMC é {imc_usuario: .2f} e você está no PESO IDEAL, PARABÉNS!')
elif imc_usuario >=25 and imc_usuario<= 29.9 :
    print (f'Seu IMC é {imc_usuario: .2f} e você está na Préiobesidade, TOME CUIDADO!')
elif imc_usuario >=30 and imc_usuario<= 34.9 :
    print (f'Seu IMC é {imc_usuario: .2f} e você está na Obesidade Grau 1, Consulte um especialista!')
else:
    print (f'Seu IMC foi {imc_usuario: .2f}, você está no Grau 2 de Obesidade, Procure um Médico URGENTE.')

print('')
print('')

print(colored('Menor que 18.5 - Abaixo do peso', 'red', attrs=['bold']))
print(colored('Entre 18.5 e 24.9 - Peso norma', 'green', attrs=['bold']))
print(colored('Entre 25.0 e 29.9 - Pré-obesidade', 'green', attrs=['bold']))
print(colored('Entre 30.0 e 34.9 - Obesidade Grau 1', 'red', attrs=['bold']))
print(colored('Entre 35.0 e 39.9 - Obesidade Grau 2', 'red', attrs=['bold']))

        
