# Completion Notification

Use UIUC's outbound email server to notify you when a long-running job is completed.

In command line:

    python myscript.py; mailme [netid]@illinois.edu
    
In Python:

``` python
from subprocess import run
run('mailme', '[netid]@illinois.edu')
```

In ipython:

    %run myscript.py; !mailme [netid]@illinois.edu
    
## Optional Subject and Body

In command line:

    python myscript.py | mailme [netid]@illinois.edu "Task is Complete"
    
In Python

``` python
from subprocess import run
message_body = "Message content"
run(['mailme', 'evanw3@illinois.edu', 'Task is Complete'], input=message_body.encode('utf8'))
```

