Bootstrap: docker
From: mariadb:10.5.3-bionic

%post
# replace `your-name` with your username, run `whoami` to see your username
YOUR_USERNAME="vle@its.aau.dk"

sed -ie "s/^#user.*/user = ${YOUR_USERNAME}/" /etc/mysql/my.cnf
chmod 1777 /run/mysqld

%runscript
exec "mysqld" "$@"

%startscript
  docker-entrypoint.sh mysqld
