# Consegna

# Tabella `Dipartimenti`
-id (int, PK, auto increment)
-nome (varchar(150))
-sede (varchar(150))
-telefono (varchar(20))
-email (varchar(150))
-città (varchar(150))
-cap (varchar(5))
-Piva (varchar(16))


# Tabella `Corsi_di_Laurea`
-id (int, PK, auto increment)
-nome (varchar(150))
-id_dipartimento (int, FK)
-durata (int)
-tipologia (varchar(150))
-descrizione (text)
-requisiti (text)
-sezione (varchar(150))

# Tabella `Corsi`
-id (int, PK, auto increment)
-nome (varchar(150))
-id_corso (int, FK)
-descrizione (text)
-crediti (int)
-semestre (varchar(20))
-anno (date)



# Tabella `Insegnanti`
-id (int, PK, auto increment)
-nome (varchar(150))
-cognome (varchar(150))
-email (varchar(150))
-telefono (varchar(20))
-codice_fiscale (varchar(16))
-id_dipartimento (int, FK)
-materia_corso (varchar(150))



# Tabella `Studenti`
-id (int, PK, auto increment)
-nome (varchar(150))
-cognome (varchar(150))
-email (varchar(150))
-telefono (varchar(20))
-codice_fiscale (varchar(16))
-matricola (varchar(20))
-id_corso (int, FK)
-data_iscrizione (date)



# Tabella `Esami`
-id (int, PK, auto increment)
-id_corso (int, FK)
-data (date)
-orario (time)
-aula (varchar(150))
-id_insegnante (int, FK)
-id_studente (int, FK)
-voto (int)
-esito (varchar(20))


# Tabella `appello_studente`
-id (int, PK, auto increment)
-id_studente (int, FK)
-id_esame (int, FK)
-data_iscrizione (date)







