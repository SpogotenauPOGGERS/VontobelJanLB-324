# LB 324

## Aufgabe 2
Erklären Sie hier, wie man `pre-commit` installiert.
1. Installieren von `pre-commit`
  ```pip
  pip install pre-commit
  ```

3. Im Anschluss erstellt man seinen pre-commit hook. Das sind meine.
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

4. Zum Schluss gibt man noch diesen Befehl in seinem Terminal ein.
   ```pre-commit install --hook-type pre-commit --hook-type pre-push```
  Jetzt kann man nur noch Commits tätigen, wenn alle Test erfolgreich sind.
## Aufgabe 4
Erklären Sie hier, wie Sie das Passwort aus Ihrer lokalen `.env` auf Azure übertragen.
