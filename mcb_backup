# Minecraft Buddies Back-up Script
# Commits and syncs with GitHub

# Announce to Server
screen -R minecraft -X stuff "say Backup starting. World no longer saving... $(printf '\r')"
screen -R minecraft -X stuff "save-off $(printf '\r')"
screen -R minecraft -X stuff "save-all $(printf '\r')"
sleep 3

# Commit
cd Servers/minecraft/
git commit -am "Daily Backup"

# Sync
git push origin master

# Turn Saves back on
screen -R minecraft -X stuff "save-on $(printf '\r')"
screen -R minecraft -X stuff "say Backup complete. World is saving... $(printf '\r')"
