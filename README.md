Linux Admin Cheat Sheet
=================


## Table Of Contents

- [Linux Admin Cheat Sheet](#linux-admin-cheat-sheet)
  - [Table Of Contents](#table-of-contents)
  - [Realtime monitoring](#Realtime_monitoring)


# Realtime monitoring
---

##  Count unique IP adresses with Apache
---

* while true; do clear; tail -100 /var/log/httpd/access_log | awk '{print $2}'  | uniq -c | sort -nr| head -10; sleep 2;  done
  - The uniq command in Linux and Unix is used for removing duplicate lines from a file. Use option '-c' to get the count of repeated lines.
 
