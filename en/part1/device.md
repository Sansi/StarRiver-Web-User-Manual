# Device


##  Controller Configuration

A controller is a physical device that controls a set of lamps.  Always add a controller before adding a lamp.

### Add a Controller

1. Select  `Device` - `Controller` - `+ Add Controller` to add a controller.  A dialog box will pop up as shown in the figure below.

2. After filling the required fields, `Name`, `Device address`, `IP address`, `Port ` and `remarks` in the dialogbox, click on `Submit` to apply the change.

![Add an Controller](img/device_addController.png 'Add controller')


### Edit a Controller

1. Select `Device` - `Controller`. Locate the target controller and then click on the ![Edit](img\Edit.png 'Edit') (pencil-shaped) button which can be found in the responding row in the controller table.  A dialog box will pop up as shown in the figure below. 
2. After changing the desired item of the controller profile, `Name`, `Device address`, `IP address`, or `Port `  in the dialogbox, click on `Submit` to update.

  ![Edit an Controller](img/device_editController.png 'Edit controller')


### Delete a Controller

1. Select `Devices` - `Controller` .  Locate the target controller and then click on the ![Delete](img\Trash bin.png 'Delete') (bin-shaped) button which can be found in the responding row in the controller table.  
2. To make sure it's not a mistaken operation, the system would have you click on the  `confirm` button in the popping-up confirmation box, as shown in the figure below.

![Delete controller](img/device_delController.png 'Delete controller')

### Give Location Info. for an Controller

1. Select `Devices` - `Controller` , Locate the controller and then click on the![Location](img/Location.png 'Location') (arrow-shape) button which can be found in the corresponding row in the controller table. 
2. After giving the `latitude` and `longitude` in the popping-up dialog box click on the `Submit` button, as shown below.

   > **Note**:  The field will hightlight in red and refuse to  submit when put into invalid value.


![GPS position controller](img/device_GPSLocation.png 'GPS position controller')


## Lamp Management

This section will provide instruction on lamp management, including adding a lamp, editing the profile of a lamp and deleting a lamp. You will find the procdedures of hadling a lamp is very similiar to those of handling a controller. 


![Configuration lamp](img/device_configLamp.png 'Configuration lamp')

> **Note**: Try refresh when the newly added lamp does not show up in the lamp list.

## Lamp Group

Group is a logical collection that grouping lamps could be treated as one logical item, in another way, bulk operation would be eaiser to implement. For an expiedent in an emergency,  such as an eclipse of the sun, you need to have a temporaty schedule in which there're only grouping lamps can be added. See [Section Emergency Control](../part2/config). This section provides information on how to group lamps.

### Add a Lamp Group

Select `Devices` - `Group` - `+ Add Group` , and click `Submit` after entering the group name in the popping-up dialog box , as the figure shown below.
![Add lamp group](img/device_addLampGroup.png 'Add lamp group')

>**Note**:
>1. When selecting a newly added group, all lamps are listed in the `Non-group lamp` box.
>2. The total member nunber of the group would be shown in a yellow circle icon followed.

### Edit the Name of a Lamp Group

Select `Devices` - `Group` , and select the target group in the list. Click the ![Edit the Group Name](img/Pensil.png 'Edit the Group Name') (pencil-shaped) button, to enter a new name for the group.  And then don't forget to click checkmark button to apply the change. 

![Edit the name of lamp group](img/device_editLampGroupName.png 'Edit the name of lamp group')
​    
### Add/Remove Lamps to/from a Group

The  `group lamp` list of a newly added lamp group would be blank.

1. Select `Devices` - `Group`, and choose the target group.
2. Choose a lamp from the `non-group lamp` list and add itto the group by clicking  `>`. 
   Or, select the target lamp in the `group lamp` list and remove it from the group by clicking `<`, as shown in the figure below.
>**Tips**:
>
>1. Enter the name or any word contained in the name of the lamp into the filter to search rapidly in the `group lamp` or `non-group lamp` search box.
>2. Use`>>` or to add all lamps in the list into the group or `<<` to remove all lamps in the list from the group.

![Add/remove lamps in group](img/device_addOrRemoveLamp.png 'Add/remove lamps in group')

3. Click `Submit` to apply the change.


### Delete a Lamp Group
1. Select `Devices` - `Group` .  Locate the target group and then click on the ![Delete](img\Trash bin.png 'Delete')` Delete Group` button which can be found in the lower right corner below the list.  
2. To make sure it's not a mistaken operation, the system would have you click on the  `confirm` button in the popping-up confirmation box, as shown in the figure below.

![Delete lamp group](img/device_delLampGroup.png 'Delete lamp group')

## After Actions Above

After the actions above, changing controller and lamps information: 

1. A restart is needed to tell the server fetching updating data. Select `Devices` - `Restart Service`, click the `restart` button.![Restart Service](img/device_restartService.png 'Restart Service')
2. Wait for the restarting and relogin once it is ready.
3. Push the changes to the target controllers. Select `Deivces` - `Release Settings`. Choose the relevant controllers (changes effected), and then click `Release`.

