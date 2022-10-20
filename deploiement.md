vi /lib/systemd/system/alarmhandler.service



[Unit]
Description=KURE V2 ALARM HANDLER

[Service]
User=root
Group=root
Type=simple
Restart=always
RestartSec=5s
WorkingDirectory=/opt/kurve/kurve-cloud-alarmsrc
ExecStart=/opt/kurve/kurve-cloud-alarm/src/kurveAlarm

[Install]
WantedBy=multi-user.target

#Access
sudo chmod +x /opt/kurve.mg/cloud/server/alarm-handler/main
# Enable service 
sudo systemctl enable alarmhandler
# Service 
systemctl start|restart|stop|status alarmhandler




en tant que root

copie-na anaty fichier (kurveAlarm) ohatra ilay main
   ==>cp main kurveAlarm
   
omena droit avy eo ilay fichier
   ==>chmod +x kurveAlarm
   
avy systemctl start ou restart ... alarmhandler




mijery fichier log
=================
tail -f anaran'ilay log
less anaran'ilay log

