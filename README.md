Dokku provisioning plugin
-------------------------

Project: https://github.com/progrium/dokku

Installation
------------
```
git clone https://github.com/Kloadut/dokku-provisioning-plugin /var/lib/dokku/plugins/provisioning
```

Usage
-----

You hust have to add a bash script named `.provisioning` at the root of your app package. It will be executed on pre-release.

```
cd /path/to/my/app
echo "chown -R www-data: /app" > .provisioning
git add .provisioning
git commit -m "Add provisioning script"
git push dokku master
```
