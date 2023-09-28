# LB 324

## Aufgabe 2
Erklären Sie hier, wie man `pre-commit` installiert.
1. Installieren von `pre-commit`
    ```pip
    pip install pre-commit
    ```

2. Im Anschluss erstellt man seinen pre-commit hook. Das sind meine.
   ```yaml
   repos: local
    hooks:
      - id: pytest-check
        stages: [commit]
        types: [python]
        name: pytest-check
        entry: python -m pytest
        language: system
        pass_filenames: false
        always_run: true
   ```

3. Zum Schluss gibt man noch diesen Befehl in seinem Terminal ein.
   ```pre-commit install --hook-type pre-commit --hook-type pre-push```
  Jetzt kann man nur noch Commits tätigen, wenn alle Test erfolgreich sind.
## Aufgabe 4
Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.

In Azure in seiner Web-App muss man unter Konfiguration auf "Neue Anwendungseinstellung" klicken und dort seine Werte für die Daten im `.env` File einfügen. 
In meinem Fall waren es diese Werte.
![image](https://github.com/SpogotenauPOGGERS/VontobelJanLB-324/assets/89130699/4a229448-fc15-4641-95d7-63ff58e42eca)

[Gehostete Seite](https://tagebbbuch.azurewebsites.net/)

