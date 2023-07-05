
nome = input('quale è il tuo nome, umano ? ')
residenza = input('e da dove vieni ?  ')

identita = 'Salve ' + nome + ' ' + 'da ' + residenza + ' io sono Grabor e sei mal capitato nella mia tana disturbando il mio sonno e per uscire da    qui dovrai rispondere ad alcuni indovinelli e salvare la tua vita '
print(identita)

domande = [
    {
        "domanda": "prima indovinello, che spero che la tua piccola mente ci riesca, cosa è la cosa che quando lo nomini non ce più ?",
        "risposta_corretta": "Il silenzio"
    },
    {
        "domanda": "Trenta bianchi destrier su un colle rosso battono e mordono, ma nessun si è mosso.",
        "risposta_corretta": "i denti"
    },
    {
        "domanda": "Parla senza bocca, ti batte e non ti tocca, corre senza piedi, passa e non lo vedi. Cos'é?",
        "risposta_corretta": "il vento"
    },
    {
        "domanda": "Sono tutto denti ma non mangio mai nulla. Cosa sono?",
        "risposta_corretta": "il pettine"
    },
     {
        "domanda": "Senza coperchio, chiave, né cerniera uno scrigno cela una dorata sfera",
        "risposta_corretta": "l'uovo"
    },
     {
        "domanda": "Ho i denti e proteggo casa, ma non mordo né abbaio...",
        "risposta_corretta": "la chiave"
    }, {
        "domanda": " Non mi puoi annegare in acqua né bruciare nel fuoco. Cosa sono?",
        "risposta_corretta": "il ghiaccio"
    }
    
]

tentativi_riusciti = 0
tentativi_falliti = 0

for domanda in domande:
    print(domanda["domanda"])
    risposta_giocatore = input("Allora? qual'é la tua risposta? ")

    if risposta_giocatore.lower() == domanda["risposta_corretta"].lower():
        print("molto bravo, un'altro\n")
        tentativi_riusciti += 1
    else:
        print("ah ah è inesatto\n")
        tentativi_falliti += 1

    if tentativi_falliti == 2:
        print("Hai perso, mi sono stancato e perciò ti mangio")
        break
    if tentativi_riusciti ==5:
        print('hai vinto la tua vita')
        break
