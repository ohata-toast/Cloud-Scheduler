# Cloud Scheduler Overview

**Application Service > Cloud Scheduler > Overview**

Cloud Scheduler allows you to set various tasks to run on a schedule of your choice. You can execute a specific task one-time on a set schedule, or you can set a cron expression or interval to run it repeatedly. Tasks can be set up through API endpoints. The API endpoint allows you to freely enter the APIs of various services, not just the preset NHN Cloud services. A typical example of a task using Cloud Scheduler is copying an object from NHN Cloud Object Storage repeatedly based on the interval you set.

Schedules you set up in Cloud Scheduler can run only during the time period you want by specifying start and end dates, and you can easily stop them from running by disabling them if you don't want them to run. You can also set retry policies to rerun a job if it doesn't complete successfully, for example, due to an API call failure.

Cloud Scheduler is available in all regions of NHN Cloud.


![Cloud Scheduler Over Image](https://static.toastoven.net/prod_cloud_scheduler/CloudScheduler_overview_ko_800.png)

<br>
This document guides you through the main features, how to use, and terminology of NHN Cloud's Cloud Scheduler service.

## Main Features

* **Various Execution Types**
    * Supports one-time execution, running only once at a specified point in time.
    * Supports Cron expressions and rate-based recurring execution.
* **Easy Schedule Management**
    * You can activate or deactivate schedules.
    * The schedule execution history gives you detailed information about success, request and response data, and more.
    * You can set retries when a task fails on a schedule.
* **Integration with NHN Cloud services** (coming soon)
    * Features of various NHN Cloud services are provided as target templates for easy schedule registration.
* **Create Target templates for APIs** (coming soon)
    * You can create target templates by directly inputting various APIs as well as NHN Cloud services.

## Get started with Cloud Scheduler

* [Create Schedule](create-schedule)
* [Manage Schedule](manage-schedule)

## Glossary


| Terms | Description |
| --- | --- |
| Schedule | A resource created using Cloud Scheduler, including additional settings such as execution type, target, and retry policy. |
| Cron | A UNIX-based job scheduler that allows tasks to run at regular time intervals or at specific times. Written via Cron expressions |