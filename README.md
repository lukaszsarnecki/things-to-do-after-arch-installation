# Things to do after arch installation

Wiele dystrybucji Linuksa ma domyślnie włączoną funkcję autouzupełniania w Bashu. Jeśli jednak z jakiegoś powodu autouzupełnianie nie działa, możesz je włączyć ręcznie.

Upewnij się, że masz zainstalowane narzędzie bash-completion:

bash-completion to pakiet, który rozszerza funkcje autouzupełniania w Bashu. Jest on dostępny w większości dystrybucji Linuksa.

sudo pacman -S bash-completion

Aktywacja bash-completion:

W większości dystrybucji Bash automatycznie ładuje bash-completion. Jeśli jednak musisz to zrobić ręcznie, dodaj poniższy kod do pliku ~/.bashrc:

bash
Skopiuj kod
# Włącz autouzupełnianie w Bashu
if ! shopt -oq posix; then
    # Włącz bash-completion
    source /etc/bash_completion
fi

source ~/.bashrc
