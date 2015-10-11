# Synchronise dotepub with your Kindle

https://dotepub.com/ is a great project to convert web pages into nice and tidy epub or mobi files.

I personally love this project because it stops me from skim-reading ( https://en.wikipedia.org/wiki/Speed_reading#Effect_on_comprehension ).

Quite nice to cache really great articles throughout the work week then relax with a fully loaded Kindle somewhere on the weekend.


## Simple udev rules and script to sync dotepub with your Kindle when it's plugged in

## Configuration

Place the in 100-sync-dotepub.rules and edit it, you'll need to change the USB ID's and the script parameters (user name, mount dir, source of epub files)

```
lsusb|grep Kindle
Bus 001 Device 043: ID 1949:0004 Lab126, Inc. Amazon Kindle 3/4/Paperwhite

```

And then place the sync-kindle-epub script in the appropriate target directly as specified in the 100-sync-dotepub.rules - I'm guessing you're not me :)

### Logging

Check /var/log/syslog or your usual syslogd daemon to monitor the output