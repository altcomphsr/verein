Die Mitglieder-Datenbank ist mit einem symmetrischen GPG-Passwort verschlüsselt. Das Passwort ist in der ```pass```-Datenbank abgelegt.

## Benutzung:

```bash
# Entschlüsseln
gpg2 --output memberdb.sqlite --decrypt memberdb.sqlite.gpg

# Bearbeiten
sqlite memberdb.sqlite

# Verschlüsseln
gpg2 --symmetric memberdb.sqlite
```

## Aktionen

### Neues Mitglied hinzufügen
```sql
INSERT INTO members (first_name,last_name,email,gender,github,active) 
  VALUES ("Vorname", "Nachname", "die@mail", "m/w", "GITHUBUSER", 1);
```
