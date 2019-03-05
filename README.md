# Team12Drupal-Helpdesk

# How to run
Ensure you have docker installed. 

Clone the Github repo to a folder you like. 

Then, navigate into that folder and run `docker-compose up -d --build`.

Navigate to `localhost:8080` to view the Drupal website.

# Troubleshooting some issues
Hopefully the above instructions work and we shouldn't need the things below but I have included them just in case.
### Installing dependencies using composer.
After loading up the container in the how to run section, run `docker-compose ps` and take note of the name of the container that has port 80 forwarded. The name should look something like `team12drupal-helpdesk_drupal_1_17f577420c3c`. 

Then run `docker exec -it team12drupal-helpdesk_drupal_1_17f577420c3c bash` replacing with your container name. You will now be inside the container.

Run the command `composer install` to install dependencies. Once this is done, on a web browser, navigate to `localhost:8080` to view the website and finish the installation.

### Database settings
When setting up the database, the database name and username is as follows.
```
host: db
username: msg whatsapp to find
password: msg whatsapp to find
```
