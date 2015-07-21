# Role Name

Installs a [luigi](http://luigi.readthedocs.org/en/latest/) central scheduler.
For more information check out http://luigi.readthedocs.org/en/latest/

## Dependencies

* sqlite3 (apt)
* python-sqlalchemy (apt)
* luigi (pip)
* tornado (pip)

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

This will install the luigi daemon on your server and start it with an init script via `/etc/init.d/luigi-server`.

    - hosts: server
      roles:
         - { role: riethmayer.luigi-server }

## License

MIT

## Author Information

Jan Riethmayer, @riethmayer
