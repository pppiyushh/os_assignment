# os_assignment

### Starve-free REader-Writer Problme

In the earlier first solution of Reader-Writer problem, Reader was guven priority over Writer
which resulted in the starvation of Writers. So, In the second dolution of this problem gave Writers priority over readers
which resulted into starvation of Readers.

So. the aimm of our current algo. is to provide a starve-free solution for both readers and writers.

Solution idea:

Considering a writer process first, if the no of active readers and waiting users im the critical section is 0 ,
then it will instantly direct the writer to the critical section, otherwise the writer will have to wait until 
the reader finishes its work.

Psuedo code:

Reader Processes:

if(active and waiting writers are zero) signal and enter the process else wait for signal

//Read

if( is the last reader) signal the waiting writers

The writer process will be analogous to the reader process.

The above file containing code is deadlock-free and starve-free.
