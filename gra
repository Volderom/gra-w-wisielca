import random

# lista słów do odgadnięcia
slowo_lista = ["kot", "pies", "samochód", "telewizor", "laptop", "komputer"]

# losowanie słowa
slowo = random.choice(slowo_lista)

# zmienna przechowująca zgadnięte litery
zgadniete_litery = []

# liczba prób
liczba_prob = 10

# pętla główna gry
while liczba_prob > 0:
    # wyświetlenie zgadniętych liter i ukrytych znaków
    for litera in slowo:
        if litera in zgadniete_litery:
            print(litera, end=" ")
        else:
            print("_", end=" ")
    print()

    # pobranie litery od gracza
    litera_zgadywana = input("Podaj literę: ")

    # sprawdzenie, czy litera jest w słowie
    if litera_zgadywana in slowo:
        zgadniete_litery.append(litera_zgadywana)
        print("Brawo, zgadłeś literę!")
    else:
        liczba_prob -= 1
        print("Niestety, ta litera nie występuje w słowie.")
        print(f"Pozostało Ci {liczba_prob} prób.")

    # sprawdzenie, czy gracz odgadł słowo
    if set(slowo) <= set(zgadniete_litery):
        print(f"Brawo, odgadłeś słowo! To było: {slowo}")
        break

# jeśli gracz nie odgadł słowa w czasie, to przegrał
if liczba_prob == 0:
    print(f"Nie udało Ci się odgadnąć słowa. To było: {slowo}")
