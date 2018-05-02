# Apply
A bash script for running a command in every subdirectory of a directory. This script is designed for projects involving several directories that contain similar files and all need the same script applied to them. Supports both forground and background processing.

Usage: apply <number of workers> <directory> <worker> [arguments...]
Calls <worker> with [arguments...] in every subdirectory in <directory>.

Also, in [arguments...], all instances of _id_, _exe_, and _path_ are replaced with the id of the task, the path the apply was called from, and the path the task is being called in before being passed on to the worker.
  
<number of workers> indicates the number of concurent processes used to call <worker>. If <number of processes> is 1, <worker> will be called in the foreground and in order for each subdirectory.
