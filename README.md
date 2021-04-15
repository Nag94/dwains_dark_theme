<h1 align="center">Dwains Dark Theme</h1> 


<p align="center">
  <a href="https://github.com/LRvdLinden/dwains_light_theme">
    <img src="https://img.shields.io/github/v/release/LRvdLinden/dwains_light_theme" />
  </a>
      <a href="https://github.com/LRvdLinden/dwains_light_theme">
    <img src="https://img.shields.io/github/downloads/LRvdLinden/dwains_light_theme/latest/total?color=purple&label=%20release%20Downloads" />
  </a>
    <a href="https://github.com/LRvdLinden/">
    <img src="https://img.shields.io/github/followers/LRvdLinden?style=social" />
  </a>
    </a>
    <a href="https://discord.gg/7yt64uX">
    <img src="https://img.shields.io/discord/688401603811999885" />
  </a>
</p>

<p align="center">A Lovelace Dark theme based on <a href=https://github.com/dwainscheeren/dwains-lovelace-dashboard>Dwains Dashboard</a></p>
<p align="center">Created by <a href="https://github.com/LRvdLinden">Léon van der Linden</a></p> 

<p align="center">
  <img src="https://user-images.githubusercontent.com/77990847/114923935-b312c200-9e2d-11eb-81b2-3ae17998b3dd.png" />
</p>


## Prerequisite
---
- Make sure you have can access youre Home Assistant config files with [Samba Share](https://www.youtube.com/watch?v=udqY2CYzYGk) or [ssh](https://community.home-assistant.io/t/home-assistant-community-add-on-ssh-web-terminal/33820)
```yaml
     # Example configuration.yaml entry
     google:
       client_id: YOUR_CLIENT_ID
       client_secret: YOUR_CLIENT_SECRET
```
- Make a calendar in Google with all the birthdays and sync the calendar with Home Assistant
- Make sure you have installed [fontawesome icons](https://github.com/thomasloven/hass-fontawesome). This can be done manually or directly via hacs.

## Installation Add-on
---
- Copy the `birthdays` folder in to the `dwains-dashboard/addons/more_page` directory.
- Open your `more_page.yaml` file in `dwains-dashboard/configs` and add the following;
 ```yaml
     - name: Birthdays
       main_menu: 'true' #Show this addon in the main navigation bar!
       icon: fas:gifts
       path: 'dwains-dashboard/addons/more_page/birthdays/page.yaml'
```
- Reload the theme configuration via Theme Settings

## Replace the following
---
 ```yaml
            - type: custom:atomic-calendar-revive
              style: |
                ha-card {
                  border-radius: 5px;
                  background-color: var(--dwains-theme-primary);
                }
                .cal-titleContainer {
                  display: none;
                }
              showProgressBar: false
              eventBarColor: 'var(--dwains-theme-grey)'
              dayWrapperLineColor: 'var(--dwains-theme-grey)'
              timeColor: 'var(--dwains-theme-grey)'
              entities:
                - calendar.friends_birthdays
```
- on line 60: add the correct `entity` or `entities` to show


## Result
---
![IMG_0544](https://user-images.githubusercontent.com/77990847/114402640-52bd1f80-9ba4-11eb-990e-7a04642bd641.PNG)

---
Enjoy my card? Help me out for a couple of :beers: or a :coffee:!

[![coffee](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://www.buymeacoffee.com/LRvdLinden)
