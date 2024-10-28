# Create Schedule
**Application Service > Cloud Scheduler > Console User Guide > Create Schedule**


A schedule consists of basic information, target info, and additional settings.

* Basic information: Select the type, cycle, and start/end dates for the schedule to execute.
* Target info: Enter the API information and HTTP methods, headers, and parameters called by the schedule.
* Additional settings: Set whether to enable/disable the schedule and the retry policy (number of times, interval).

This document explains the steps to create a schedule in detail.

!!! tip "Important"
    Date data is based on UTC+09:00.


## Create Schedule

To create a schedule, you must first enable the Cloud Scheduler service. See [Guide to Enabling Project Services ](https://docs.nhncloud.com/en/nhncloud/en/console-guide/#_21) to enable the Cloud Scheduler service.

1. In the NHN Cloud console, click **Application Service > Cloud Scheduler**.
2. Click **+ Create Schedule**.

3. Enter basic information settings, then click **Next**.
    * **Name**: Enter a name for the schedule you're creating. You can enter up to 32 characters. 
    * **Description**: Enter a description for the schedule you're creating. You can enter up to 255 characters.
    * **Execution Type**: Select the type of schedule execution. The type can be **one-time** or **recurring**, and the settings will vary depending on the type you select.
        * **One-time**: Run the task only once at the time you specify. Enter the **execution date and time**.
        * **Recurring**: Run the task repeatedly at a set time or at a set interval. You can choose between **Cron** or **Rate** types to set when the task runs.
            * **Cron expression**: Enter 5 fields separated by spaces. The fields are, in order, "Minute hour day month day of week." Each field can be entered as shown in the following table, and you can also use symbols to separate entries in each field or to indicate repetition.
            
              | Field | Value | Allowed symbols |
              | --- | --- | --- |
              | minutes | 0~59 | `*`, `,`, `-` |
              | Hour | 1 to 1000 | `*`, `,`, `-` |
              | Day | 1~31 | `*`, `,`, `-` |
              | Month | 1 to 12 or JAN to DEC | `*`, `,`, `-` |
              | Day of the week | 0 to 6 or SUN to SAT | `*`, `,`, `-` | 
              
            * **Rate**: Run the schedule at a certain time interval (in minutes/hours/day). You can register for up to 30 days (43,200 minutes, 720 hours).
            
        * **Started on**: The date the schedule starts. The start date is required, and if you don't enter it, it is automatically set to the time at the time you saved the schedule.
        * **Ended on**: The date on which the schedule ends. If not set, the schedule will continue to run with the recurrence interval you entered.

4. Set the target for the schedule, then click **Next**.
    * **URL**: Enter the URL to call.
    * **HTTP Method**: Click the drop-down list to select an HTTP method.
    * **HTTP headers**: Click ** + Add** to enter HTTP headers. You can add up to 20 HTTP headers, and the total size of all headers you add can be up to 8 KB combined.
    * **Parameters**: Enter the body of the request. The Parameters field appears when you select the HTTP method as **POST**, **PUT**, or **PATCH**. The maximum parameter size you can enter is 256 KB.

5. After you complete the additional settings, click **Next**.
    * **Activate Schedule**: Select whether to activate the schedule.
    * **Retry policy**: You can set to retry a schedule run when it fails. When you select **set**, the **Retry interval** and **Maximum number of retries** fields are displayed.
        * If the API call fails, retry the schedule according to the retry policy you set.
        * The API success criteria are as follows
            * NHN Cloud service: If the HTTP Response Status Code is `200` and the value of `$.header.isSuccessful` is `true`
            * External service: HTTP Response Status Code is `2xx`
        * **Retry Interval**: Enter the interval to retry failed schedules. You can set a minimum of 1 minute and a maximum of 60 minutes.
        * **Maximum Number of Retries**: Enter the maximum number of retries. You can set a maximum of 5 retries.

6. In the **Final Review and Save** step, confirm the information you set up earlier and click **Create Schedule**.

!!! tip "Important"
    * Cron expressions are built with five fields, which are in the order "Minute Hour Day Month Day of Week".
    * The first start time of the Rate type can vary depending on the Rate interval you set.
    * It can take up to 30 seconds for the schedule you create to be reflected, so changes to the schedule contents, including activation/deactivation, may fail during that time.

!!! danger "Caution"
    If you select the recurrence type as **Rate**, the **started on** may be different from the actual schedule run time. See the [Schedule Execution Examples](create-schedule/#_3) to set it up correctly. 



## Schedule Execution Examples

When a schedule runs depends on the start and end dates you set, and what type of schedule you entered.
To help you understand, we'll show you an example of how a Cron and Rate schedule type would run with the same start and end dates.

* **Started on**: 2024-01-05 00:00:00
* **Ended on**: 2024-01-08 01:00:00
* For Cron schedules
    * **Cron expression**: 0 12 * * * (run every day at 12 noon)
    * First Schedule Execution Time
        * 2024-01-05 12:00:00
    * Last Schedule Execution Time
        * 2024-01-07 12:00:00
* For Rate schedules
    * **Rate**: Execute every 12 hours
    * First Schedule Execution Time
        * 2024-01-05 00:00:00
    * Last Schedule Execution Time
        * 2024-01-08 00:00:00