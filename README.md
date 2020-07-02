# Ramdisk iphone  5 ,5c A6 Linux Tools

sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 mount -o rw,union,update /
sshpass -p 'alpine' scp -P 2222 bypass_scripts/mobileactivationd_13_x/mobileactivationd root@localhost:/usr/libexec/mobileactivationd
sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 chmod 755 /usr/libexec/mobileactivationd
sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 launchctl unload /System/Library/LaunchDaemons/com.apple.mobileactivationd.plist
sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 launchctl load /System/Library/LaunchDaemons/com.apple.mobileactivationd.plist
sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 uicache -a
sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 killall backboardd
sshpass -p 'alpine' ssh -o StrictHostKeyChecking=no root@localhost -p 2222 killall SpringBoard


#Activation 13.5.1 checkra jailbreak device 
