# Role Name

Installs a luigi central scheduler.

## Dependencies

* sqlite

## Role Variables


    # for starting the daemon
    luigi_config_path: /etc/luigi/client.cfg
    luigi_log_file_path: /var/log/luigid
    luigi_history_db: sqlite:///usr/local/var/luigi-task-hist.db
    luigi_pid_file: /usr/local/var/luigi.pid
    luigi_record_task_history: True
    luigi_state_file: /usr/local/var/luigi-state.pickle
    # enabled task history by default
    luigi_record_task_history: True
    luigi_history_db: sqlite:///usr/local/var/luigi-task-hist.db

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: riethmayer.luigi-server }

## License

MIT

## Author Information

Jan Riethmayer, @riethmayer
