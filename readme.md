sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

## table departments

literature: NOT NULL
biology:NOT NULL
art:NOT NULL


### courses ###
##  table literature_courses
european_literature: NOT NULL
asian_literature:NOT NULL

## biology_courses
human_biology: NOT NULL
flora_biology: NOT NULL
fauna_biology:NOT NULL


## art_courses
sketch_art: NOT NULL
painting_art: NOT NULL
sculpting_art: NOT NULL
digital_art: NOT NULL

### Teachers ###

## literature_teachers
id: (BIGINT)- auto-increment  NOT NULL
fullname: varchar(30)NOT NULL
telephone: smallinit NOT NULL
address:  varchar(50)NOT NULL
email: varchar(30) NOT NULL
Specialization: varchar(50) NOT NULL

## biology_teachers
iid: (BIGINT)- auto-increment  NOT NULL
fullname: varchar(30)NOT NULL
telephone: smallinit NOT NULL
address:  varchar(50)NOT NULL
email: varchar(30) NOT NULL
Specialization: varchar(50) NOT NULL

## art_teachers
id: (BIGINT)- auto-increment  NOT NULL
fullname: varchar(30)NOT NULL
telephone: smallinit NOT NULL
address:  varchar(50)NOT NULL
email: varchar(30) NOT NULL
Specialization: varchar(50) NOT NULL

## exam_appeals
id: (BIGINT)- auto-increment  NOT NULL
student_id:NOT NULL
student_vote: NOT NULL
teacher_id:NOT NULL
course:

## students
id: (BIGINT)- auto-increment  NOT NULL
fullname: varchar(30) NOT NULL
telephone: smallinit NOT NULL
address:  varchar(50)NOT NULL
email: varchar(30) NOT NULL
department: varchar (20)NOT NULL
course:varchar (20) NOT NULL
vote:tinyinit NOT NULL

