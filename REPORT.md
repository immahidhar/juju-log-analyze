Juju Log Analyzer Report



Timeline:

Jul 8, 2024, 5:20 PM : 30 min : Understood message structure of the debug log attached and juju charms and units.
Jul 8, 2024, 5:50 PM : 30 min : Designed a solution approach and data structures required to store information needed.
Jul 9, 2024, 9:00 AM : 2 hrs : Created the program with designed classes, data structures and functions of analysis.
Jul 9, 2024, 10:00 AM : 1 hr : Tested the program, fixed some minor issues and refactored code for extensibility.
Jul 9, 2024, 3:00 PM : 15 min : Written a README on things to know about program and how to run it.
Jul 9, 2024, 3:15 PM : 15 min : Written a REPORT detailing the work done and assumptions.



Assumptions:

1. The program should only read and analyze log lines that start with a juju unit name i.e., "unit-{charm}-{unit_id}".
2. All other log lines will be ignored and not counted towards output.
3. To identify a charm, the charm name must match the exact regex given above.
4. If a charm parameter is passed, only the log lines of that particular charm are analyzed and the rest are ignored.
5. The log file must be of a reasonable size so that all the data will fit in memory for testing.

Below are the assumptions about the output requirements:

- The charms that produced warning messages (if not restricted to a single charm)
    
  Charms that have log lines with 'WARNING' severity must be printed.
  If a charm parameter is passed, only it will be printed if and only if it has at least one 'WARNING' severity log line.
    
- The number of each severity of message.
  
  The number of log lines of each severity of any charm will be printed.
  If a charm parameter is passed, the number of log lines of each severity of the particular charm will be printed.
  
- The number of duplicate messages (and their severity).

  If a message of same severity appears multiple times, the number of duplicates excluding the first one will be printed.
  If a charm parameter is passed, only messages of that charm will be considered and the rest will be ignored.

- The proportions of each type of log message for each charm (or just the single charm).

  The proportion (%) of each severity type messages compared to all severity type messages of all charms will be printed.
  If a charm parameter is passed, only messages of that charm will be considered and the rest will be ignored. 

- The total number of log messages per charm.

  Total number of log lines analyzed for each charm will be printed.
  If a charm parameter is passed, only total number of log lines analyzed of that particular charm will be printed.

- The total number of log messages.

  Total number of log lines analyzed of all charms will be printed.
  If a charm parameter is passed, only messages of that charm will be considered and the rest will be ignored.
