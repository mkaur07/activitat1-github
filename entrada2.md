# Desenvolupament del programa de càlcul de DNI

En aquesta segona entrada explico com he creat el programa per calcular la lletra del DNI fent servir Python.

### El Codi Font
He escrit el següent codi a Visual Studio Code.He hagut d'instal·lar l'extensió de Python per poder-lo executar correctament:

```python
# Programa creat per manheer
print("--- Calculadora de lletra de DNI ---")
numero = input("Escriu el teu número de DNI (8 xifres): ")
lletres = "TRWAGMYFPDXBNJZSQVHLCKE"

if numero.isdigit() and len(numero) == 8:
    resta = int(numero) % 23
    lletra_final = lletres[resta]
    print(f"La lletra que et correspon al DNI {numero} és: {lletra_final}")
else:
    print("Error: Has d'introduir exactament 8 números.")