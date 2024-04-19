## ps

#### List currently running processes:

`ps -ef`

`ps -aux`

#### List the processes based on user(s):

`ps -f -u jay`

`ps -f -u jay,root`

#### List processes based on PID:

`ps -f -p <PID1>,<PID2>,<PID3>`

#### List processes based on PPID:

`ps -f --ppid <PID>`

#### List processes in a hierarchy:

`ps -e -o pid,args --forest`

#### List elapsed wall time for processes:

`ps -p <PID1>,<PID2>,<PID3> -o pid,etime=`

#### List all threads for a particular process:

`ps -C java -L -o pid,tid,pcpu,state,nlwp,args`

#### List proesses but sort by memory usage (useful in finding memory leaks):

`ps aux --sort pmem`

#### Show top five processes consuming the most CPU:

`ps aux --sort=-pcpu | head -5`

#### Show the top five processes consuming the most CPU, with condensed columns:

`ps -e -o pid,uname,pcpu,pmem,comm --sort=-pcpu |head -n 5`

#### Show top five processes consuming the most memory:

`ps aux --sort=-pmem | head -5`

#### Show top five processes using memory, with condensed columns:

`ps -e -o pid,uname,pcpu,pmem,comm --sort=-pmem |head -n 5`

#### Display child processes of a parent process

`ps -o pid,uname,comm -C apache2`

#### Real time output:

`watch -n 1 'ps -e -o pid,uname,cmd,pmem,pcpu --sort=-pmem,-pcpu | head -15'`
