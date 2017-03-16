# Introduction

StarRiver Web control system is intended for control and management of luminaires and other devices. It is a portal integrates information of connected devices with which devices can be accessed remotely. 

This document provides instructions on installation and configuration. Mandatory steps are denoted that you may not miss. Also there’s an [FAQ](part3/errors.md) at the end of the document, the first thing you may turn to if you run into any trouble with the system.

## Outline

The outline of the StarRvier Web control system is listed as follows:

### Control Module

- Map view
  All devices are shown on the map as icons after placing them respectively in the `Device` - `Map`. This page also allow you to click the device icon for its status, turn a lamp or a group of lamps up and down, and synchronize device with the computer where the StarRiver web page runs.
- Shortcut
  Pick a scenrio and click `Apply` to apply the dimming strategy defined in it to the devices respectively. Scenarios on this page are listed by groups only if any has been defined and added into at least one group. 
- Controller 
  Display status of all the controllers, including each of `Communications state`, `Device state`, and `Dimming mode`.
- Lamp
  Display status of all the lamps, including each of `Communication state`, `Brightness`, `Input voltage`, etc.
- Charging pile
  Display information for each charging piles, including each of `State`, `Duration of last charging`, `Volume of last charging`, etc.
- System Control
  User could choose and apply working mode and emergency dimming policy to each controller.  There are two working modes: `remote` and `auto`. Devices in remote mode execute dimming commands from the server. Devices in auto mode work independently according to a preconfigured time schedule. Emergency dimming policies include: `Failure brightness` (set during device configuration), `Keep brightness` and `Mmergency dimming schedule`. The policy would be used when a device lost connection to the server.

### Configuration Module

- Time-Brightness Schedule
  A schedule defines brightness values in each time periods, can be used to specify brightness for devices directly or schedule multiple devices in a scenario.

- Auto-Brightness Schedule
  A chart defines the denpendence curve of brightness and the sensor input, can be used to specify brightness for devices directly or schedule multiple devices in a scenario.

- Scene Configuration
  A scenario defines brightnesss for each device manually or automatically depending by a time-brightness schedule or a auto-brightness schedule.

- Emergency Control
  Contingency plan is defined to deal with an emergency or a contingency such as  a fogy day, that need two-hour more long lighting. So that its priority is higher than the scenario.

- Playlist

  A playlist defines contents showing in the outdoor advertisingboard integrated in a intelligent roadmap.

### Query Module

- Query device failure record
- Query device historical data (such as brightness, current, voltage, etc.)
- Query user operating record

### User Management Module

- User’s privilege management;　software needs login;　different user has different privilege
- Administrators could `add` or `delete` users and modify a user's privilege.

## Login

1. Open the system URL in a browser. 
2. Enter user name and the password to login. The administrator user is `admin` and its initial password is `admin`.  

![Login](./part1/img/login.png 'Login')

<p style="text-align: center">Picture 1-1 Login</p>

![Dashboard](./part1/img/dashboard.png 'Dashboard')

3. After login, a dashboard with useful system statistics such as `Energy consumption`, `Lighting rate`, `Luminaire condition` and `Energy savings`, etc., is listed on the homepage, as shown in the figure above.