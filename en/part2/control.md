# Control

This chapter provides instructions on how to check information and apply changes for all the devices in the system.

## Map View

![Map View](img/control_mapView.png 'Map View')

<p style="text-align:center">Picture 2-1 Map View</p>

All the devices can be seen as icons with name lables and managed in the map view when they have been properly added to the map.

### Controller Management

#### Check Status

1. Select `Control` - `Map View` and locate the target controller on the map.
2. The controller status will be shown in the popping-up dialog box after clicking on the controller.

The following table specified the items of the status list.

| Item               | Description                              |
| ------------------ | ---------------------------------------- |
| Communicaton state | Indicates if the device is able to communicate with the server or not |
| Status code        | Indicates if the device functions correctly or not |
| Work mode          | Shows the current work mode of the device, `Auto` or `Remote` |

#### Clock Synchronization for a Controller

1. Select `Control` - `Map View` and locate the target controller on the map.
2. Click on the controller.
3. Click on `Control` in the popping-up dialog box. The dialog box will expand and a hidden button show up as the figure shown below.
4. Click on the  `timing` button to synchronize the clock of the controller to the local computer.

![Controller status in Map View](img/control_controllerStatus.png 'Controller status in Map View')

### Lamp Management

#### Check Status

1. Select `Control` - `Map View` and locate the target lamp on the map. 
2. The lamp status will be shown in the popping-up dialog box after clicking on the lamp.

The following table specified the items in the status list.

| Item                | Description                              |
| ------------------- | ---------------------------------------- |
| Brightness          | Indicates the brightness of the lamp     |
| Lamp State          | Indicates if the lamp is normal or not   |
| Communication State | Indicates if the device is able to communicate with the server or not |
| Lamp                | Indicates if the lamp hardware is normal or not |

#### Brightness Control

1. Select `Control` - `Map View` and locate the target lamp on the map. 
2. Click on the lamp.
3. Click on `Control` in the popping-up dialog box. The dialog box will expand and a hidden button show up as the figure shown below.
4. Choose one of the patterns to control the brightness and click `Summit` to save the change.

![Lamp status and control in Map View](img/control_lampStatus.png 'Lamp status and control in Map View')

The following table gives the information on the three patterns controlling the brightness

| pattern   | Description                              |
| --------- | ---------------------------------------- |
| Manual    | The lamp will emit light as brightness value specified once submitted. |
| Schedule  | The lamp will emit light as the selected schedule specified once submitted. |
| Automatic | The lamp will emit light depending on the light sensor as the selected dependence chart specified once submitted. |

## Shortcut

A scenario is a plan that defines the light-emitting patterns each device (could be lamp or controller) should follow. Applying a scenario implements a quick pattern switch for multiple devices at one time.

Scenarios are displayed by groups in the `Control` - `Shortcut` screen where a scenario can be applied simply by clicking one button, which means that, a scenario can only be found and applied when it is one of the scenario group member.

<div style="text-align:center">

![Shortcut](img/control_shortcut.png 'Shortcut')

<p style="text-align:center">Picture 2-4 Shortcut</p>

Before appling any scenario, you need to add and define scenario in the `Config` - `Scene` tab (see section [Scenario][] for instruction) and group scenarios in the `Config` - `Sceneconfig` tab (see section [Group Scenario][] for instruction).

## Controller Status

![Controller](img/control_controller.png 'Controller')

<p style="text-align:center">Picture 2-5 Controller status</p>

To get information (`communication state`, `device state`, `dimming model`) of all the controllers select `Control` - ` Controller`, as shown in the figure above.

Click `Previous` or `Next` to turn the page backward or foreward.

## Lamp
![Lamp](img/control_lamp.png 'Lamp')
<p style="text-align:center">Lamp status</p>
To get information (`communication state`, `device state`, `brightness`, `input and output voltage`, `input and output current`, `power`, etc.) of all the controllers select `Control` - ` Controller`, as shown in the figure above.
Click `Previous` or `Next` to turn the page backward or foreward.
## Work Mode of Controllers
Controllers can be working under `Auto` mode or `Remote` mode. 

- The `Auto` mode, in which controllers are offen offline and working as the contingency plan specified 
- The `Remote` mode, in which controllers are in good connections with the server and can be acted as operating in real time


> **Tips**:A contingency plan designates brightness for device group in multiple time periods.

### Auto Mode

1. Select `Control` - `System Control`.

2. Locate the target controller and click to swith its work mode to `Auto` if it is not.

   > **Note**: If a controller is appearred unknown mode, neither `Auto` nor `Remote` mode, the very controller must have connection failure or other errors that is not available for the system.
3. Select a contingency plan in the drop down list. Contingency plans could be added in the `Config` - `Emergency ` page.
4. Click `Apply` to save the change.



![System Control](img/control_sysControl.png 'System Control')

<p style="text-align:center">Work Mode of Controllers</p>

### Remote Mode

1. Select `Control` - `System Control`.

2. Locate the target controller and click to swith its work mode to `Remote` if it is not.

   > **Note**: If a controller is appearred unknown mode, neither `Auto` nor `Remote` mode, the very controller must have connection failure or other errors that is not available for the system.

3. Choose a strategy when a comminication a failure detected. 

   - Fault brightness, which could be set in the `Devices` - `Dimming Params`.
   - Current brightness, which keeps nothing changed
   - The contingency plan, which shall be specified before or after this procedure.

4. Enter the time periods that triggerred an emergency, range from 1-65535 minutes.

5. Click `Apply` to save the change.

   if you choose `Contingency plan`, follow the instruction below after finishing all the steps above:

6. Locate the target controller and choose a contingency plan in the drop list.

7. Click `Apply` to save the change.