# LampPack
A bash script to automate the installation of LAMP, phpMyAdmin and Let's Encrypt

## About LampPack
LampPack is a set of some bash/shell scripts that automate several tasks together on your Ubuntu servers. If you are tired of repetitive tasks while deploying Ubuntu servers for web or if you aren't well-versed in server configuration, then these scripts are for you. Automate installation of Apache, MySQL, PHP, phpMyAdmin, Let's Encrypt (free SSL) as well as automate the deploy of WordPress for new domains. For WordPress deployment, I've used [wp-cli](https://github.com/wp-cli/wp-cli), the renowned WordPress deployment command-line tool.

## Getting started

Step 1: Clone the repo

```bash
git clone https://github.com/rehmatworks/lamp-pack
```
Step 2: Browse the directory
```bash
cd lamp-pack
```
Step 3: Make sp-lamp.sh executable
```bash
chmod +x sp-lamp.sh
```

Step 4: Execute the script and wait for the configuration to complete
```bash
./sp-lamp.sh
```

## Dealing with vhosts
Creating vhosts
```bash
spvhost create example.com
```

Deleting vhosts (Beware! This will delete the domain's directory with all data as well)
```bash
spvhost delete example.com
```
## Deploying WordPress (Courtesy: [wp-cli](https://github.com/wp-cli/wp-cli))
When you deploy a WordPress website, a new vhost is created. So if you have created any vhost previously, then you will have to delete it before proceeding.
```bash
 spwp example.com "Website Title" "admin_username" "admin_email" "admin_password"
```

