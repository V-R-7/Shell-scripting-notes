# tail Command

In shell scripting, the tail command is used to display the last part of a file. 
It's particularly useful for viewing the end of log files, monitoring file changes, and more. 

The basic syntax of the tail command is:
```

tail [options] [filename]

```

some common options used with the tail command:

- -n : Displays the last N lines of the file. For example, -n 10 will display the last 10 lines.
- -f : Follows the output, displaying appended data as the file grows. This is often used to monitor log files in real-time.
- -c : Displays the last N bytes of the file.
- --pid=PID: Stops the tail command when the process with the specified PID ends.

Examples:

i) To display the last 10 lines of a file named example.log,

```

tail -n 10 example.log

```

ii) To monitor a log file continuously,

```

tail -f /var/log/syslog

```

iii) To display the last 100 bytes of a file named data.txt,

```

tail -c 100 data.txt

```

iv) To monitor a log file until the background process completes,

```
#!/bin/bash

# Define a background process
background_process() {
    echo "Background process started..."
    for i in {1..5}; do
        echo "Processing iteration $i"
        sleep 1
    done
    echo "Background process completed."
}

# Start the background process
background_process > background.log &

# Capture the PID of the background process
BG_PROCESS_PID=$!

echo "Background process started with PID: $BG_PROCESS_PID"

# Monitor the log file until the background process ends
tail --pid=$BG_PROCESS_PID -f background.log

echo "Tail command exited, background process may have completed."

```
This script demonstrates how you can monitor the output of a background process using tail --pid until the background process finishes.

Summarize Entirely, In a shell script, you can use the tail command to extract relevant information from log files, track changes,

or perform other tasks where accessing the end of a file is necessary.
