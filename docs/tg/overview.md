# Overview

The RingTools Telegram-bot is currently main supporting the Satoshi Radio / Connect the World Rings of Fire and therefore mainly suited as support for the process they are using. It is still is early development so commands might change.

## Public commands
````text
/ping                           - Check if I'm alive.
/donate [Sats] [Message]        - Donate to Ringtools-Web Development
/fullnodeaddress [PubKey]       - Get full address of lightning node
/nodeinfo [PubKey]              - Get Lightning node info
/chaninfo [ChannelID]           - Get Lightning channel info
/set_country [CountryCode]      - Set your country to #connect_the_world (e.g. NL or US)
/add_node                       - Register node (see convience features)
/country_visible                - Make country visible in ring participation polls.
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
/get_file [igniterconf]           - Get igniter.conf file (only when all channels are opened)
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
/update_logo                          - Update ring group logo
````

### Poll commands
````diff
- /poll_ring [RingName] [MaxPpl]  - Create poll to join a ring, old format (admins only)
/poll_ring_v2 [RingName] [MaxPpl]  - Create poll to join a ring (admins only)
/poll_ringleader                - Create poll to become ringleader (admins only)
/admin_close_poll               - Force close poll
````