# Overview

The RingTools Telegram-bot is currently main supporting the Satoshi Radio / Connect the World Rings of Fire and therefore mainly suited as support for the process they are using. It is still is early development so commands might change.

## Public commands
| Command | Description                      |
| --- | --- |
| /ping                          | Check if I'm alive. |
| /set_language [lang]           | Change language of the bot (en, es, de, nl) |
| /fullnodeaddress [PubKey]      | Get full address of lightning node |
| /nodeinfo [PubKey]             | Get Lightning node info |
| /chaninfo [ChannelID]          | Get Lightning channel info |
| /set_country [CountryCode]     | Set your country to #connect_the_world (e.g. NL or US) |
| /add_node                      | Register node (see convience features) |
| /country_visible               | Make country visible in ring participation polls. |
| /howtojoin                     | Get instructions on how to join a Ring of Fire |
| /donate [Sats] [Message]       | Donate to Ringtools-Web Development |

## Ring-group commands

### For all ring participants
| Command | Description                      |
| --- | --- |
| /ringurl                       | Get ring-specific link for Ringtools-Web | 
| /get_tz                        | Get overview of timezones of all participants| 


### For individual ring participants
| Command | Description                      |
| --- | --- |
| /participate [PubKey]          | Join this ring (if you don't have any channels, use your full node URI) |
| /unparticipate                 | Leave this ring |
| /set_funded                    | Confirm you are funded |
| /set_country [CountryCode]     | Set your country to #connect_the_world (e.g. NL or US) |
| /unparticipate                 | Leave this ring |
| /get_file [igniterconf]        | Get igniter.conf file (only when all channels are opened) |

### For masters of ceremony
| Command | Description                      |
| --- | --- |
| /ring_channels                       | Get overview of channels |
| /node_overview                       | Ring participant overview |
| /start_ring_wizard                   | Start Ring Wizard |
| /edit_ring_wizard                    | Edit Ring Wizard |
| /set_order [PubKeysContents]         | Reorder participants (using pubkeys.txt export from Ringtools-Web) |
| /set_order_user [username]           | Reorder participants (set @username at the bottom for igniter) |
| /set_ringleader                      | Set Ringleader of the ring |
| /update_ring                         | Update ring name and logo |
| /ring_visual                         | Get ring visual (same as on rof.tools) |
| /raffle [user1] [user2] [user...]    | Do a raffle, e.g. ringleader selection. |
| /explain_igniter                     | Explain Igniter output. Reply to a single message with output or to a file in the chat. |
| /view_channel_settings               | View channel settings |
| /import_csv [FileContents]           | Import Groupnodes CSV from Cheeserobot |
| /update_name                         | Update ring name |
| /update_logo                         | Update ring group logo |
| /set_autoclean [cmd\|self] [true]     | Change autoclean settings |
| /set_greeting [text]                 | Set new user message |
| /post_message [template]             | Post message (welcome, opening_channels, igniter, fee_info, balanced) |
| /set_name [RingName]                 | Set name of ring |
| /set_size [RingSize]                 | Set size of ring |
| /set_ring_mode [mode]                | Set ring mode (e.g. opening_channels) |
| /ring_greet [true/false] [cleanDelay]| Enable/disable new user greeting |

### Poll commands
| Command | Description                      |
| --- | --- |
| /poll_ring [RingName] [MaxPpl] | Create poll to join a ring |
| /poll_repost [RingName] [MaxPpl] | Repost poll to join a ring |
| /poll_ringleader               | Create poll to become ringleader (admins only) |
| /admin_close_poll              | Force close poll |
