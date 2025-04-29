# Manage Template
**Application Service > Cloud Scheduler > Console User Guide > Manage Template**

Templates are a way to preset the execution information, audience information, and additional settings for schedules.
You can quickly create a schedule by selecting a template you've created.

This section describes the feature to create and manage templates.

!!! tip "Important"
    Date data is based on UTC+09:00.

## Create Template
Click **+ Create Template**.
Create a template in the same way creating a schedule. See [Create Schedule](create-schedule) to create a template.

!!! tip "Important"
    The template name is a required field, the other fields can be set as needed to create a template.

## Modify Template
Select a template to change template information, such as launch information and audience information. Select the template you want to change, then click **Modify Template**. See [Create Schedule](create-schedule) to change the template information.

## Delete Template
Select a template to delete. You can also delete multiple at the same time. Select the template you want to delete, then click **Delete Template**.

## Copy Template
Select a template you want to copy, then select **Copy Template** to copy it.
The template name and description are not copied. This is useful if you want to reuse a template that you've already created.

## View Template Information
You can select the template you're using to view template information in the bottom area of the screen.

* **Basic Info**: Show basic information about the schedule, including the name, description, status, and execution type.
* **Target Info**: Show the information about a target to run a schedule . Target information varies depending on the target type.
    * **Direct Input**: Show the URL, HTTP method, HTTP headers, and parameters to run.
    * **Target Template**: Show the information you entered for the target template to run.
* **Execution History**: Show when the schedule is executed, whether it succeeded or failed, whether it was retried, and the execution log.
    * Execution logs can be viewed for up to 30 days.
* **Additional Settings**: Check the retry policy information.