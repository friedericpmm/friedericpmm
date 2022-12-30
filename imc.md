print("""
=======================
Índice de masa corporal
=======================""")

peso = int(input("Por favor indique su peso en kilogramos (Kg): "))
estatura = int(input("Señale tambien por favor cual es su estatura en metros (mts): "))

print(f"Tu índice de masa corporal es de {peso / (estatura*2)}")
