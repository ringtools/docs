# For admins

## Ring Wizard

The ring wizard automates the channel setup, just use `/start_ring_wizard` and follow the steps.

## Manually set up Telegram channel

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


## Opening channels

1. (Optional) reorder participats with `/set_order [PubKeysContents]` (after reordering, download pubkeys.txt from [ringtools-web](https://rof.tools))
2. Share ring visual from the watch page of [ringtools-web](https://rof.tools)
3. Let know who has to open with who `/ring_channels long`
4. Set the channel message to auto update with `/set_ring_mode opening_channels`
5. Get ring visual `/ring_visual`