## Sensors Management

StarRvier system collects and keep one-day long record of all the sensors. You need to add at least one light sensor before creating any automatic-dimming plan. Or You could query the information of the sensors (except for the light sensor) in `Query` - `Sensor`. Before that, you need to add them to the system. The following sections provide instructions on sensor management. If you are looking for instruction of sensors in a intelligent lamp, see the Section [Intelligent Lamp][] - [Add a Sensor][].

### Add a Sensor

1. Select  `Devices` - `Sensor` - `+ Add sensor` to add a sensor.  A dialog box will pop up as shown in the figure below.
2. After filling the required fields, `Name` and `type`  in the dialogbox, click on `Submit` to apply the change.

   > **Tips**: StarRiver system has supports for the following sensor type: light sensor, people flow counter and traffic flow counter. 

![Add sensor](img/device_addSensor.png 'Add sensor')

### Edit a Sensor

1. Select `Device` - `Sensor`.  Locate the target sensor and then click on the ![Edit](img\Edit.png 'Edit') (pencil-shaped) button which can be found in the responding row in the sensor table.  A dialog box will pop up as shown in the figure below. 
2. After changing the desired item of the controller profile, `Name` or `Type `  in the dialogbox, click on `Submit` to update.

![Edit sensor](img/device_editSensor.png 'Edit sensor')

### Delete a Sensor

1. Select `Devices` - `Sensor` .  Locate the target sensor and then click on the ![Delete](img\Trash bin.png 'Delete') (bin-shaped) button which can be found in the responding row in the sensor table.  
2. To make sure it's not a mistaken operation, the system would have you click on the  `confirm` button in the popping-up confirmation box, as shown in the figure below.


![Delete sensor](img/device_delSensor.png 'Delete sensor')

## Location Management

> **Note**: Online map is one of the threee supported map system. Contact the local vendor for the revision with support for one of the other two map system, raster map or offline map.   

To place devices in their respective postion in the map as they actually are, select  `Devices` - `Map location`.  

For exampe, there's one controller and its three lamps need to be placed in the map. 

- To allocate the device in the map click on ![Allocation](img/Location Allocate.png 'Allocation') to enter the place mode,  and then choose the target device in the list and drop it to the ideal location.

  > **Tip**:  
  >
  > - Enter the name or any word contained in the name of the device into the filter to search the target device rapidly on top of the device list.
  > - Drag the map to find the target spot and roll the mouse up or down to zoom in or out.

- To change the location of the device, click on ![Edit](img/Edit Plain.png 'Edit') to enter the edit mode,  and then select the target device in the map and drag it to the ideal location.

  > **Tip**:  Enter the name or any word contained in the name of the device into the search box to locate the target device rapidly.

- To remove a device from the map, click on ![Delete](img/Trash bin Plain.png 'Delete') to enter the delete mode,  and then select the target device in the map or list and click `save` to apply the change.


![View device location](img/view_device_location.png 'View device location')

## Raster Map

> **Note**: Raster map is one of the threee supported map system. Contact the local vendor for the revision with support for one of the other two map system, online map or offline map.   

Raster map is applied to scenario like tunnels. To manage devices in the raster map view, you need to upload image maps in the `Devices` - `Raster Map`. 

![Raster Map](img/device_rasterMap.png 'Raster Map')

### Add a Map

1. Select  `Devices` - `Raster Map` - `+ Add Map` to add a map.  

2. Click `Browse` in the popping-up dialog box. Browse and select an image map in the explorer, and then click `Open` to upload. 

   > **Tip**: The name of the map will be aotumatically filled with the name of the iamge file. However, it can be changed by clicking on the pencill button. Click on the check button to apply the change. 

### Edit a Map

To update image file or name of the exsting maps, follow the instructions below:

1. Select `Device` - `Raster Map`.  Locate the target map and then click  `Edit`  which can be found in the lower left of the responding map file.   

2. Click `Browse` in the popping-up dialog box. Browse and reselect an image map in the explorer, and then click `Open` to upload. 

   > **Tip**: The name of the map will be aotumatically filled with the name of the iamge file. However, it can be changed by clicking on the pencill button. Click on the check button to apply the change. 

### Delete a Map

1. Select `Device` - `Raster Map`.  Locate the target map and then click  `Delete`  which can be found in the lower right of the responding map file.  
2. To make sure it's not a mistaken operation, the system would have you click on the  `confirm` button in the popping-up confirmation box.

## Dimming Params

To set the brightness parameters of each lamp gourp, select `Device` - `Dimming Params`, as the figure shown below. Any changes of the parameter can only be applied to the selected group in the list. In another way, group the lamps before making any dimming change. After updating any parameters, click `Submit` to apply the change.

![Dimming Params](img/device_dimmingParams.png 'Dimming Params')

