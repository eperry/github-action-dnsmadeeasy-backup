# DNS Made Easy - DNS Backup

## To Activate
* Fork this repo to your own copy
* Edit the inventory/hosts file to replace the domains with your specific domain
* Copy the the file to the workflows directory, commit and push it
``` cp github-action-backup.yml .github/workflows/```
  ***You might want to edit the file to change when the crontab kicks off.
* git add .github/workflows
* git commit -am 'Activate'
* git push the code update
* go to the action tab on GIT and you should see it 
* You need to create some "Secrets" so go to github and go to the settings tab on the project.
```
DNSMADEEASY_APIKEY = The api key generated @ DNS Made Easy admin account
DNSMADEEASY_SECRET = The Secret for the Generated API Key
SLACK_WEBHOOKS     = The slakc WEBHOOK to post to. If you don't want to use slack, make sure you remove the Notif slack sections
```

```
.github/workflows/backup_dnsme.yml
```
It utilizes the Repository-> Settings-> Secrets to pass in the DNSME API Tokens

