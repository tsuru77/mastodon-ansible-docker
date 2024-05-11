# Deploying Mastodon instance

Using Ansible to deploy a Mastodon instance on a swarm cluster with Traefik reverse proxy and Let's Encrypt SSL certificate.

# Requirements

- 3 VPS on a cloud provider (ex: DigitalOcean)

- Ansible installed from the computer where your will be executing the playbook

- A domain name with A records created (vps)


# Steps 

## 1. Generate SSH keys

Before buying your VPS, you need to generate ssh keys so that afterwards you can log in your vps with the ssh keys.

```bash
ssh-keygen -t rsa
```

## 2. Deploy

Use the command below to deploy your mastodon instance

```bash
ansible-playbook -i inventory.yml -u root deploy.yml --private-key=~/.ssh/id_rsa
```