import random
saldo_bip = 0
Historial = []
def mostrar_menu():
    print("1.Recarga Bip")
    print("2.Saldo Bip")
    print("3.Validar Recarga")
    print("4.Historial Recarga")
    print("5.Salir")
while True:
        mostrar_menu()
        try:
            OpcionInicio = int(input("Bienvenido, Seleccione Una Opcion Para continuar: "))
        except ValueError:
            print("Seleccione Las Opciones Validas")
            continue
        
        if OpcionInicio == 1:
                try: 
                    print(f"Su Saldo Es de ${saldo_bip}")
                    SaldoRecargar = int(input("¿Cuanto Desea Recargar?: "))
                    if SaldoRecargar > 0:
                        Nuevo_Saldo = saldo_bip + SaldoRecargar
                        print("Su Saldo Ha Sido Agregado Con Exito!")
                        Historial.append(f"Recarga De ${Nuevo_Saldo}")
                    else:
                        print("!Ingrese Un Valor Positivo!")
                except ValueError:
                    print("Ingrese Un Saldo Agregar Valido")
        elif OpcionInicio == 2:
                print(f"Su Saldo Es ${saldo_bip}")
        elif OpcionInicio == 3:
                saldo_bip = Nuevo_Saldo
                print(f"Su Nuevo Saldo Es De ${Nuevo_Saldo}")
        elif OpcionInicio == 4:
            print("....Historial De Recarga....")
            if not Historial:
                print("!No Hay Transacciones Registradas!")
            else:
                for item in Historial:
                    print("+","$",SaldoRecargar)
        elif OpcionInicio == 5:
            print("Saliendo......")
            break
