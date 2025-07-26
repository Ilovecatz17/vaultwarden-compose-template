# vaultwarden-compose-template

This is for people who want to set up vaultwarden with Docker compose but dont know what to put in the compose file

```services:
  server:
    container_name: vaultwarden
    image: vaultwarden/server:latest
    ports:
      - '[port]:80'
    volumes:
      - '[Folder to hold vaultwarden data]:/data'
    environment:
      - SIGNUPS_ALLOWED="true" or "false"
      - ADMIN_TOKEN=[password] 
      - DOMAIN= [Website that its hosting to, for example, "localhost:8080"]

Make sure to back up your compose file when updating vaultwarden
