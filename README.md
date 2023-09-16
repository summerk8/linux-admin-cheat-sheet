Linux Admin Cheat Sheet
=================


## Table Of Contents

- [Linux Admin Cheat Sheet](#linux-admin-cheat-sheet)
  - [Table Of Contents](#table-of-contents)
  - [Monitoring](#Monitoring)


## Monitoring
---

###  Realtime counting unique IP addresses in access log
---

* while true; do clear; tail -100 /var/log/httpd/access_log | awk '{print $2}'  | uniq -c | sort -nr| head -10; sleep 2;  done
  - The __uniq command in Linux is used for removing duplicate lines from a file. Use option '-c' to get the count of repeated lines.

###  Realtime counting number of files currently open by Java application
---

* watch 'cd /proc/$(pidof java)/fd && ls -l | wc -l'
  
