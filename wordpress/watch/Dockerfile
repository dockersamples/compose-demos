# Use the official WordPress image as the base image
FROM wordpress:latest

# Install and activate the Contact Form 7 plugin
RUN apt-get update && apt-get install -y unzip && \
    curl -o /tmp/contact-form-7.latest-stable.zip -SL https://downloads.wordpress.org/plugin/contact-form-7.latest-stable.zip && \
    unzip /tmp/contact-form-7.latest-stable.zip -d /var/www/html/wp-content/plugins/ && \
    rm /tmp/contact-form-7.latest-stable.zip

# Expose the port (usually port 80) on which your WordPress site runs
EXPOSE 80
