# Pushover
Script to send Pushover notifications from command line

Inspired by: https://github.com/akusei/pushover-bash

* Download to location in $PATH ...
`wget https://raw.githubusercontent.com/danteali/Pushover/master/pushover -O /usr/bin/pushover`

* Edit script and add your API key - get from Pushbullet website
* Add your own user_key to the script
* Add your own list of channels and corresponding API keys to the script
* Make executable: `chmod +x /usr/bin/pushover`
* Run: `pushover -c alerts -u yyyyyyyyyy -m "This is a test"
  Sends a simple "This is a test" message to app/channel 'alerts'.

## Usage:

`$ pushover --help`

```Push notifications to your Android, iOS, or desktop devices

NOTE: This script requires an account at http://www.pushover.net

usage: pushover <-c|--channel app_name> <-t|--token apikey> <-u|--user userkey> <-m|--message message> [options]

  -c,  --channel APP_NAME    The pushover.net application name (as defined in script)
  -t,  --token APIKEY        The pushover.net API Key for your application (not needed if supplying defined channel)
  -u,  --user USERKEY        Your pushover.net user key
  -m,  --message MESSAGE     The message to send; supports HTML formatting
  -a,  --attachment filename The Picture you want to send
  -T,  --title TITLE         Title of the message
  -d,  --device NAME         Comma seperated list of devices to receive message
  -U,  --url URL             URL to send with message
       --url-title URLTITLE  Title of the URL
  -p,  --priority PRIORITY   Priority of the message
                               -2 - no notification/alert
                               -1 - quiet notification
                                0 - normal priority
                                1 - bypass the user's quiet hours
                                2 - require confirmation from the user
  -s,  --sound SOUND         Notification sound to play with message
                               pushover - Pushover (default)
                               bike - Bike
                               bugle - Bugle
                               cashregister - Cash Register
                               classical - Classical
                               cosmic - Cosmic
                               falling - Falling
                               gamelan - Gamelan
                               incoming - Incoming
                               intermission - Intermission
                               magic - Magic
                               mechanical - Mechanical
                               pianobar - Piano Bar
                               siren - Siren
                               spacealarm - Space Alarm
                               tugboat - Tug Boat
                               alien - Alien Alarm (long)
                               climb - Climb (long)
                               persistent - Persistent (long)
                               echo - Pushover Echo (long)
                               updown - Up Down (long)
                               none - None (silent)

CHANNELS:
  These channels have been defined in the script:
alert, backup, docker, media_stack, notifications, monitor, system,

NOTES:
  - APIKEYs are created within pushover web interface for different apps, equivalent to Slack channels.
  - You can define multiple channel's APIKEYs inside the script or config file, if doing this the '--token' APIKEY
    does not need to be supplied.

EXAMPLES:

  pushover -c alerts -u yyyyyyyyyy -m "This is a test"
  Sends a simple "This is a test" message to app/channel 'alerts'.

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test"
  Sends a simple "This is a test" message to all devices.

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test" -T "Test Title"
  Sends a simple "This is a test" message with the title "Test Title" to all devices.

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test" -d "Phone,Home Desktop"
  Sends a simple "This is a test" message to the devices named "Phone" and "Home Desktop".

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test" -U "http://www.google.com" --url-title Google
  Sends a simple "This is a test" message to all devices that contains a link to www.google.com titled "Google".

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test" -p 1
  Sends a simple "This is a test" high priority message to all devices.

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test" -s bike
  Sends a simple "This is a test" message to all devices that uses the sound of a bike bell as the notification sound.

  pushover -t xxxxxxxxxx -u yyyyyyyyyy -m "This is a test Pic" -a /path/to/pic.jpg
  Sends a simple "This is a test Pic" message to all devices and send the Picture with the message.```
