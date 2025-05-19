Richieste di importazione
Sistema d'importazione

#Emoji
banner = "🔍"
successo = "✅"
fail = "❌"
url_emoji = "🌐"

def find_subdomains (dominio, wordlist_path):
    print (f"{banner} Avvio scansione sottodomini per: {dominio}\n")

    Prova:
        con open (wordlist_path, "r") come file:
            sottodomini = file.read ().splitlines ()
    eccetto FileNotFoundError:
        print (f"{fail} Wordlist non trovata: {wordlist_path}")
            sys.exit (1)

    per i sottodomini:
        url = f"http://{sub}.{dominio}"
        Prova:
            risposta = request.get (url, timeout=2)
            print (f"{successo} Trovato: {url_emoji} {url}")
        ad eccezione delle richieste. Errore di connessione:
            pass # Dominio non esiste, silenzio

 se ____ == "Nome____principale__":
    se len (sys.argv)!= 3:
        print (f"{fail} Uso corretto: python subdomain_finder.py < Dominio><wordlist.txt""
        sys.exit (1)

    target_domain = sys.argv[1]
    wordlist = sys.argv[2]
    find_subdomini)
