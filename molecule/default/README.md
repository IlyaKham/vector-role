PLAY [Verify] ******************************************************************

TASK [Gathering Facts] *********************************************************
ok: [instance-ubuntu]
ok: [instance-oraclelinux]

TASK [Check if vector binary exists] *******************************************
ok: [instance-ubuntu]
ok: [instance-oraclelinux]

TASK [Assert vector binary exists and is executable] ***************************
ok: [instance-oraclelinux] => {
    "changed": false,
    "msg": "All assertions passed"
}
ok: [instance-ubuntu] => {
    "changed": false,
    "msg": "All assertions passed"
}

TASK [Check if vector config directory exists] *********************************
ok: [instance-ubuntu]
ok: [instance-oraclelinux]

TASK [Assert vector config directory exists] ***********************************
ok: [instance-oraclelinux] => {
    "changed": false,
    "msg": "All assertions passed"
}
ok: [instance-ubuntu] => {
    "changed": false,
    "msg": "All assertions passed"
}

TASK [Check if vector config file exists] **************************************
ok: [instance-ubuntu]
ok: [instance-oraclelinux]

TASK [Assert vector config file exists] ****************************************
ok: [instance-oraclelinux] => {
    "changed": false,
    "msg": "All assertions passed"
}
ok: [instance-ubuntu] => {
    "changed": false,
    "msg": "All assertions passed"
}

TASK [Validate vector configuration file] **************************************
ok: [instance-ubuntu]
ok: [instance-oraclelinux]

TASK [Assert configuration is valid] *******************************************
ok: [instance-oraclelinux] => {
    "changed": false,
    "msg": "All assertions passed"
}
ok: [instance-ubuntu] => {
    "changed": false,
    "msg": "All assertions passed"
}

PLAY RECAP *********************************************************************
instance-oraclelinux       : ok=9    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
instance-ubuntu            : ok=9    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

INFO     default ➜ verify: Executed: Successful
INFO     default ➜ cleanup: Executing
WARNING  default ➜ cleanup: Executed: Missing playbook (Remove from test_sequence to suppress)
INFO     default ➜ destroy: Executing

PLAY [Destroy] *****************************************************************

TASK [Set async_dir for HOME env] **********************************************
ok: [localhost]

TASK [Destroy molecule instance(s)] ********************************************
changed: [localhost] => (item=instance-ubuntu)
changed: [localhost] => (item=instance-oraclelinux)

TASK [Wait for instance(s) deletion to complete] *******************************
FAILED - RETRYING: [localhost]: Wait for instance(s) deletion to complete (300 retries left).
changed: [localhost] => (item=instance-ubuntu)
changed: [localhost] => (item=instance-oraclelinux)

TASK [Delete docker networks(s)] ***********************************************
skipping: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=3    changed=2    unreachable=0    failed=0    skipped=1    rescued=0    ignored=0

INFO     default ➜ destroy: Executed: Successful
INFO     default ➜ scenario: Pruning extra files from scenario ephemeral directory
WARNING  Molecule executed 1 scenario (1 missing files)