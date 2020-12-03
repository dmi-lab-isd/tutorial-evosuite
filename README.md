# Tutorial: Evosuite

Documentazione: https://www.evosuite.org/documentation

Sebbene sia possibile usare EvoSuite anche da riga di comando (tramite il jar) l'utilizzo del plugin maven è più immediato.

In questo tutorial, EvoSuite verrà eseguito usando il plugin di maven.

## Step

EvoSuite genererà una classe di test per ciascuna delle classi del progetto.

La cartella dei test contiene già un esempio di test generati da EvoSuite.

- `mvn compile` (necessario compilare le classi per poter generare i test)
- `mvn evosuite:generate` (genera i test in *.evosuite*, richiede 4 minuti circa)
- `mvn evosuite:info` (opzionale, per info sui test generati)
- `mvn evosuite:export` (copia i test da *.evosuite* a *src/test/java*)
- `mvn evosuite:clean` (opzionale: elimina la cartella *.evosuite*)
- `mvn test` (esegue i test)
- `mvn evosuite:coverage` (opzionale, per misurare la copertura dei test)

## Altri comandi

- `mvn evosuite:help` (per l'help dei goal disponibili nel plugin)
- `mvn evosuite:help -Ddetail=true -Dgoal=generate` (per i dettagli di un goal)
- `rm src/test/java/*ESTest*.java` (per rimuovere i test esportati)
