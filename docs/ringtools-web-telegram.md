# Telegram Bot

The RingTools Telegram-bot is currently main supporting the Satoshi Radio / Connect the World Rings of Fire and therefore mainly suited as support for the process they are using. It is still is early development so commands might change.

## Public commands
````text
/ping                           - Check if I'm alive.
/donate [Sats] [Message]        - Donate to Ringtools-Web Development
/fullnodeaddress [PubKey]       - Get full address of lightning node
/nodeinfo [PubKey]              - Get Lightning node info
/chaninfo [ChannelID]           - Get Lightning channel info
````

## Ring-group commands

### For all ring participants
````text
/ringurl                        - Get ring-specific link for Ringtools-Web
/ring_channels                  - Get overview of channels
/node_overview_csv              - Export Groupnodes CSV
/node_overview                  - Ring participant overview
````

### For individual ring participants
````text
/participate [PubKey]           - Join this ring (if you don't have any channels, 
                                  use your full node URI)
/unparticipate                  - Leave this ring
/set_funded                     - Confirm you are funded
/set_country [CountryCode]      - Set your country to #connect_the_world (e.g. NL or US)
/unparticipate                  - Leave this ring
/get_tz                         - Get overview of timezones of all participants
/get_file [ignitersh]           - Get igniter.sh file (only when all channels are opened)
````

### For masters of ceremony
````text
/set_name [RingName]                  - Get Lightning channel info
/set_size [RingSize]                  - Get Lightning channel info
/import_csv [FileContents]            - Import Groupnodes CSV from Cheeserobot
/set_ring_mode [mode]                 - Set ring mode (e.g. opening_channels)
/ring_group_logo [Size] [Nr]          - Create a ring group logo (admins only) 
                                        last parameters are balanced and country
/set_order [PubKeysContents]          - Reorder participants (using pubkeys.txt export 
                                        from Ringtools-Web)
/set_ringleader                       - Set Ringleader of the ring
/post_message [welcome|channels]      - Post welcome/channel opening message
/view_channel_settings                - View channel settings
/set_autoclean [cmd|self] [true]      - Change autoclean settings
/set_greeting [text]                  - Set new user message
/ring_greet [true/false] [cleanDelay] - Enable/disable new user greeting
/update_name                          - Update ring name
/ring_visual                          - Get ring visual (same as on rof.tools)
/ring_group_logo_update               - Update ring group logo
````

### Poll commands
````text
/poll_ring [RingName] [MaxPpl]  - Create poll to join a ring (admins only)
/poll_ringleader                - Create poll to become ringleader (admins only)
/admin_close_poll               - Force close poll
````

## Participate in ring

1. Signal your participation with `/participate [PubKey]` (e.g. `/participate 0380b3dbdf090cacee19eb4dc7a82630bd3de8b12608dd7bee971fb3cd2a5ae2fc`)
2. Set your country with `/set_country [Country]` using the 2-letter country code (e.g. `/set_country nl`)
3. Let know if/when you have the funds to open the channel `/set_funded true` 

## Set up Telegram channel (for admins)

1. Create channel group, set name and invite [@ringtools_bot](https://t.me/ringtools_bot).
2. Set name and size:
    - `/set_name [RingName]` (e.g.) `/set_name #SRROF_1Msats_21stRING`
    - `/set_size [RingSize]` (e.g.) `/set_size 1000000`
3. Get channel logo: `/ring_group_logo_update` (It should automatically detect size and number from the Ring Name).
4. Create ringleader poll: `/poll_ringleader`
5. Set autoclean (optional):
    - `/set_autoclean cmd true` (Removes bot commands by others after 1 minute)
    - `/set_autoclean self true` (Removes bot response after 1 minute)
6. (Optional) Post welcome message `/post_message welcome`
7. (Optional) Set user greeting `/set_greeting`
8. (Optional) Enable user greeting `/ring_greet true 900` (900 seconds is 15 minutes)
9. (Optional) Change ring group channel name `/update_name`


## Opening channels (for admins)

1. (Optional) reorder participats with `/set_order [PubKeysContents]` (after reordering, download pubkeys.txt from [ringtools-web](https://rof.tools))
2. Share ring visual from the watch page of [ringtools-web](https://rof.tools)
3. Let know who has to open with who `/ring_channels long`
4. Set the channel message to auto update with `/set_ring_mode opening_channels`
5. Get ring visual `/ring_visual`