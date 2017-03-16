# Wizard

This section is recommended for someone who is going to do the configuration and use the system for the first time. 

As an example, the following instruction will provide major procedure though in the actual world, things may be a little different. Refer to the [FAQ](/part3/errors.md) for problems may have. If it stunks and can't get any answers in the section above, contact the local retailer for tenical supports.

John is the administrator of the StarRiver system, who wants to acheive the following goals with *4* lamps in the *King street*. 

| Lamp | Controller | 1st quarter | 1st quarter | 2nd quarter | 2nd quarter |
| ---- | ---------- | ----------- | ----------- | ----------- | ----------- |
|      |            | 6 AM-6 PM   | 6 PM-6 AM   | 5 AM-7 PM   | 7 PM-5 AM   |
| A    | A          | Off         | On          | Off         | On          |
| B    | A          | Off         | On          | Off         | On          |
| C    | B          | Off         | On          | Off         | On          |
| D    | B          | Off         | 50% on      | Off         | 50% On      |

> **Note**:
>
> * As days getting longer in the 2nd quarter, lamp-lighting time need to be shrunk.
> * Lamp D stands near a resident building, that it's allowed to emit 50% light when on.

## Add Devices

First of all, we need to add the 4 lamps and their controllers into the StarRiver system for management and control.

### Add Controllers

Controllers communicate to the lamps directly that we need to add controllers before lamps.

1.  Select `Devices` - `Contrller` to get to the controller management page.

2.  Click `+ Add controllers`.

3.  Fill in the table in the poping-up box and click `submit` to save the change.
    * Device address: the MAC adress of the controller, you may find it in the documents comming with the controller.
    * IP address: make sure the IP address of the controller is not blocked from the server.
    * Port: *3434* is recommended. but if the port number has been occupied, try get another available one.

4.  Repeat Step 2 and Step 3 to add controller B.

5.  Make sure the information listed in the controller page is correct, click ![](img/Edit.png) to update information.

         Go to the next step if everything is ok.

### Add Lamps

Add lamps after controllers have been added.

1. Select `Devices` - `Lamp` to get to the lamp management page.
2. Click `+ Add lamp`.
3. Fill in the table in the poping-up box and click `submit` to save the change.
   - Device address: the MAC adress of the lamp, you may find it in the documents comming with the device.
   - Controller, according to the information given in the example, Lamp A is subordinated to Controller A.
4. Repeat Step 2 and Step 3 to add controller B.
5. Make sure the information listed in the controller page is correct, click ![](img/Edit.png) to update information.
   Go to the next step if everything is ok.

### Group Lamps

A lamp group is necessary for a contingency plan, and makes group dimming possible in the map view.

1. Select `Devices` - `Group` to get to the group page.
2. Click `+ Add group` and give a name for the group, such as, *Group 1*. After clicking `Submit` *Group 1* will be shown up in the group list.
3. Select *Group 1* in the group list, and then click `>>` in the lamp list to add all the lamps to *Group 1*. However, we don't need *Lamp D* in the *Group 1* indeed, so select *Lamp D* in the In Group list and then click `<` to remove it from the *Group 1*. 
4. Add *Group 2*.
5. Add *Lamp D* into *Group 2*.

>**Note**: Group information on the web page may not be up to date due to the network latency after the procedure. Do not take actions repeatly. Wait for a moment and refresh the web page to see the changes.
>
### Notify the Server and Controllers

Changes have been made to the data base, however, the server and controllers will not process with the update information until getting notification.

1. Restart the service.
   Select `Devices` - `Restart`, and click `Reset` to restart the service, so that the server will reload device information from the data base.
2. Wait until the web page is available, and then re-login.
3. Notify the controllers.
   Select `Devices` - `Release`, and click `Release` followed each related controllers to push the updated information to it.

Now, we have finished adding devices and can go to the next step, scheduling illumination plan.

## Schedule Illumination Plan

In this section, we will schedule illumination plan according to the given demands. Time-brigthtness schedule and scenario tools will be used for it. Also, a contingency plan would be created as a backup for the schedule. 

