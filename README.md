# ThySupervisor

An example implementation of a supervisor in elixir

## How to Play

- Load app `iex -S mix`
- Create supervisor `{:ok, sup_pid} = ThySupervisor.start_link([])`
- Create a child `{:ok, child_pid} = ThySupervisor.start_child(sup_pid, {ThyWorker, :start_link, []})`
- Display all proccess linked to supervisor `Process.info(sup_pid, :links)`
- Kill child process `Process.exit(child_pid, :crash)`
- Display all proccess linked to supervisor `Process.info(sup_pid, :links)`
- Display all child processes of supervisor `ThySupervisor.which_children(sup_pid)`