## Intelligent Lamp

Intelligent Lamp is a light pole which integrates a set of intelligent devices. To manage an intelligent lamp, select `Device` - `Intelligent Lamp` and add intelligent lamps into the system.

### Add an Intelligent Lamp

#### Add a Light Pole

Select `Devices`-`Intelligent Lamp`-`+Add Intelligent Lamp`, and give the name in the popping-up dialog box and click `Submit` to save the change, as the figure shown below.  

### ![Add Intelligent Lamp](img/device_addIntelligentLamp.png 'Add Intelligent Lamp')

Following the instruction above, you would have added an intelligent lamp into the system. Now, we can add each device of the intelligent lamp so that the system could perform fully control and mangement of this set of intelligent devices.

#### Add a Lamp

1. Select `Devices`-`Intelligent Lamp`, select the target intelligent lamp in the list.  

   > **Tip**:   Enter the name or any word contained in the name of the device into the search box to locate the target device rapidly.

2. After filling the required fields in the popping-up dialog box,  click on `Submit` to apply the change, as the figure shown below.

   > **Tip**: Try Refresh when the newly added device does not show up.

![Add Lamp](img/device_intelligentLamp_addLamp.png 'Add Lamp')

Locate the target controller and then click on the ![Delete](img\Trash bin.png 'Delete') (bin-shaped) button which can be found in the responding row in the controller table.  

#### Add Sensor

Click `Devices`-`Intelligent Lamp`,select the intelligent lamp you want to add device ,click `Sensor` tab and `+Add Sensor` button,a dialog box will pop up,you can select a sensor in the box and the click  `Submit` button,as shown below.

![Add Sensor](img/device_intelligentLamp_addSensor.png 'Add Sensor')

> **Note**：Device-specific configuration of the sensor see 2.4.2.。

#### Add Camera

Click `Devices`-`Intelligent Lamp`,select the intelligent lamp you want to add device ,click `Camera` tab and `+Add Camera` button,a dialog box will pop up,you need input IP,port,username,password,channel and select the type of this camera,and then click  `Submit` button,as shown below.

![Add Camera](img/device_intelligentLamp_addCamera.png 'Add Camera')

#### Add RFID

Click `Devices`-`Intelligent Lamp`,select the intelligent lamp you want to add device ,click `Rfid` tab and `+Add Rfid` button,a dialog box will pop up,you need select the type of RFID first,the type of `reader` need two item as IP and address,the type of `Trigger` and `Label` only need address,and then click  `Submit` button,as shown below.

![Add Rfid](img/device_intelligentLamp_addRfid.png 'Add Rfid')

#### Add Screen

Click `Devices`-`Intelligent Lamp`,select the intelligent lamp you want to add device ,click `Screen` tab and `+Add Screen` button,a dialog box will pop up,you can input the ip and port and select a Resolution in the box and the click  `Submit` button,as shown below.

![Add Screen](img/device_intelligentLamp_addScreen.png 'Add Screen')

#### Add Charging Pile

Click `Devices`-`Intelligent Lamp`,select the intelligent lamp you want to add device ,click `Charging Pile` tab and `+Add Charging Pile` button,a dialog box will pop up,you can select a charging pile through a search query box(such as input '4') in the box and then click  `Submit` button,as shown below.

![Add Charging Pile](img/device_intelligentLamp_addChargingPile.png 'Add Charging Pile')

### Edit the Name of an Intelligent Lamp

1. Select `Devices`-`Intelligent Lamp`. Locate the target sensor and then click on the ![Edit](img\Edit.png 'Edit') (pencil-shaped) button which can be found in the name field, as the figure shown below.  

   >**Tip**:   Enter the name or any word contained in the name of the device into the search box to locate the target device rapidly.

2. After updating the name, click the check button to apply the change. 

![Edit Intelligent Lamp Name](img/device_editIntelligentLamp.png 'Edit Intelligent Lamp Name')

### Give Location Info. for an Intelligent Lamp

1. Select `Devices`-`Intelligent Lamp`, select the target intelligent lamp in the list.  

   > **Tip**:  Enter the name or any word contained in the name of the device into the search box to locate the target device rapidly.

2. Click on the![Location](img/Location.png 'Location') (arrow-shape) button which can be found upper right of the screen. 

3. After giving the `latitude` and `longitude` in the popping-up dialog box click on the `Submit` button, as shown below.

   > **Note**:  The field will hightlight in red and refuse to  submit when put into invalid value.

### Delete an Intelligent Lamp

1. Select `Devices`-`Intelligent Lamp`, select the target intelligent lamp in the list and click  `Delete` to remove the item.  

   > **Tip**:   Enter the name or any word contained in the name of the device into the search box to locate the target device rapidly.

2. To make sure it's not a mistaken operation, the system would have you click on the  `confirm` button in the popping-up confirmation box.

   ![Delete Charging Pile](img/device_deleteLamp.png 'Delete Charging Pile')