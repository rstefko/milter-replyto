1. Build the project

```
git clone https://github.com/rstefko/milter-replyto.git
cd milter-replyto
go build
```
2. Create `milter` user

```
useradd --system --no-create-home --shell /usr/sbin/nologin milter
mkdir /var/spool/postfix/milter-replyto/
chown milter:postfix /var/spool/postfix/milter-replyto/
```

3. Copy `milter-replyto.service` to `/etc/systemd/system/milter-replyto.service`

```
systemctl enable milter-replyto
systemctl start milter-replayto
```
