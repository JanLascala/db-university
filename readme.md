sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

## table departments

literature:
biology:
art:


### courses ###
##  table literature_courses
european_literature:
asian_literature:

## biology_courses
human_biology:
flora_biology:
fauna_biology:


## art_courses
sketch_art:
painting_art:
sculpting_art:
digital_art:

### Teachers ###

## literature_teachers
id: (BIGINT)- auto-increment  NOT NULL
fullname:
telephone:
address:
email:
Specialization:

## biology_teachers
id: (BIGINT)- auto-increment  NOT NULL
fullname:
telephone:
address:
email:
Specialization:

## art_teachers
id: (BIGINT)- auto-increment  NOT NULL
fullname:
telephone:
address:
email:
Specialization:
