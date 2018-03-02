
User `jenkins` is gone after OS updated.

1, Create jenkins user in `System Preferences/Users & Groups`
  Account name: jenkins
  Full name: Jenkins
  
2, Update permission for jenkins folders
`sudo chown -R jenkins /Users/Shared/Jenkins`
`sudo chown jenkins /var/log/jenkins`

3, Restart jenkins server
`sudo launchctl unload /Library/LaunchDaemons/org.jenkins-ci.plist`
`sudo launchctl load /Library/LaunchDaemons/org.jenkins-ci.plist`
