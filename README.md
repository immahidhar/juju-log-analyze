Canonical Take Home Exercise

Program: juju-log-analyze.py
This program will read a juju log file looking for log messages with severities of “INFO”, “DEBUG”, “WARNING”, “ERROR”. 
If a charm name is included in the parameters then it will ignore all the other charms’ log outputs.

Note:
    The program "juju-log-analyze.py" has been written in Python version 3.9.6. 
    So, make sure to install python version 3.9 or above before running the program.



How to run the program?

To run the program, extract the files and execute the following from the folder where "juju-log-analyze.py" is present:

    python3 juju-log-analyze.py juju_log_file [target_charm]

If the output is too long, redirect it to a file using '>'.

Example test run has been run as follows:

    python3 juju-log-analyze.py juju-debug.log > output.txt

Sample output: see attached [output.txt](output.txt)

Example test run with a charm parameter is as follows:

    python3 juju-log-analyze.py juju-debug.log nova-compute > out.txt

Sample output: see attached [out.txt](out.txt)
