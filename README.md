# Keycloak with Amazon RDS and SSL Certificate in a Docker Swarm

Install Docker Swarm by following my [guide](https://www.heyvaldemar.com/install-docker-swarm-on-ubuntu-server/).

Create an Amazon RDS database instance, configure Traefik and create secrets for storing the passwords on the Docker Swarm manager node before applying the configuration.

Traefik [configuration](https://github.com/heyValdemar/traefik-ssl-certificate-docker-swarm).

Create a secret for storing the password for Keycloak database using the command:

`printf "YourPassword" | docker secret create keycloak-postgres-password -`

Create a secret for storing the password for Keycloak administrator using the command:

`printf "YourPassword" | docker secret create keycloak-application-password -`

Clear passwords from bash history using the command:

`history -c && history -w`

Deploy Keycloak in a Docker Swarm using the command:

`docker stack deploy -c keycloak-traefik-ssl-certificate-rds-docker-swarm.yml keycloak`

# Author

hey, I’m Vladimir Mikhalev, but my friends call me Valdemar.

🌐 My [website](https://www.heyvaldemar.com/) with detailed IT guides\
🎬 Follow me on [YouTube](https://www.youtube.com/channel/UCf85kQ0u1sYTTTyKVpxrlyQ?sub_confirmation=1)\
🐦 Follow me on [Twitter](https://twitter.com/heyValdemar)\
🎨 Follow me on [Instagram](https://www.instagram.com/heyvaldemar/)\
🎸 Follow me on [Facebook](https://www.facebook.com/heyValdemarFB/)\
🎥 Follow me on [TikTok](https://www.tiktok.com/@heyvaldemar)\
💻 Follow me on [LinkedIn](https://www.linkedin.com/in/heyvaldemar/)\
🐈 Follow me on [GitHub](https://github.com/heyvaldemar)

# Communication
👾 Chat with IT pros on [Discord](https://discord.com/invite/D7fGMYjdR9)\
🚀 Chat with IT pros on [Telegram](https://t.me/heyValdemarCOMchat)\
📧 Reach me at ask@sre.gg

# Give Thanks
💎 Support on [GitHub](https://github.com/sponsors/heyValdemar)\
🏆 Support on [Patreon](https://www.patreon.com/heyValdemar)\
🥤 Support on [BuyMeaCoffee](https://www.buymeacoffee.com/heyValdemar)\
🍪 Support on [Ko-fi](https://ko-fi.com/heyValdemar)\
💖 Support on [PayPal](https://www.paypal.com/paypalme/heyValdemarCOM)
