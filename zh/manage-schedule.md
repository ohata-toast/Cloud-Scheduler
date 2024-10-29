# Manage Schedule
**Application Service > Cloud Scheduler > Console User Guide > Manage Schedule**

This document explains the feature to manage the schedules you create.

!!! tip "Important"
    Date data is based on UTC+09:00.

## Change Schedule
You can select a schedule to change its information, including execution information, target information, and more. Select the schedule you want to change, then click **Change Schedule**. See [Create Schedule](create-schedule) to change the schedule information.

!!! danger "Caution"
    It can take up to 20 seconds for changes to the schedule to be reflected, so changes to the contents of the schedule, including activation/deactivation, may fail during that time.


## Delete Schedule
You can select a schedule to delete. You can also delete multiple at the same time. Select the schedule you want to delete, then click **Delete Schedule**.

## Copy Schedule
Select the schedule you want to copy, then select **Copy Schedule** to copy.
The schedule name and description are not copied, which is useful if you want to reuse a pre-created schedule.

## Activate/Deactivate Schedule
Select a schedule, and then click **Activate** or **Deactivate**.

!!! tip "Important"
    * A deactivated schedule will not execute any schedules.
    * If you reactivate a deactivated schedule, it will not run any schedules that were not run during the deactivation period.
    * Activation/deactivation can be performed after multiple simultaneous selections.
    * It is not possible to select both activated and deactivated schedules at the same time.

## View Schedule Information
You can view schedule information in the bottom area of the screen by selecting the schedule you're using.

* **Basic Information**: Show basic information about the schedule, including the name, description, status, and execution type.
* **Target Info**: Show the URL, HTTP method, HTTP headers, and parameters to run the schedule.
* **Execution History**: Show when the schedule is executed, whether it succeeded or failed, whether it was retried, and the execution log.
* **Additional Settings**: Check the retry policy information.