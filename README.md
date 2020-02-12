# osTicket-playbook

Deploy osTicket using ansible playbook

***Currently it only supports osTicket deployment to debian derived operating systems.***

**Requirements:**

- python 2 or newer version
- python-pip

**Setup your environment:**

Install requirements for this project

```bash
$ pip install -r requirements.txt
```

**Deploy osTicket:**

1) Update `vars.yml` and `hosts`file, use the settings you want.

2) Deploy osTicket

```bash
$ ansible-playbook -i hosts main.yml
```

Optional:

If you want to use https on osTicket, you can generate an SSL certificate via lets encrypt. Just run 1 more playbook.

```bash
$ ansible-playbook -i hosts lets-encrypt.yml
```

