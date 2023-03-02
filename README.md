# About my Homelab Setup



# Bring up all services

```docker-compose up -d```



# Passbolt First Run

Gotta generate a first user, and then you can create more users from the web interface.

```
docker-compose exec passbolt su -m -c "/usr/share/php/passbolt/bin/cake \
						passbolt register_user \
						-u <your@email.com> \
						-f <yourname> \
						-l <surname> \
						-r admin" -s /bin/sh www-data
```

# Yubikey: https://upgrade.yubico.com/getapikey/


go-passbolt-cli configure --serverAddress https://passbolt.devopsbrad.com --userPassword $PASSBOLT_PASSWORD --userPrivateKeyFile 'passbolt-recovery.key' --mfaDelay 60m --mfaMode noninteractive-totp


go-passbolt-cli create resource --name "Test Resource" --password "Strong Password"
go-passbolt-cli list resource
go-passbolt-cli get resource --id <ResourceID>


# Restoring from a Snapshot:
```
sudo cp -rp /volume2/share2-SSD/#snapshot/GMT-08-2023.03.01-07.00.01/homelab/docker/volumes/* .
```