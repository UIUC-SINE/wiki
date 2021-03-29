# Running tasks while disconnected

Use `screen` to keep long-running tasks running after you disconnect from SSH.

## Quickstart

    # start a new screen session
    screen -S mytask
    # launch script
    python longscript.py
    
Either close the ssh client window or detach from the screen session with `Ctrl-a d` (control-A, then d).  After reconnecting to the server later, you may reattach to the session with

    screen -x mytask

## Useful Commands

- `screen -S [session_name]` - create new screen session
- `screen -list` - list existing screen sessions
- `screen -x [session_name]` - reattach to existing screen session
- `killall screen` - kill all screen sessions

## Useful Shortcuts

- `Ctrl-a d` - detach from current screen session and leave it running
- `Ctrl-a k` - kill current screen session
