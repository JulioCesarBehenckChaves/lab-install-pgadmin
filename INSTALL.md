
### Steps to install the pgAdmin

```bash
sudo apt update
sudo apt upgrade -y
sudo apt autoremove -y
```

```bash
sudo apt install curl -y
```

```bash
sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
```

```bash
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && sudo apt update'
```

```bash
sudo apt install pgadmin4 -y
sudo apt install pgadmin4-desktop -y
sudo apt install pgadmin4-web -y
```

```bash
sudo /usr/pgadmin4/bin/setup-web.sh
```

Enter an e-mail and password to be used to log-in the pgadmin portal.
When asked, choose "y" and "y".

Create a new superuser in you postgres.
Enter in your psql line command prompt and type:

```sql
create user admin with superuser password 'SUA_SENHA';
```

Open up the URL below in brave-browser:

```
brave-browser
```

```
http://127.0.0.1/pgadmin4
```

Enter with the e-mail and the user you just specified.
Inside the portal, use a quick link to add a new server.
Use the connection info from the superuser you just created in you SGBD.



Ref: https://itslinuxfoss.com/install-pgadmin-ubuntu-22-04/