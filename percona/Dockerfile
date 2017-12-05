FROM percona:5.7

# Dirty hack to make docker-compose able to rebuild image
# Avoid permissions issue
RUN user=mysql new_uid=1000 old_uid=$(id -u $user) \
    && group=mysql new_gid=1000 old_gid=$(id -g $user) \
    && usermod -u $new_uid $user \
    && groupmod -g $new_gid $group

RUN chown -R mysql:mysql /var/lib/mysql/

COPY etc/mysql/conf.d/my.cnf* /etc/mysql/conf.d/

CMD ["mysqld"]

EXPOSE 3306