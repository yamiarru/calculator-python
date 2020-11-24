# calculator-python
SUMA
import sys
numeros = []
continueNumber = True
result = 0


def sumarNumero(list):
    global result
    for n in list:
        result += n

    return 'El resultado es {}'.format(result)



if __name__ == '__main__':
    while continueNumber == True:
        numero = int(input('Numero: '))
        numeros.append(numero)
        continueN = int(input('Desea añadir otro numero: 1=si, 0=no: '))
        if continueN == 1:
            continueNumber = True
        else:
            continueNumber = False
            print(sumarNumero(numeros))
            print('='*50)
            continueIsTrue = int(input('Desea ejecutar el programa nuevamente: 1=si, 0=no: '))
            if continueIsTrue == 1:
                numeros = []
                result = 0
                continueNumber = True

            else:
                sys.exit()