Besides, a contingency plan is very useful for controllers that are offline in most of the time. Controllers run in `Auto` mode with the contingency plan instead of a regular scenario but acheiving the same goal.

### Add a Time-Brightness Schedule

Select `Config` - `Time-Brightness Schedule`, and add 2 shedules as follows:

1. The first schedule, with brightness of  100 when on.

   | Start date | end date | time     | brightness |
   | ---------- | -------- | -------- | ---------- |
   | 01-01      | 03-31    | 06:00:00 | 0          |
   | 01-01      | 03-31    | 18:00:00 | 100        |
   | 04-01      | 06-30    | 05:00:00 | 0          |
   | 04-01      | 06-30    | 19:00:00 | 100        |



2. The second schedule, with brightness of 50 when on. 
   | Start date | end date | time     | brightness |
   | ---------- | -------- | -------- | ---------- |
   | 01-01      | 03-31    | 06:00:00 | 0          |
   | 01-01      | 03-31    | 18:00:00 | 50         |
   | 04-01      | 06-30    | 05:00:00 | 0          |
   | 04-01      | 06-30    | 19:00:00 | 50         |


### Add a Scenario

A scenario designates brightness or strategy for each device. In this example, we will designate the above schedules for each device.

| Device     | Name         | mode                     | brightness/schedule | Note                                     |
| ---------- | ------------ | ------------------------ | ------------------- | ---------------------------------------- |
| Controller | Controller A | Time-brightness schedule | *1st schedule*      | Apply the time schedule to all the lamps subordinated to the controller. |
| Device     | Lamp C       | Time-brightness schedule | *1st schedule*      | *Lamp C* should be *100* percent light as *Lamp A* and *Lamp B*. |
| Device     | Lamp D       | Time-brightness schedule | *2nd schedule*      | *Lamp D* should *50* percent light according to the given demands. |

2. To be applied rapidly, the scenario should be grouped in the `Config` - `Scene Config` page. 

### Add a Contingency Plan

A contingency plan is very useful for controllers that are offline in most of the time. Controllers run in `Auto` mode with the contingency plan instead of a regular scenario but acheiving the same goal.

Select `Config` - `Emergency Control`, add a plan as follow:

| Group     | Start date | end date | time     | brightness |
| --------- | ---------- | -------- | -------- | ---------- |
| All       | 01-01      | 03-31    | 6:00:00  | 0          |
| *Group 1* | 01-01      | 03-31    | 18:00:00 | 100        |
| *Group 2* | 01-01      | 03-31    | 18:00:00 | 50         |
| All       | 04-01      | 06-30    | 5:00:00  | 0          |
| *Group 1* | 04-01      | 06-30    | 19:00:00 | 100        |
| *Group 2* | 04-01      | 06-30    | 19:00:00 | 50         |

> **Note**: In the Grouping step, we have Lamp A, B, and C in the Group A and Lamp D in the Group B.

## Carry out the Plan

As all the schedules have been set up, we could carry out the plan.

1. Select `Control` - `System Control`, to designate a contingency plan for each controller.

2. Make sure each controller is working under the `Remote` mode. If not, click to switch to `Remote`.

   > **Note**: Under the `Remote` mode, the scenario can be applied. (which will be introduced in the next step.) While   in the `Auto` mode, the controller will execute the contingency plan pushed in the previous step.

3. Choose a contingency stratege.
   Check the *Contingency stratege* and give *30* (minutes) in the trigger time box, and click `Apply` to save the change. So that, when a commnunication failure has been detected and does not recover in 30 mininutes, the controller will execute the contingency plan designated in Step 1.

4. Select `Control` - `Shortcut`, and choose the target scenario before clicking `Apply`.

In the case of a offline-controller system, contingency plan can act as a regular plan. Follow the instructions below:
1. Select `Control` - `System Control`, to designate a contingency plan for each controller.

2. Make sure each controller is working under the `Auto` mode. If not, click to switch to `Auto` and click `Apply` to save the change.