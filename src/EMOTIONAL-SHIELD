       IDENTIFICATION DIVISION.
       PROGRAM-ID. EMOTIONAL-SHIELD.

       ENVIRONMENT DIVISION.
       DATA DIVISION.

       WORKING-STORAGE SECTION.
       01 INPUT-EVENT            PIC X(200).
       01 PROCESSED-EVENT        PIC X(200).
       01 EMOTIONAL-LOAD         PIC 9(03) VALUE 0.
       01 THRESHOLD              PIC 9(03) VALUE 50.
       01 RESPONSE               PIC X(200).

       01 NEGATIVE-WORDS.
          05 WORD PIC X(20) OCCURS 5 TIMES
             VALUE "CRITICA",
                   "ATAQUE",
                   "CULPA",
                   "DESVALORIZACAO",
                   "PROJECAO".

       01 POSITIVE-RESPONSE      PIC X(200)
          VALUE "MANTER LIMITES ESTAVEIS E REFORCAR AUTO-RESPEITO.".

       01 NEUTRAL-RESPONSE       PIC X(200)
          VALUE "REGISTAR EVENTO SEM INTERNALIZAR.".

       01 BLOCK-RESPONSE PIC X(200)
          VALUE "EVENTO BLOQUEADO — NAO ABSORVER CARGA EMOCIONAL.".

       PROCEDURE DIVISION.
       MAIN-PROCESS.

           DISPLAY ">> Emotional Shield v1.0 Activated".
           
           ACCEPT INPUT-EVENT FROM CONSOLE.

           PERFORM SCAN-INPUT.

           IF EMOTIONAL-LOAD > THRESHOLD
              MOVE BLOCK-RESPONSE TO RESPONSE
           ELSE
              IF EMOTIONAL-LOAD = 0
                 MOVE NEUTRAL-RESPONSE TO RESPONSE
              ELSE
                 MOVE POSITIVE-RESPONSE TO RESPONSE
              END-IF
           END-IF.

           DISPLAY ">> OUTPUT: " RESPONSE.

           STOP RUN.

       SCAN-INPUT.
           PERFORM VARYING IDX FROM 1 BY 1 UNTIL IDX > 5
              IF INPUT-EVENT CONTAINS WORD(IDX)
                 ADD 20 TO EMOTIONAL-LOAD
              END-IF
           END-PERFORM.
