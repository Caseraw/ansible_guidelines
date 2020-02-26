# Tasks in general

Tasks are actions performed by Ansible to do *"something"*.  
Make sure your tasks consist of the following:

1. Give a **name** to all tasks that show what the task is doing and what it is for.
2. Make use of Ansible modules when applicable, if not use other means and methods but try to keep it simple.
3. Use **handlers** as post actions to a regular task which will run at the end of the job.
4. Use **register** to record the output of tasks for additional work later on in the job.
5. Do not put all the module parameters in one line. Though it is possible, it is not Nice!
6. Try not to over complicate things, ... I know ... sometimes you have to ... just try to avoid it if possible.
