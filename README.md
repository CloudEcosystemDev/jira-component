# <p align="center" width="100%"> <img src="https://cdn.iconscout.com/icon/free/png-256/jira-282222.png" width="250" height="250"> </p> 
# <p align="center" width="100%"> The Jira Cloud platform REST API OIH Connector </p>

## Description

A generated OIH connector for the The Jira Cloud platform REST API API (version 1001.0.0-SNAPSHOT).

Generated from: https://developer.atlassian.com/cloud/jira/platform/swagger-v3.v3.json<br/>
Generated at: 2021-10-15T09:05:27+02:00

## API Description

Jira Cloud platform REST API documentation<br/>

## Authorization

Supported authorization schemes:
- Basic Authentication - You can access this resource via basic auth.
- OAuth2 - OAuth2 scopes for Jira

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Update custom field configurations
> Update the configuration for contexts of a custom field created by a [Forge app](https://developer.atlassian.com/platform/forge/).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg). Jira permissions are not required for the Forge app that created the custom field.<br/>

*Tags:* `Issue custom field configuration (apps)`

#### Input Parameters
* `fieldIdOrKey` - _required_ - The ID or key of the custom field, for example `customfield_10000`.<br/>

### Update custom field value
> Updates the value of a custom field on one or more issues. Custom fields can only be updated by the Forge app that created them.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only the app that created the custom field can update its values with this operation.<br/>

*Tags:* `Issue custom field values (apps)`

#### Input Parameters
* `fieldIdOrKey` - _required_ - The ID or key of the custom field. For example, `customfield_10010`.<br/>
* `generateChangelog` - _optional_ - Whether to generate a changelog for this update. Default: true.<br/>

### Set application property
> Changes the value of an application property. For example, you can change the value of the `jira.clone.prefix` from its default value of *CLONE -* to *Clone -* if you prefer sentence case capitalization. Editable properties are described below along with their default values.<br/>
> <br/>
> #### Advanced settings ####<br/>
> <br/>
> The advanced settings below are also accessible in [Jira](https://confluence.atlassian.com/x/vYXKM).<br/>
> <br/>
> | Key | Description | Default value |  <br/>
> | -- | -- | -- |  <br/>
> | `jira.clone.prefix` | The string of text prefixed to the title of a cloned issue. | `CLONE -` |  <br/>
> | `jira.date.picker.java.format` | The date format for the Java (server-side) generated dates. This must be the same as the `jira.date.picker.javascript.format` format setting. | `d/MMM/yy` |  <br/>
> | `jira.date.picker.javascript.format` | The date format for the JavaScript (client-side) generated dates. This must be the same as the `jira.date.picker.java.format` format setting. | `%e/%b/%y` |  <br/>
> | `jira.date.time.picker.java.format` | The date format for the Java (server-side) generated date times. This must be the same as the `jira.date.time.picker.javascript.format` format setting. | `dd/MMM/yy h:mm a` |  <br/>
> | `jira.date.time.picker.javascript.format` | The date format for the JavaScript (client-side) generated date times. This must be the same as the `jira.date.time.picker.java.format` format setting. | `%e/%b/%y %I:%M %p` |  <br/>
> | `jira.issue.actions.order` | The default order of actions (such as *Comments* or *Change history*) displayed on the issue view. | `asc` |  <br/>
> | `jira.table.cols.subtasks` | The columns to show while viewing subtask issues in a table. For example, a list of subtasks on an issue. | `issuetype, status, assignee, progress` |  <br/>
> | `jira.view.issue.links.sort.order` | The sort order of the list of issue links on the issue view. | `type, status, priority` |  <br/>
> | `jira.comment.collapsing.minimum.hidden` | The minimum number of comments required for comment collapsing to occur. A value of `0` disables comment collapsing. | `4` |  <br/>
> | `jira.newsletter.tip.delay.days` | The number of days before a prompt to sign up to the Jira Insiders newsletter is shown. A value of `-1` disables this feature. | `7` |  <br/>
> <br/>
> <br/>
> #### Look and feel ####<br/>
> <br/>
> The settings listed below adjust the [look and feel](https://confluence.atlassian.com/x/VwCLLg).<br/>
> <br/>
> | Key | Description | Default value |  <br/>
> | -- | -- | -- |  <br/>
> | `jira.lf.date.time` | The [ time format](https://docs.oracle.com/javase/6/docs/api/index.html?java/text/SimpleDateFormat.html). | `h:mm a` |  <br/>
> | `jira.lf.date.day` | The [ day format](https://docs.oracle.com/javase/6/docs/api/index.html?java/text/SimpleDateFormat.html). | `EEEE h:mm a` |  <br/>
> | `jira.lf.date.complete` | The [ date and time format](https://docs.oracle.com/javase/6/docs/api/index.html?java/text/SimpleDateFormat.html). | `dd/MMM/yy h:mm a` |  <br/>
> | `jira.lf.date.dmy` | The [ date format](https://docs.oracle.com/javase/6/docs/api/index.html?java/text/SimpleDateFormat.html). | `dd/MMM/yy` |  <br/>
> | `jira.date.time.picker.use.iso8061` | When enabled, sets Monday as the first day of the week in the date picker, as specified by the ISO8601 standard. | `false` |  <br/>
> | `jira.lf.logo.url` | The URL of the logo image file. | `/images/icon-jira-logo.png` |  <br/>
> | `jira.lf.logo.show.application.title` | Controls the visibility of the application title on the sidebar. | `false` |  <br/>
> | `jira.lf.favicon.url` | The URL of the favicon. | `/favicon.ico` |  <br/>
> | `jira.lf.favicon.hires.url` | The URL of the high-resolution favicon. | `/images/64jira.png` |  <br/>
> | `jira.lf.navigation.bgcolour` | The background color of the sidebar. | `#0747A6` |  <br/>
> | `jira.lf.navigation.highlightcolour` | The color of the text and logo of the sidebar. | `#DEEBFF` |  <br/>
> | `jira.lf.hero.button.base.bg.colour` | The background color of the hero button. | `#3b7fc4` |  <br/>
> | `jira.title` | The text for the application title. The application title can also be set in *General settings*. | `Jira` |  <br/>
> | `jira.option.globalsharing` | Whether filters and dashboards can be shared with anyone signed into Jira. | `true` |  <br/>
> | `xflow.product.suggestions.enabled` | Whether to expose product suggestions for other Atlassian products within Jira. | `true` |  <br/>
> <br/>
> <br/>
> #### Other settings ####<br/>
> <br/>
> | Key | Description | Default value |  <br/>
> | -- | -- | -- |  <br/>
> | `jira.issuenav.criteria.autoupdate` | Whether instant updates to search criteria is active. | `true` |  <br/>
> <br/>
> <br/>
> *Note: Be careful when changing [application properties and advanced settings](https://confluence.atlassian.com/x/vYXKM).*<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Jira settings`

#### Input Parameters
* `id` - _required_ - The key of the application property to update.<br/>

### Get application role
> Returns an application role.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Application roles`

#### Input Parameters
* `key` - _required_ - The key of the application role. Use the [Get all application roles](#api-rest-api-3-applicationrole-get) operation to get the key for each application role.<br/>

### Get attachment metadata
> Returns the metadata for an attachment. Note that the attachment itself is not returned.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue attachments`

#### Input Parameters
* `id` - _required_ - The ID of the attachment.<br/>

### Delete attachment
> Deletes an attachment from an issue.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** For the project holding the issue containing the attachment:<br/>
> <br/>
>  *  *Delete own attachments* [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment created by the calling user.<br/>
>  *  *Delete all attachments* [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment created by any user.<br/>

*Tags:* `Issue attachments`

#### Input Parameters
* `id` - _required_ - The ID of the attachment.<br/>

### Get comments by IDs
> Returns a [paginated](#pagination) list of comments specified by a list of comment IDs.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** Comments are returned where the user:<br/>
> <br/>
>  *  has *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the comment.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the comment has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue comments`

#### Input Parameters
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about comments in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `renderedBody` Returns the comment body rendered in HTML.<br/>
 *  `properties` Returns the comment's properties.<br/>

### Get comment property
> Returns the value of a comment property.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the comment has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue comment properties`

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Set comment property
> Creates or updates the value of a property for a comment. Use this resource to store custom data against a comment.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> **[Permissions](#permissions) required:** either of:<br/>
> <br/>
>  *  *Edit All Comments* [project permission](https://confluence.atlassian.com/x/yodKLg) to create or update the value of a property on any comment.<br/>
>  *  *Edit Own Comments* [project permission](https://confluence.atlassian.com/x/yodKLg) to create or update the value of a property on a comment created by the user.<br/>
> <br/>
> Also, when the visibility of a comment is restricted to a role or group the user must be a member of that role or group.<br/>

*Tags:* `Issue comment properties`

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.<br/>
* `propertyKey` - _required_ - The key of the property. The maximum length is 255 characters.<br/>

### Delete comment property
> Deletes a comment property.<br/>
> <br/>
> **[Permissions](#permissions) required:** either of:<br/>
> <br/>
>  *  *Edit All Comments* [project permission](https://confluence.atlassian.com/x/yodKLg) to delete a property from any comment.<br/>
>  *  *Edit Own Comments* [project permission](https://confluence.atlassian.com/x/yodKLg) to delete a property from a comment created by the user.<br/>
> <br/>
> Also, when the visibility of a comment is restricted to a role or group the user must be a member of that role or group.<br/>

*Tags:* `Issue comment properties`

#### Input Parameters
* `commentId` - _required_ - The ID of the comment.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Create component
> Creates a component. Use components to provide containers for issues within a project.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project in which the component is created or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project components`

### Get component
> Returns a component.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for project containing the component.<br/>

*Tags:* `Project components`

#### Input Parameters
* `id` - _required_ - The ID of the component.<br/>

### Update component
> Updates a component. Any fields included in the request are overwritten. If `leadAccountId` is an empty string ("") the component lead is removed.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the component or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project components`

#### Input Parameters
* `id` - _required_ - The ID of the component.<br/>

### Delete component
> Deletes a component.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the component or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project components`

#### Input Parameters
* `id` - _required_ - The ID of the component.<br/>
* `moveIssuesTo` - _optional_ - The ID of the component to replace the deleted component. If this value is null no replacement is made.<br/>

### Select time tracking provider
> Selects a time tracking provider.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Time tracking`

### Set time tracking settings
> Sets the time tracking settings.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Time tracking`

### Get custom field option
> Returns a custom field option. For example, an option in a select list.<br/>
> <br/>
> Note that this operation **only works for issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource**, it cannot be used with issue field select list options created by Connect apps.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** The custom field option is returned as follows:<br/>
> <br/>
>  *  if the user has the *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>
>  *  if the user has the *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for at least one project the custom field is used in, and the field is visible in at least one layout the user has permission to view.<br/>

*Tags:* `Issue custom field options`

#### Input Parameters
* `id` - _required_ - The ID of the custom field option.<br/>

### Create dashboard
> Creates a dashboard.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `Dashboards`

### Get dashboard item property
> Returns the key and value of a dashboard item property.<br/>
> <br/>
> A dashboard item enables an app to add user-specific information to a user dashboard. Dashboard items are exposed to users as gadgets that users can add to their dashboards. For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).<br/>
> <br/>
> When an app creates a dashboard item it registers a callback to receive the dashboard item ID. The callback fires whenever the item is rendered or, where the item is configurable, the user edits the item. The app then uses this resource to store the item's content or configuration details. For more information on working with dashboard items, see [ Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/) and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/) documentation.<br/>
> <br/>
> There is no resource to set or get dashboard items.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** The user must be the owner of the dashboard or have the dashboard shared with them. Note, users with the *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) are considered owners of the System dashboard. The System dashboard is considered to be shared with all other users, and is accessible to anonymous users when Jira's anonymous access is permitted.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.<br/>
* `itemId` - _required_ - The ID of the dashboard item.<br/>
* `propertyKey` - _required_ - The key of the dashboard item property.<br/>

### Set dashboard item property
> Sets the value of a dashboard item property. Use this resource in apps to store custom data against a dashboard item.<br/>
> <br/>
> A dashboard item enables an app to add user-specific information to a user dashboard. Dashboard items are exposed to users as gadgets that users can add to their dashboards. For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).<br/>
> <br/>
> When an app creates a dashboard item it registers a callback to receive the dashboard item ID. The callback fires whenever the item is rendered or, where the item is configurable, the user edits the item. The app then uses this resource to store the item's content or configuration details. For more information on working with dashboard items, see [ Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/) and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/) documentation.<br/>
> <br/>
> There is no resource to set or get dashboard items.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** The user must be the owner of the dashboard. Note, users with the *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) are considered owners of the System dashboard.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.<br/>
* `itemId` - _required_ - The ID of the dashboard item.<br/>
* `propertyKey` - _required_ - The key of the dashboard item property. The maximum length is 255 characters.<br/>

### Delete dashboard item property
> Deletes a dashboard item property.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** The user must be the owner of the dashboard. Note, users with the *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) are considered owners of the System dashboard.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `dashboardId` - _required_ - The ID of the dashboard.<br/>
* `itemId` - _required_ - The ID of the dashboard item.<br/>
* `propertyKey` - _required_ - The key of the dashboard item property.<br/>

### Get dashboard
> Returns a dashboard.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>
> <br/>
> However, to get a dashboard, the dashboard must be shared with the user or the user must own it. Note, users with the *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) are considered owners of the System dashboard. The System dashboard is considered to be shared with all other users.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `id` - _required_ - The ID of the dashboard.<br/>

### Update dashboard
> Updates a dashboard, replacing all the dashboard details with those provided.<br/>
> <br/>
> **[Permissions](#permissions) required:** None<br/>
> <br/>
> The dashboard to be updated must be owned by the user.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `id` - _required_ - The ID of the dashboard to update.<br/>

### Delete dashboard
> Deletes a dashboard.<br/>
> <br/>
> **[Permissions](#permissions) required:** None<br/>
> <br/>
> The dashboard to be deleted must be owned by the user.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `id` - _required_ - The ID of the dashboard.<br/>

### Copy dashboard
> Copies a dashboard. Any values provided in the `dashboard` parameter replace those in the copied dashboard.<br/>
> <br/>
> **[Permissions](#permissions) required:** None<br/>
> <br/>
> The dashboard to be copied must be owned by or shared with the user.<br/>

*Tags:* `Dashboards`

#### Input Parameters
* `id` - _required_

### Analyse Jira expression
> Analyses and validates Jira expressions.<br/>
> <br/>
> As an experimental feature, this operation can also attempt to type-check the expressions.<br/>
> <br/>
> Learn more about Jira expressions in the [documentation](https://developer.atlassian.com/cloud/jira/platform/jira-expressions/).<br/>
> <br/>
> **[Permissions](#permissions) required**: None.<br/>

*Tags:* `Jira expressions`

#### Input Parameters
* `check` - _optional_ - The check to perform:<br/>
<br/>
 *  `syntax` Each expression's syntax is checked to ensure the expression can be parsed. Also, syntactic limits are validated. For example, the expression's length.<br/>
 *  `type` EXPERIMENTAL. Each expression is type checked and the final type of the expression inferred. Any type errors that would result in the expression failure at runtime are reported. For example, accessing properties that don't exist or passing the wrong number of arguments to functions. Also performs the syntax check.<br/>
 *  `complexity` EXPERIMENTAL. Determines the formulae for how many [expensive operations](https://developer.atlassian.com/cloud/jira/platform/jira-expressions/#expensive-operations) each expression may execute.<br/>
    Possible values: syntax, type, complexity.

### Evaluate Jira expression
> Evaluates a Jira expression and returns its value.<br/>
> <br/>
> This resource can be used to test Jira expressions that you plan to use elsewhere, or to fetch data in a flexible way. Consult the [Jira expressions documentation](https://developer.atlassian.com/cloud/jira/platform/jira-expressions/) for more details.<br/>
> <br/>
> #### Context variables ####<br/>
> <br/>
> The following context variables are available to Jira expressions evaluated by this resource. Their presence depends on various factors; usually you need to manually request them in the context object sent in the payload, but some of them are added automatically under certain conditions.<br/>
> <br/>
>  *  `user` ([User](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#user)): The current user. Always available and equal to `null` if the request is anonymous.<br/>
>  *  `app` ([App](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#app)): The [Connect app](https://developer.atlassian.com/cloud/jira/platform/index/#connect-apps) that made the request. Available only for authenticated requests made by Connect Apps (read more here: [Authentication for Connect apps](https://developer.atlassian.com/cloud/jira/platform/security-for-connect-apps/)).<br/>
>  *  `issue` ([Issue](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#issue)): The current issue. Available only when the issue is provided in the request context object.<br/>
>  *  `issues` ([List](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#list) of [Issues](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#issue)): A collection of issues matching a JQL query. Available only when JQL is provided in the request context object.<br/>
>  *  `project` ([Project](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#project)): The current project. Available only when the project is provided in the request context object.<br/>
>  *  `sprint` ([Sprint](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#sprint)): The current sprint. Available only when the sprint is provided in the request context object.<br/>
>  *  `board` ([Board](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#board)): The current board. Available only when the board is provided in the request context object.<br/>
>  *  `serviceDesk` ([ServiceDesk](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#servicedesk)): The current service desk. Available only when the service desk is provided in the request context object.<br/>
>  *  `customerRequest` ([CustomerRequest](https://developer.atlassian.com/cloud/jira/platform/jira-expressions-type-reference#customerrequest)): The current customer request. Available only when the customer request is provided in the request context object.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required**: None. However, an expression may return different results for different users depending on their permissions. For example, different users may see different comments on the same issue.  <br/>
> Permission to access Jira Software is required to access Jira Software context variables (`board` and `sprint`) or fields (for example, `issue.sprint`).<br/>

*Tags:* `Jira expressions`

#### Input Parameters
* `expand` - _optional_ - Use [expand](#expansion) to include additional information in the response. This parameter accepts `meta.complexity` that returns information about the expression complexity. For example, the number of expensive operations used by the expression and how close the expression is to reaching the [complexity limit](https://developer.atlassian.com/cloud/jira/platform/jira-expressions/#restrictions). Useful when designing and debugging your expressions.<br/>

### Create custom field
> Creates a custom field.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue fields`

### Update custom field
> Updates a custom field.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue fields`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>

### Create custom field context
> Creates a custom field context.<br/>
> <br/>
> If `projectIds` is empty, a global context is created. A global context is one that applies to all project. If `issueTypeIds` is empty, the context applies to all issue types.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>

### Set custom field contexts default values
> Sets default for contexts of a custom field. Default are defined using these objects:<br/>
> <br/>
>  *  `CustomFieldContextDefaultValueDate` (type `datepicker`) for date fields.<br/>
>  *  `CustomFieldContextDefaultValueDateTime` (type `datetimepicker`) for date-time fields.<br/>
>  *  `CustomFieldContextDefaultValueSingleOption` (type `option.single`) for single choice select lists and radio buttons.<br/>
>  *  `CustomFieldContextDefaultValueMultipleOption` (type `option.multiple`) for multiple choice select lists and checkboxes.<br/>
>  *  `CustomFieldContextDefaultValueCascadingOption` (type `option.cascading`) for cascading select lists.<br/>
>  *  `CustomFieldContextSingleUserPickerDefaults` (type `single.user.select`) for single users.<br/>
>  *  `CustomFieldContextDefaultValueMultiUserPicker` (type `multi.user.select`) for user lists.<br/>
>  *  `CustomFieldContextDefaultValueSingleGroupPicker` (type `grouppicker.single`) for single choice group picker.<br/>
>  *  `CustomFieldContextDefaultValueMultipleGroupPicker` (type `grouppicker.multiple`) for multiple choice group picker.<br/>
> <br/>
> Only one type of default object can be included in a request. To remove a default for a context, set the default parameter to `null`.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>

### Get custom field contexts for projects and issue types
> Returns a [paginated](#pagination) list of project and issue type mappings and, for each mapping, the ID of a [custom field context](https://confluence.atlassian.com/x/k44fOw) that applies to the project and issue type.<br/>
> <br/>
> If there is no custom field context assigned to the project then, if present, the custom field context that applies to all projects is returned if it also applies to the issue type or all issue types. If a custom field context is not found, the returned custom field context ID is `null`.<br/>
> <br/>
> Duplicate project and issue type mappings cannot be provided in the request.<br/>
> <br/>
> The order of the returned values is the same as provided in the request.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `startAt` - _optional_ - The index of the first item to return in a page of results (page offset).<br/>
* `maxResults` - _optional_ - The maximum number of items to return per page.<br/>

### Update custom field context
> Updates a [ custom field context](https://confluence.atlassian.com/adminjiracloud/what-are-custom-field-contexts-991923859.html).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Delete custom field context
> Deletes a [ custom field context](https://confluence.atlassian.com/adminjiracloud/what-are-custom-field-contexts-991923859.html).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Add issue types to context
> Adds issue types to a custom field context, appending the issue types to the issue types list.<br/>
> <br/>
> A custom field context without any issue types applies to all issue types. Adding issue types to such a custom field context would result in it applying to only the listed issue types.<br/>
> <br/>
> If any of the issue types exists in the custom field context, the operation fails and no issue types are added.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Remove issue types from context
> Removes issue types from a custom field context.<br/>
> <br/>
> A custom field context without any issue types applies to all issue types.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Update custom field options (context)
> Updates the options of a custom field.<br/>
> <br/>
> If any of the options are not found, no options are updated. Options where the values in the request match the current values aren't updated and aren't reported in the response.<br/>
> <br/>
> Note that this operation **only works for issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource**, it cannot be used with issue field select list options created by Connect apps.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field options`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Create custom field options (context)
> Creates options and, where the custom select field is of the type Select List (cascading), cascading options for a custom select field. The options are added to a context of the field.<br/>
> <br/>
> The maximum number of options that can be created per request is 1000 and each field can have a maximum of 10000 options.<br/>
> <br/>
> This operation works for custom field options created in Jira or the operations from this resource. **To work with issue field select list options created for Connect apps use the [Issue custom field options (apps)](#api-group-issue-custom-field-options--apps-) operations.**<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field options`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Reorder custom field options (context)
> Changes the order of custom field options or cascading options in a context.<br/>
> <br/>
> This operation works for custom field options created in Jira or the operations from this resource. **To work with issue field select list options created for Connect apps use the [Issue custom field options (apps)](#api-group-issue-custom-field-options--apps-) operations.**<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field options`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Delete custom field options (context)
> Deletes a custom field option.<br/>
> <br/>
> Options with cascading options cannot be deleted without deleting the cascading options first.<br/>
> <br/>
> This operation works for custom field options created in Jira or the operations from this resource. **To work with issue field select list options created for Connect apps use the [Issue custom field options (apps)](#api-group-issue-custom-field-options--apps-) operations.**<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field options`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context from which an option should be deleted.<br/>
* `optionId` - _required_ - The ID of the option to delete.<br/>

### Assign custom field context to projects
> Assigns a custom field context to projects.<br/>
> <br/>
> If any project in the request is assigned to any context of the custom field, the operation fails.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Remove custom field context from projects
> Removes a custom field context from projects.<br/>
> <br/>
> A custom field context without any projects applies to all projects. Removing all projects from a custom field context would result in it applying to all projects.<br/>
> <br/>
> If any project in the request is not assigned to the context, or the operation would result in two global contexts for the field, the operation fails.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue custom field contexts`

#### Input Parameters
* `fieldId` - _required_ - The ID of the custom field.<br/>
* `contextId` - _required_ - The ID of the context.<br/>

### Create issue field option
> Creates an option for a select list issue field.<br/>
> <br/>
> Note that this operation **only works for issue field select list options added by Connect apps**, it cannot be used with issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg). Jira permissions are not required for the app providing the field.<br/>

*Tags:* `Issue custom field options (apps)`

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: **$(app-key)\_\_$(field-key)**. For example, *example-add-on\_\_example-issue-field*. To determine the `fieldKey` value, do one of the following:<br/>
<br/>
 *  open the app's plugin descriptor, then **app-key** is the key at the top and **field-key** is the key in the `jiraIssueFields` module. **app-key** can also be found in the app listing in the Atlassian Universal Plugin Manager.<br/>
 *  run [Get fields](#api-rest-api-3-field-get) and in the field details the value is returned in `key`. For example, `"key": "teams-add-on__team-issue-field"`<br/>

### Get issue field option
> Returns an option from a select list issue field.<br/>
> <br/>
> Note that this operation **only works for issue field select list options added by Connect apps**, it cannot be used with issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg). Jira permissions are not required for the app providing the field.<br/>

*Tags:* `Issue custom field options (apps)`

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: **$(app-key)\_\_$(field-key)**. For example, *example-add-on\_\_example-issue-field*. To determine the `fieldKey` value, do one of the following:<br/>
<br/>
 *  open the app's plugin descriptor, then **app-key** is the key at the top and **field-key** is the key in the `jiraIssueFields` module. **app-key** can also be found in the app listing in the Atlassian Universal Plugin Manager.<br/>
 *  run [Get fields](#api-rest-api-3-field-get) and in the field details the value is returned in `key`. For example, `"key": "teams-add-on__team-issue-field"`<br/>
* `optionId` - _required_ - The ID of the option to be returned.<br/>

### Update issue field option
> Updates or creates an option for a select list issue field. This operation requires that the option ID is provided when creating an option, therefore, the option ID needs to be specified as a path and body parameter. The option ID provided in the path and body must be identical.<br/>
> <br/>
> Note that this operation **only works for issue field select list options added by Connect apps**, it cannot be used with issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg). Jira permissions are not required for the app providing the field.<br/>

*Tags:* `Issue custom field options (apps)`

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: **$(app-key)\_\_$(field-key)**. For example, *example-add-on\_\_example-issue-field*. To determine the `fieldKey` value, do one of the following:<br/>
<br/>
 *  open the app's plugin descriptor, then **app-key** is the key at the top and **field-key** is the key in the `jiraIssueFields` module. **app-key** can also be found in the app listing in the Atlassian Universal Plugin Manager.<br/>
 *  run [Get fields](#api-rest-api-3-field-get) and in the field details the value is returned in `key`. For example, `"key": "teams-add-on__team-issue-field"`<br/>
* `optionId` - _required_ - The ID of the option to be updated.<br/>

### Delete issue field option
> Deletes an option from a select list issue field.<br/>
> <br/>
> Note that this operation **only works for issue field select list options added by Connect apps**, it cannot be used with issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg). Jira permissions are not required for the app providing the field.<br/>

*Tags:* `Issue custom field options (apps)`

#### Input Parameters
* `fieldKey` - _required_ - The field key is specified in the following format: **$(app-key)\_\_$(field-key)**. For example, *example-add-on\_\_example-issue-field*. To determine the `fieldKey` value, do one of the following:<br/>
<br/>
 *  open the app's plugin descriptor, then **app-key** is the key at the top and **field-key** is the key in the `jiraIssueFields` module. **app-key** can also be found in the app listing in the Atlassian Universal Plugin Manager.<br/>
 *  run [Get fields](#api-rest-api-3-field-get) and in the field details the value is returned in `key`. For example, `"key": "teams-add-on__team-issue-field"`<br/>
* `optionId` - _required_ - The ID of the option to be deleted.<br/>

### Replace issue field option
> Deselects an issue-field select-list option from all issues where it is selected. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.<br/>
> <br/>
> Connect app users with admin permissions (from user permissions and app scopes) and Forge app users with the `manage:jira-configuration` scope can override the screen security configuration using `overrideScreenSecurity` and `overrideEditableFlag`.<br/>
> <br/>
> This is an [asynchronous operation](#async). The response object contains a link to the long-running task.<br/>
> <br/>
> Note that this operation **only works for issue field select list options added by Connect apps**, it cannot be used with issue field select list options created in Jira or using operations from the [Issue custom field options](#api-group-Issue-custom-field-options) resource.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg). Jira permissions are not required for the app providing the field.<br/>

*Tags:* `Issue custom field options (apps)`

#### Input Parameters
* `replaceWith` - _optional_ - The ID of the option that will replace the currently selected option.<br/>
* `jql` - _optional_ - A JQL query that specifies the issues to be updated. For example, *project=10000*.<br/>
* `overrideScreenSecurity` - _optional_ - Whether screen security is overridden to enable hidden fields to be edited. Available to Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope.<br/>
* `overrideEditableFlag` - _optional_ - Whether screen security is overridden to enable uneditable fields to be edited. Available to Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope.<br/>
* `fieldKey` - _required_ - The field key is specified in the following format: **$(app-key)\_\_$(field-key)**. For example, *example-add-on\_\_example-issue-field*. To determine the `fieldKey` value, do one of the following:<br/>
<br/>
 *  open the app's plugin descriptor, then **app-key** is the key at the top and **field-key** is the key in the `jiraIssueFields` module. **app-key** can also be found in the app listing in the Atlassian Universal Plugin Manager.<br/>
 *  run [Get fields](#api-rest-api-3-field-get) and in the field details the value is returned in `key`. For example, `"key": "teams-add-on__team-issue-field"`<br/>
* `optionId` - _required_ - The ID of the option to be deselected.<br/>

### Delete custom field
> Deletes a custom field. The custom field is deleted whether it is in the trash or not. See [Edit or delete a custom field](https://confluence.atlassian.com/x/Z44fOw) for more information on trashing and deleting custom fields.<br/>
> <br/>
> This operation is [asynchronous](#async). Follow the `location` link in the response to determine the status of the task and use [Get task](#api-rest-api-3-task-taskId-get) to obtain subsequent updates.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue fields`

#### Input Parameters
* `id` - _required_ - The ID of a custom field.<br/>

### Restore custom field from trash
> Restores a custom field from trash. See [Edit or delete a custom field](https://confluence.atlassian.com/x/Z44fOw) for more information on trashing and deleting custom fields.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue fields`

#### Input Parameters
* `id` - _required_ - The ID of a custom field.<br/>

### Move custom field to trash
> Moves a custom field to trash. See [Edit or delete a custom field](https://confluence.atlassian.com/x/Z44fOw) for more information on trashing and deleting custom fields.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue fields`

#### Input Parameters
* `id` - _required_ - The ID of a custom field.<br/>

### Create field configuration
> Creates a field configuration. The field configuration is created with the same field properties as the default configuration, with all the fields being optional.<br/>
> <br/>
> This operation can only to create configurations for use in classic projects.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue field configurations`

### Assign field configuration scheme to project
> Assigns a field configuration scheme to a project. If the field configuration scheme ID is `null`, the operation assigns the default field configuration scheme.<br/>
> <br/>
> Field configuration schemes can only be assigned to classic projects.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue field configurations`

### Create filter
> Creates a filter. The filter is shared according to the [default share scope](#api-rest-api-3-filter-post). The filter is not selected as a favorite.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Filters`

#### Input Parameters
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about filter in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `sharedUsers` Returns the users that the filter is shared with. This includes users that can browse projects that the filter is shared with. If you don't specify `sharedUsers`, then the `sharedUsers` object is returned but it doesn't list any users. The list of users returned is limited to 1000, to access additional users append `[start-index:end-index]` to the expand request. For example, to access the next 1000 users, use `?expand=sharedUsers[1001:2000]`.<br/>
 *  `subscriptions` Returns the users that are subscribed to the filter. If you don't specify `subscriptions`, the `subscriptions` object is returned but it doesn't list any subscriptions. The list of subscriptions returned is limited to 1000, to access additional subscriptions append `[start-index:end-index]` to the expand request. For example, to access the next 1000 subscriptions, use `?expand=subscriptions[1001:2000]`.<br/>

### Set default share scope
> Sets the default sharing for new filters and dashboards for a user.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Filter sharing`

### Get filter
> Returns a filter.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None, however, the filter is only returned where it is:<br/>
> <br/>
>  *  owned by the user.<br/>
>  *  shared with a group that the user is a member of.<br/>
>  *  shared with a private project that the user has *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for.<br/>
>  *  shared with a public project.<br/>
>  *  shared with the public.<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter to return.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about filter in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `sharedUsers` Returns the users that the filter is shared with. This includes users that can browse projects that the filter is shared with. If you don't specify `sharedUsers`, then the `sharedUsers` object is returned but it doesn't list any users. The list of users returned is limited to 1000, to access additional users append `[start-index:end-index]` to the expand request. For example, to access the next 1000 users, use `?expand=sharedUsers[1001:2000]`.<br/>
 *  `subscriptions` Returns the users that are subscribed to the filter. If you don't specify `subscriptions`, the `subscriptions` object is returned but it doesn't list any subscriptions. The list of subscriptions returned is limited to 1000, to access additional subscriptions append `[start-index:end-index]` to the expand request. For example, to access the next 1000 subscriptions, use `?expand=subscriptions[1001:2000]`.<br/>

### Update filter
> Updates a filter. Use this operation to update a filter's name, description, JQL, or sharing.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however the user must own the filter.<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter to update.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about filter in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `sharedUsers` Returns the users that the filter is shared with. This includes users that can browse projects that the filter is shared with. If you don't specify `sharedUsers`, then the `sharedUsers` object is returned but it doesn't list any users. The list of users returned is limited to 1000, to access additional users append `[start-index:end-index]` to the expand request. For example, to access the next 1000 users, use `?expand=sharedUsers[1001:2000]`.<br/>
 *  `subscriptions` Returns the users that are subscribed to the filter. If you don't specify `subscriptions`, the `subscriptions` object is returned but it doesn't list any subscriptions. The list of subscriptions returned is limited to 1000, to access additional subscriptions append `[start-index:end-index]` to the expand request. For example, to access the next 1000 subscriptions, use `?expand=subscriptions[1001:2000]`.<br/>

### Delete filter
> Delete a filter.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however filters can only be deleted by the creator of the filter or a user with *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter to delete.<br/>

### Set columns
> Sets the columns for a filter. Only navigable fields can be set as columns. Use [Get fields](#api-rest-api-3-field-get) to get the list fields in Jira. A navigable field has `navigable` set to `true`.<br/>
> <br/>
> The parameters for this resource are expressed as HTML form data. For example, in curl:<br/>
> <br/>
> `curl -X PUT -d columns=summary -d columns=description https://your-domain.atlassian.net/rest/api/3/filter/10000/columns`<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however, columns are only set for:<br/>
> <br/>
>  *  filters owned by the user.<br/>
>  *  filters shared with a group that the user is a member of.<br/>
>  *  filters shared with a private project that the user has *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for.<br/>
>  *  filters shared with a public project.<br/>
>  *  filters shared with the public.<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>

### Reset columns
> Reset the user's column configuration for the filter to the default.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however, columns are only reset for:<br/>
> <br/>
>  *  filters owned by the user.<br/>
>  *  filters shared with a group that the user is a member of.<br/>
>  *  filters shared with a private project that the user has *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for.<br/>
>  *  filters shared with a public project.<br/>
>  *  filters shared with the public.<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>

### Add filter as favorite
> Add a filter as a favorite for the user.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however, the user can only favorite:<br/>
> <br/>
>  *  filters owned by the user.<br/>
>  *  filters shared with a group that the user is a member of.<br/>
>  *  filters shared with a private project that the user has *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for.<br/>
>  *  filters shared with a public project.<br/>
>  *  filters shared with the public.<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about filter in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `sharedUsers` Returns the users that the filter is shared with. This includes users that can browse projects that the filter is shared with. If you don't specify `sharedUsers`, then the `sharedUsers` object is returned but it doesn't list any users. The list of users returned is limited to 1000, to access additional users append `[start-index:end-index]` to the expand request. For example, to access the next 1000 users, use `?expand=sharedUsers[1001:2000]`.<br/>
 *  `subscriptions` Returns the users that are subscribed to the filter. If you don't specify `subscriptions`, the `subscriptions` object is returned but it doesn't list any subscriptions. The list of subscriptions returned is limited to 1000, to access additional subscriptions append `[start-index:end-index]` to the expand request. For example, to access the next 1000 subscriptions, use `?expand=subscriptions[1001:2000]`.<br/>

### Remove filter as favorite
> Removes a filter as a favorite for the user. Note that this operation only removes filters visible to the user from the user's favorites list. For example, if the user favorites a public filter that is subsequently made private (and is therefore no longer visible on their favorites list) they cannot remove it from their favorites list.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Filters`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about filter in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `sharedUsers` Returns the users that the filter is shared with. This includes users that can browse projects that the filter is shared with. If you don't specify `sharedUsers`, then the `sharedUsers` object is returned but it doesn't list any users. The list of users returned is limited to 1000, to access additional users append `[start-index:end-index]` to the expand request. For example, to access the next 1000 users, use `?expand=sharedUsers[1001:2000]`.<br/>
 *  `subscriptions` Returns the users that are subscribed to the filter. If you don't specify `subscriptions`, the `subscriptions` object is returned but it doesn't list any subscriptions. The list of subscriptions returned is limited to 1000, to access additional subscriptions append `[start-index:end-index]` to the expand request. For example, to access the next 1000 subscriptions, use `?expand=subscriptions[1001:2000]`.<br/>

### Add share permission
> Add a share permissions to a filter. If you add a global share permission (one for all logged-in users or the public) it will overwrite all share permissions for the filter.<br/>
> <br/>
> Be aware that this operation uses different objects for updating share permissions compared to [Update filter](#api-rest-api-3-filter-id-put).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Share dashboards and filters* [global permission](https://confluence.atlassian.com/x/x4dKLg) and the user must own the filter.<br/>

*Tags:* `Filter sharing`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>

### Get share permission
> Returns a share permission for a filter. A filter can be shared with groups, projects, all logged-in users, or the public. Sharing with all logged-in users or the public is known as a global share permission.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None, however, a share permission is only returned for:<br/>
> <br/>
>  *  filters owned by the user.<br/>
>  *  filters shared with a group that the user is a member of.<br/>
>  *  filters shared with a private project that the user has *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for.<br/>
>  *  filters shared with a public project.<br/>
>  *  filters shared with the public.<br/>

*Tags:* `Filter sharing`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>
* `permissionId` - _required_ - The ID of the share permission.<br/>

### Delete share permission
> Deletes a share permission from a filter.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira and the user must own the filter.<br/>

*Tags:* `Filter sharing`

#### Input Parameters
* `id` - _required_ - The ID of the filter.<br/>
* `permissionId` - _required_ - The ID of the share permission.<br/>

### Create group
> Creates a group.<br/>
> <br/>
> **[Permissions](#permissions) required:** Site administration (that is, member of the *site-admin* [group](https://confluence.atlassian.com/x/24xjL)).<br/>

*Tags:* `Groups`

### Remove group
> Deletes a group.<br/>
> <br/>
> **[Permissions](#permissions) required:** Site administration (that is, member of the *site-admin* strategic [group](https://confluence.atlassian.com/x/24xjL)).<br/>

*Tags:* `Groups`

#### Input Parameters
* `groupname` - _required_ - The name of the group.<br/>
* `swapGroup` - _optional_ - The group to transfer restrictions to. Only comments and worklogs are transferred. If restrictions are not transferred, comments and worklogs are inaccessible after the deletion.<br/>

### Add user to group
> Adds a user to a group.<br/>
> <br/>
> **[Permissions](#permissions) required:** Site administration (that is, member of the *site-admin* [group](https://confluence.atlassian.com/x/24xjL)).<br/>

*Tags:* `Groups`

#### Input Parameters
* `groupname` - _required_ - The name of the group (case sensitive).<br/>

### Remove user from group
> Removes a user from a group.<br/>
> <br/>
> **[Permissions](#permissions) required:** Site administration (that is, member of the *site-admin* [group](https://confluence.atlassian.com/x/24xjL)).<br/>

*Tags:* `Groups`

#### Input Parameters
* `groupname` - _required_ - The name of the group.<br/>
* `username` - _optional_ - This parameter is no longer available. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `accountId` - _required_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>

### Create issue
> Creates an issue or, where the option to create subtasks is enabled in Jira, a subtask. A transition may be applied, to move the issue or subtask to a workflow step other than the default start step, and issue properties set.<br/>
> <br/>
> The content of the issue or subtask is defined using `update` and `fields`. The fields that can be set in the issue or subtask are determined using the [ Get create issue metadata](#api-rest-api-3-issue-createmeta-get). These are the same fields that appear on the issue's create screen. Note that the `description`, `environment`, and any `textarea` type custom fields (multi-line text fields) take Atlassian Document Format content. Single line custom fields (`textfield`) accept a string and don't handle Atlassian Document Format content.<br/>
> <br/>
> Creating a subtask differs from creating an issue as follows:<br/>
> <br/>
>  *  `issueType` must be set to a subtask issue type (use [ Get create issue metadata](#api-rest-api-3-issue-createmeta-get) to find subtask issue types).<br/>
>  *  `parent` must contain the ID or key of the parent issue.<br/>
> <br/>
> In a next-gen project any issue may be made a child providing that the parent and child are members of the same project. In a classic project the parent field is only valid for subtasks.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* and *Create issues* [project permissions](https://confluence.atlassian.com/x/yodKLg) for the project in which the issue or subtask is created.<br/>

*Tags:* `Issues`

#### Input Parameters
* `updateHistory` - _optional_ - Whether the project in which the issue is created is added to the user's **Recently viewed** project list, as shown under **Projects** in Jira. When provided, the issue type and request type are added to the user's history for a project. These values are then used to provide defaults on the issue create screen.<br/>

### Bulk create issue
> Creates issues and, where the option to create subtasks is enabled in Jira, subtasks. Transitions may be applied, to move the issues or subtasks to a workflow step other than the default start step, and issue properties set.<br/>
> <br/>
> The content of each issue or subtask is defined using `update` and `fields`. The fields that can be set in the issue or subtask are determined using the [ Get create issue metadata](#api-rest-api-3-issue-createmeta-get). These are the same fields that appear on the issues' create screens. Note that the `description`, `environment`, and any `textarea` type custom fields (multi-line text fields) take Atlassian Document Format content. Single line custom fields (`textfield`) accept a string and don't handle Atlassian Document Format content.<br/>
> <br/>
> Creating a subtask differs from creating an issue as follows:<br/>
> <br/>
>  *  `issueType` must be set to a subtask issue type (use [ Get create issue metadata](#api-rest-api-3-issue-createmeta-get) to find subtask issue types).<br/>
>  *  `parent` the must contain the ID or key of the parent issue.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* and *Create issues* [project permissions](https://confluence.atlassian.com/x/yodKLg) for the project in which each issue or subtask is created.<br/>

*Tags:* `Issues`

### Bulk set issues properties
> Sets the values of entity properties on issues. It can set up to 10 entity properties on up to 10,000 issues.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON. The maximum length of single issue property value is 32768 characters. This operation can be accessed anonymously.<br/>
> <br/>
> This operation is:<br/>
> <br/>
>  *  transactional, either all properties are updated in all eligible issues or, when errors occur, no properties are updated.<br/>
>  *  [asynchronous](#async). Follow the `location` link in the response to determine the status of the task and use [Get task](#api-rest-api-3-task-taskId-get) to obtain subsequent updates.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Edit issues* [project permissions](https://confluence.atlassian.com/x/yodKLg) for the project containing the issue.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue properties`

### Bulk set issue property
> Sets a property value on multiple issues.<br/>
> <br/>
> The value set can be a constant or determined by a [Jira expression](https://developer.atlassian.com/cloud/jira/platform/jira-expressions/). Expressions must be computable with constant complexity when applied to a set of issues. Expressions must also comply with the [restrictions](https://developer.atlassian.com/cloud/jira/platform/jira-expressions/#restrictions) that apply to all Jira expressions.<br/>
> <br/>
> The issues to be updated can be specified by a filter.<br/>
> <br/>
> The filter identifies issues eligible for update using these criteria:<br/>
> <br/>
>  *  `entityIds` Only issues from this list are eligible.<br/>
>  *  `currentValue` Only issues with the property set to this value are eligible.<br/>
>  *  `hasProperty`:<br/>
>     <br/>
>      *  If *true*, only issues with the property are eligible.<br/>
>      *  If *false*, only issues without the property are eligible.<br/>
> <br/>
> If more than one criteria is specified, they are joined with the logical *AND*: only issues that satisfy all criteria are eligible.<br/>
> <br/>
> If an invalid combination of criteria is provided, an error is returned. For example, specifying a `currentValue` and `hasProperty` as *false* would not match any issues (because without the property the property cannot have a value).<br/>
> <br/>
> The filter is optional. Without the filter all the issues visible to the user and where the user has the EDIT\_ISSUES permission for the issue are considered eligible.<br/>
> <br/>
> This operation is:<br/>
> <br/>
>  *  transactional, either all eligible issues are updated or, when errors occur, none are updated.<br/>
>  *  [asynchronous](#async). Follow the `location` link in the response to determine the status of the task and use [Get task](#api-rest-api-3-task-taskId-get) to obtain subsequent updates.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for each project containing issues.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Edit issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for each issue.<br/>

*Tags:* `Issue properties`

#### Input Parameters
* `propertyKey` - _required_ - The key of the property. The maximum length is 255 characters.<br/>

### Bulk delete issue property
> Deletes a property value from multiple issues. The issues to be updated can be specified by filter criteria.<br/>
> <br/>
> The criteria the filter used to identify eligible issues are:<br/>
> <br/>
>  *  `entityIds` Only issues from this list are eligible.<br/>
>  *  `currentValue` Only issues with the property set to this value are eligible.<br/>
> <br/>
> If both criteria is specified, they are joined with the logical *AND*: only issues that satisfy both criteria are considered eligible.<br/>
> <br/>
> If no filter criteria are specified, all the issues visible to the user and where the user has the EDIT\_ISSUES permission for the issue are considered eligible.<br/>
> <br/>
> This operation is:<br/>
> <br/>
>  *  transactional, either the property is deleted from all eligible issues or, when errors occur, no properties are deleted.<br/>
>  *  [asynchronous](#async). Follow the `location` link in the response to determine the status of the task and use [Get task](#api-rest-api-3-task-taskId-get) to obtain subsequent updates.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [ project permission](https://confluence.atlassian.com/x/yodKLg) for each project containing issues.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Edit issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for each issue.<br/>

*Tags:* `Issue properties`

#### Input Parameters
* `propertyKey` - _required_ - The key of the property.<br/>

### Get issue
> Returns the details for an issue.<br/>
> <br/>
> The issue is identified by its ID or key, however, if the identifier doesn't match an issue, a case-insensitive search and check for moved issues is performed. If a matching issue is found its details are returned, a 302 or other redirect is **not** returned. The issue key returned in the response is the key of the issue found.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `fields` - _optional_ - A list of fields to return for the issue. This parameter accepts a comma-separated list. Use it to retrieve a subset of fields. Allowed values:<br/>
<br/>
 *  `*all` Returns all fields.<br/>
 *  `*navigable` Returns navigable fields.<br/>
 *  Any issue field, prefixed with a minus to exclude.<br/>
<br/>
Examples:<br/>
<br/>
 *  `summary,comment` Returns only the summary and comments fields.<br/>
 *  `-description` Returns all (default) fields except description.<br/>
 *  `*navigable,-comment` Returns all navigable fields except comment.<br/>
<br/>
This parameter may be specified multiple times. For example, `fields=field1,field2& fields=field3`.<br/>
<br/>
Note: All fields are returned by default. This differs from [Search for issues using JQL (GET)](#api-rest-api-3-search-get) and [Search for issues using JQL (POST)](#api-rest-api-3-search-post) where the default is all navigable fields.<br/>
* `fieldsByKeys` - _optional_ - Whether fields in `fields` are referenced by keys rather than IDs. This parameter is useful where fields have been added by a connect app and a field's key may differ from its ID.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about the issues in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `renderedFields` Returns field values rendered in HTML format.<br/>
 *  `names` Returns the display name of each field.<br/>
 *  `schema` Returns the schema describing a field type.<br/>
 *  `transitions` Returns all possible transitions for the issue.<br/>
 *  `editmeta` Returns information about how each field can be edited.<br/>
 *  `changelog` Returns a list of recent updates to an issue, sorted by date, starting from the most recent.<br/>
 *  `versionedRepresentations` Returns a JSON array for each version of a field's value, with the highest number representing the most recent version. Note: When included in the request, the `fields` parameter is ignored.<br/>
* `properties` - _optional_ - A list of issue properties to return for the issue. This parameter accepts a comma-separated list. Allowed values:<br/>
<br/>
 *  `*all` Returns all issue properties.<br/>
 *  Any issue property key, prefixed with a minus to exclude.<br/>
<br/>
Examples:<br/>
<br/>
 *  `*all` Returns all properties.<br/>
 *  `*all,-prop1` Returns all properties except `prop1`.<br/>
 *  `prop1,prop2` Returns `prop1` and `prop2` properties.<br/>
<br/>
This parameter may be specified multiple times. For example, `properties=prop1,prop2& properties=prop3`.<br/>
* `updateHistory` - _optional_ - Whether the project in which the issue is created is added to the user's **Recently viewed** project list, as shown under **Projects** in Jira. This also populates the [JQL issues search](#api-rest-api-3-search-get) `lastViewed` field.<br/>

### Edit issue
> Edits an issue. A transition may be applied and issue properties updated as part of the edit.<br/>
> <br/>
> The edits to the issue's fields are defined using `update` and `fields`. The fields that can be edited are determined using [ Get edit issue metadata](#api-rest-api-3-issue-issueIdOrKey-editmeta-get).<br/>
> <br/>
> The parent field may be set by key or ID. For standard issue types, the parent may be removed by setting `update.parent.set.none` to *true*. Note that the `description`, `environment`, and any `textarea` type custom fields (multi-line text fields) take Atlassian Document Format content. Single line custom fields (`textfield`) accept a string and don't handle Atlassian Document Format content.<br/>
> <br/>
> Connect app users with admin permission (from user permissions and app scopes) and Forge app users with the `manage:jira-configuration` scope can override the screen security configuration using `overrideScreenSecurity` and `overrideEditableFlag`.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Edit issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `notifyUsers` - _optional_ - Whether a notification email about the issue update is sent to all watchers. To disable the notification, administer Jira or administer project permissions are required. If the user doesn't have the necessary permission the request is ignored.<br/>
* `overrideScreenSecurity` - _optional_ - Whether screen security is overridden to enable hidden fields to be edited. Available to Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope.<br/>
* `overrideEditableFlag` - _optional_ - Whether screen security is overridden to enable uneditable fields to be edited. Available to Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope.<br/>

### Delete issue
> Deletes an issue.<br/>
> <br/>
> An issue cannot be deleted if it has one or more subtasks. To delete an issue with subtasks, set `deleteSubtasks`. This causes the issue's subtasks to be deleted with the issue.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Delete issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the issue.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `deleteSubtasks` - _optional_ - Whether the issue's subtasks are deleted when the issue is deleted.<br/>
    Possible values: true, false.

### Assign issue
> Assigns an issue to a user. Use this operation when the calling user does not have the *Edit Issues* permission but has the *Assign issue* permission for the project that the issue is in.<br/>
> <br/>
> If `name` or `accountId` is set to:<br/>
> <br/>
>  *  `"-1"`, the issue is assigned to the default assignee for the project.<br/>
>  *  `null`, the issue is set to unassigned.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse Projects* and *Assign Issues* [ project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue to be assigned.<br/>

### Add attachment
> Adds one or more attachments to an issue. Attachments are posted as multipart/form-data ([RFC 1867](https://www.ietf.org/rfc/rfc1867.txt)).<br/>
> <br/>
> Note that:<br/>
> <br/>
>  *  The request must have a `X-Atlassian-Token: no-check` header, if not it is blocked. See [Special headers](#special-request-headers) for more information.<br/>
>  *  The name of the multipart/form-data parameter that contains the attachments must be `file`.<br/>
> <br/>
> The following examples upload a file called *myfile.txt* to the issue *TEST-123*:<br/>
> <br/>
> #### curl ####<br/>
> <br/>
>     curl --location --request POST 'https://your-domain.atlassian.net/rest/api/3/issue/TEST-123/attachments'<br/>
>      -u 'email@example.com:<api_token>'<br/>
>      -H 'X-Atlassian-Token: no-check'<br/>
>      --form 'file=@"myfile.txt"'<br/>
> <br/>
> #### Node.js ####<br/>
> <br/>
>     // This code sample uses the 'node-fetch' and 'form-data' libraries:<br/>
>      // https://www.npmjs.com/package/node-fetch<br/>
>      // https://www.npmjs.com/package/form-data<br/>
>      const fetch = require('node-fetch');<br/>
>      const FormData = require('form-data');<br/>
>      const fs = require('fs');<br/>
>     <br/>
>      const filePath = 'myfile.txt';<br/>
>      const form = new FormData();<br/>
>      const stats = fs.statSync(filePath);<br/>
>      const fileSizeInBytes = stats.size;<br/>
>      const fileStream = fs.createReadStream(filePath);<br/>
>     <br/>
>      form.append('file', fileStream, {knownLength: fileSizeInBytes});<br/>
>     <br/>
>      fetch('https://your-domain.atlassian.net/rest/api/3/issue/TEST-123/attachments', {<br/>
>          method: 'POST',<br/>
>          body: form,<br/>
>          headers: {<br/>
>              'Authorization': `Basic ${Buffer.from(<br/>
>                  'email@example.com:'<br/>
>              ).toString('base64')}`,<br/>
>              'Accept': 'application/json',<br/>
>              'X-Atlassian-Token': 'no-check'<br/>
>          }<br/>
>      })<br/>
>          .then(response => {<br/>
>              console.log(<br/>
>                  `Response: ${response.status} ${response.statusText}`<br/>
>              );<br/>
>              return response.text();<br/>
>          })<br/>
>          .then(text => console.log(text))<br/>
>          .catch(err => console.error(err));<br/>
> <br/>
> #### Java ####<br/>
> <br/>
>     // This code sample uses the  'Unirest' library:<br/>
>      // http://unirest.io/java.html<br/>
>      HttpResponse response = Unirest.post("https://your-domain.atlassian.net/rest/api/2/issue/{issueIdOrKey}/attachments")<br/>
>              .basicAuth("email@example.com", "")<br/>
>              .header("Accept", "application/json")<br/>
>              .header("X-Atlassian-Token", "no-check")<br/>
>              .field("file", new File("myfile.txt"))<br/>
>              .asJson();<br/>
>     <br/>
>              System.out.println(response.getBody());<br/>
> <br/>
> #### Python ####<br/>
> <br/>
>     # This code sample uses the 'requests' library:<br/>
>      # http://docs.python-requests.org<br/>
>      import requests<br/>
>      from requests.auth import HTTPBasicAuth<br/>
>      import json<br/>
>     <br/>
>      url = "https://your-domain.atlassian.net/rest/api/2/issue/{issueIdOrKey}/attachments"<br/>
>     <br/>
>      auth = HTTPBasicAuth("email@example.com", "")<br/>
>     <br/>
>      headers = {<br/>
>         "Accept": "application/json",<br/>
>         "X-Atlassian-Token": "no-check"<br/>
>      }<br/>
>     <br/>
>      response = requests.request(<br/>
>         "POST",<br/>
>         url,<br/>
>         headers = headers,<br/>
>         auth = auth,<br/>
>         files = {<br/>
>              "file": ("myfile.txt", open("myfile.txt","rb"), "application-type")<br/>
>         }<br/>
>      )<br/>
>     <br/>
>      print(json.dumps(json.loads(response.text), sort_keys=True, indent=4, separators=(",", ": ")))<br/>
> <br/>
> #### PHP ####<br/>
> <br/>
>     // This code sample uses the 'Unirest' library:<br/>
>      // http://unirest.io/php.html<br/>
>      Unirest\Request::auth('email@example.com', '');<br/>
>     <br/>
>      $headers = array(<br/>
>        'Accept' => 'application/json',<br/>
>        'X-Atlassian-Token' => 'no-check'<br/>
>      );<br/>
>     <br/>
>      $parameters = array(<br/>
>        'file' => File::add('myfile.txt')<br/>
>      );<br/>
>     <br/>
>      $response = Unirest\Request::post(<br/>
>        'https://your-domain.atlassian.net/rest/api/2/issue/{issueIdOrKey}/attachments',<br/>
>        $headers,<br/>
>        $parameters<br/>
>      );<br/>
>     <br/>
>      var_dump($response)<br/>
> <br/>
> #### Forge ####<br/>
> <br/>
>     // This sample uses Atlassian Forge and the `form-data` library.<br/>
>      // https://developer.atlassian.com/platform/forge/<br/>
>      // https://www.npmjs.com/package/form-data<br/>
>      import api from "@forge/api";<br/>
>      import FormData from "form-data";<br/>
>     <br/>
>      const form = new FormData();<br/>
>      form.append('file', fileStream, {knownLength: fileSizeInBytes});<br/>
>     <br/>
>      const response = await api.asApp().requestJira('/rest/api/2/issue/{issueIdOrKey}/attachments', {<br/>
>          method: 'POST',<br/>
>          body: form,<br/>
>          headers: {<br/>
>              'Accept': 'application/json',<br/>
>              'X-Atlassian-Token': 'no-check'<br/>
>          }<br/>
>      });<br/>
>     <br/>
>      console.log(`Response: ${response.status} ${response.statusText}`);<br/>
>      console.log(await response.json());<br/>
> <br/>
> Tip: Use a client library. Many client libraries have classes for handling multipart POST operations. For example, in Java, the Apache HTTP Components library provides a [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) class for multipart POST operations.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** <br/>
> <br/>
>  *  *Browse Projects* and *Create attachments* [ project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue attachments`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue that attachments are added to.<br/>

### Get changelogs by IDs
> Returns changelogs for an issue specified by a list of changelog IDs.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>

### Add comment
> Adds a comment to an issue.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Add comments* [ project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue containing the comment is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue comments`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about comments in the response. This parameter accepts `renderedBody`, which returns the comment body rendered in HTML.<br/>

### Get comment
> Returns a comment.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the comment.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the comment has visibility restrictions, the user belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue comments`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `id` - _required_ - The ID of the comment.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about comments in the response. This parameter accepts `renderedBody`, which returns the comment body rendered in HTML.<br/>

### Update comment
> Updates a comment.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue containing the comment is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Edit all comments*[ project permission](https://confluence.atlassian.com/x/yodKLg) to update any comment or *Edit own comments* to update comment created by the user.<br/>
>  *  If the comment has visibility restrictions, the user belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue comments`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `id` - _required_ - The ID of the comment.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about comments in the response. This parameter accepts `renderedBody`, which returns the comment body rendered in HTML.<br/>

### Delete comment
> Deletes a comment.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue containing the comment is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Delete all comments*[ project permission](https://confluence.atlassian.com/x/yodKLg) to delete any comment or *Delete own comments* to delete comment created by the user,<br/>
>  *  If the comment has visibility restrictions, the user belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue comments`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `id` - _required_ - The ID of the comment.<br/>

### Send notification for issue
> Creates an email notification for an issue and adds it to the mail queue.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - ID or key of the issue that the notification is sent for.<br/>

### Get issue property
> Returns the key and value of an issue's property.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the issue.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue properties`

#### Input Parameters
* `issueIdOrKey` - _required_ - The key or ID of the issue.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Set issue property
> Sets the value of an issue's property. Use this resource to store custom data against an issue.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Edit issues* [project permissions](https://confluence.atlassian.com/x/yodKLg) for the project containing the issue.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue properties`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `propertyKey` - _required_ - The key of the issue property. The maximum length is 255 characters.<br/>

### Delete issue property
> Deletes an issue's property.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Edit issues* [project permissions](https://confluence.atlassian.com/x/yodKLg) for the project containing the issue.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue properties`

#### Input Parameters
* `issueIdOrKey` - _required_ - The key or ID of the issue.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Create or update remote issue link
> Creates or updates a remote issue link for an issue.<br/>
> <br/>
> If a `globalId` is provided and a remote issue link with that global ID is found it is updated. Any fields without values in the request are set to null. Otherwise, the remote issue link is created.<br/>
> <br/>
> This operation requires [issue linking to be active](https://confluence.atlassian.com/x/yoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Link issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue remote links`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>

### Delete remote issue link by global ID
> Deletes the remote issue link from the issue using the link's global ID. Where the global ID includes reserved URL characters these must be escaped in the request. For example, pass `system=http://www.mycompany.com/support&id=1` as `system%3Dhttp%3A%2F%2Fwww.mycompany.com%2Fsupport%26id%3D1`.<br/>
> <br/>
> This operation requires [issue linking to be active](https://confluence.atlassian.com/x/yoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Link issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is implemented, issue-level security permission to view the issue.<br/>

*Tags:* `Issue remote links`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `globalId` - _required_ - The global ID of a remote issue link.<br/>

### Get remote issue link by ID
> Returns a remote issue link for an issue.<br/>
> <br/>
> This operation requires [issue linking to be active](https://confluence.atlassian.com/x/yoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue remote links`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `linkId` - _required_ - The ID of the remote issue link.<br/>

### Update remote issue link by ID
> Updates a remote issue link for an issue.<br/>
> <br/>
> Note: Fields without values in the request are set to null.<br/>
> <br/>
> This operation requires [issue linking to be active](https://confluence.atlassian.com/x/yoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Link issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue remote links`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `linkId` - _required_ - The ID of the remote issue link.<br/>

### Delete remote issue link by ID
> Deletes a remote issue link from an issue.<br/>
> <br/>
> This operation requires [issue linking to be active](https://confluence.atlassian.com/x/yoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects*, *Edit issues*, and *Link issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue remote links`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `linkId` - _required_ - The ID of a remote issue link.<br/>

### Transition issue
> Performs an issue transition and, if the transition has a screen, updates the fields from the transition screen.<br/>
> <br/>
> sortByCategory To update the fields on the transition screen, specify the fields in the `fields` or `update` parameters in the request body. Get details about the fields using [ Get transitions](#api-rest-api-3-issue-issueIdOrKey-transitions-get) with the `transitions.fields` expand.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Transition issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issues`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>

### Add vote
> Adds the user's vote to an issue. This is the equivalent of the user clicking *Vote* on an issue in Jira.<br/>
> <br/>
> This operation requires the **Allow users to vote on issues** option to be *ON*. This option is set in General configuration for Jira. See [Configuring Jira application options](https://confluence.atlassian.com/x/uYXKM) for details.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue votes`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>

### Delete vote
> Deletes a user's vote from an issue. This is the equivalent of the user clicking *Unvote* on an issue in Jira.<br/>
> <br/>
> This operation requires the **Allow users to vote on issues** option to be *ON*. This option is set in General configuration for Jira. See [Configuring Jira application options](https://confluence.atlassian.com/x/uYXKM) for details.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue votes`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>

### Add watcher
> Adds a user as a watcher of an issue by passing the account ID of the user. For example, `"5b10ac8d82e05b22cc7d4ef5"`. If no user is specified the calling user is added.<br/>
> <br/>
> This operation requires the **Allow users to watch issues** option to be *ON*. This option is set in General configuration for Jira. See [Configuring Jira application options](https://confluence.atlassian.com/x/uYXKM) for details.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  To add users other than themselves to the watchlist, *Manage watcher list* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>

*Tags:* `Issue watchers`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>

### Delete watcher
> Deletes a user as a watcher of an issue.<br/>
> <br/>
> This operation requires the **Allow users to watch issues** option to be *ON*. This option is set in General configuration for Jira. See [Configuring Jira application options](https://confluence.atlassian.com/x/uYXKM) for details.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  To remove users other than themselves from the watchlist, *Manage watcher list* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>

*Tags:* `Issue watchers`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `username` - _optional_ - This parameter is no longer available. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `accountId` - _optional_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*. Required.<br/>

### Add worklog
> Adds a worklog to an issue.<br/>
> <br/>
> Time tracking must be enabled in Jira, otherwise this operation returns an error. For more information, see [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* and *Work on issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue worklogs`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key the issue.<br/>
* `notifyUsers` - _optional_ - Whether users watching the issue are notified by email.<br/>
* `adjustEstimate` - _optional_ - Defines how to update the issue's time estimate, the options are:<br/>
<br/>
 *  `new` Sets the estimate to a specific value, defined in `newEstimate`.<br/>
 *  `leave` Leaves the estimate unchanged.<br/>
 *  `manual` Reduces the estimate by amount specified in `reduceBy`.<br/>
 *  `auto` Reduces the estimate by the value of `timeSpent` in the worklog.<br/>
    Possible values: new, leave, manual, auto.
* `newEstimate` - _optional_ - The value to set as the issue's remaining time estimate, as days (\#d), hours (\#h), or minutes (\#m or \#). For example, *2d*. Required when `adjustEstimate` is `new`.<br/>
* `reduceBy` - _optional_ - The amount to reduce the issue's remaining estimate by, as days (\#d), hours (\#h), or minutes (\#m). For example, *2d*. Required when `adjustEstimate` is `manual`.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about work logs in the response. This parameter accepts `properties`, which returns worklog properties.<br/>
* `overrideEditableFlag` - _optional_ - Whether the worklog entry should be added to the issue even if the issue is not editable, because jira.issue.editable set to false or missing. For example, the issue is closed. Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope can use this flag.<br/>

### Get worklog
> Returns a worklog.<br/>
> <br/>
> Time tracking must be enabled in Jira, otherwise this operation returns an error. For more information, see [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the worklog has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue worklogs`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `id` - _required_ - The ID of the worklog.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about work logs in the response. This parameter accepts<br/>
<br/>
`properties`, which returns worklog properties.<br/>

### Update worklog
> Updates a worklog.<br/>
> <br/>
> Time tracking must be enabled in Jira, otherwise this operation returns an error. For more information, see [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Edit all worklogs*[ project permission](https://confluence.atlassian.com/x/yodKLg) to update any worklog or *Edit own worklogs* to update worklogs created by the user.<br/>
>  *  If the worklog has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue worklogs`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key the issue.<br/>
* `id` - _required_ - The ID of the worklog.<br/>
* `notifyUsers` - _optional_ - Whether users watching the issue are notified by email.<br/>
* `adjustEstimate` - _optional_ - Defines how to update the issue's time estimate, the options are:<br/>
<br/>
 *  `new` Sets the estimate to a specific value, defined in `newEstimate`.<br/>
 *  `leave` Leaves the estimate unchanged.<br/>
 *  `auto` Updates the estimate by the difference between the original and updated value of `timeSpent` or `timeSpentSeconds`.<br/>
    Possible values: new, leave, manual, auto.
* `newEstimate` - _optional_ - The value to set as the issue's remaining time estimate, as days (\#d), hours (\#h), or minutes (\#m or \#). For example, *2d*. Required when `adjustEstimate` is `new`.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about worklogs in the response. This parameter accepts `properties`, which returns worklog properties.<br/>
* `overrideEditableFlag` - _optional_ - Whether the worklog should be added to the issue even if the issue is not editable. For example, because the issue is closed. Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope can use this flag.<br/>

### Delete worklog
> Deletes a worklog from an issue.<br/>
> <br/>
> Time tracking must be enabled in Jira, otherwise this operation returns an error. For more information, see [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Delete all worklogs*[ project permission](https://confluence.atlassian.com/x/yodKLg) to delete any worklog or *Delete own worklogs* to delete worklogs created by the user,<br/>
>  *  If the worklog has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue worklogs`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `id` - _required_ - The ID of the worklog.<br/>
* `notifyUsers` - _optional_ - Whether users watching the issue are notified by email.<br/>
* `adjustEstimate` - _optional_ - Defines how to update the issue's time estimate, the options are:<br/>
<br/>
 *  `new` Sets the estimate to a specific value, defined in `newEstimate`.<br/>
 *  `leave` Leaves the estimate unchanged.<br/>
 *  `manual` Increases the estimate by amount specified in `increaseBy`.<br/>
 *  `auto` Reduces the estimate by the value of `timeSpent` in the worklog.<br/>
    Possible values: new, leave, manual, auto.
* `newEstimate` - _optional_ - The value to set as the issue's remaining time estimate, as days (\#d), hours (\#h), or minutes (\#m or \#). For example, *2d*. Required when `adjustEstimate` is `new`.<br/>
* `increaseBy` - _optional_ - The amount to increase the issue's remaining estimate by, as days (\#d), hours (\#h), or minutes (\#m or \#). For example, *2d*. Required when `adjustEstimate` is `manual`.<br/>
* `overrideEditableFlag` - _optional_ - Whether the work log entry should be added to the issue even if the issue is not editable, because jira.issue.editable set to false or missing. For example, the issue is closed. Connect app users with admin permission and Forge app users with the `manage:jira-configuration` scope can use this flag.<br/>

### Get worklog property
> Returns the value of a worklog property.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the worklog has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue worklog properties`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `worklogId` - _required_ - The ID of the worklog.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Set worklog property
> Sets the value of a worklog property. Use this operation to store custom data against the worklog.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  *Edit all worklogs*[ project permission](https://confluence.atlassian.com/x/yodKLg) to update any worklog or *Edit own worklogs* to update worklogs created by the user.<br/>
>  *  If the worklog has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue worklog properties`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `worklogId` - _required_ - The ID of the worklog.<br/>
* `propertyKey` - _required_ - The key of the issue property. The maximum length is 255 characters.<br/>

### Delete worklog property
> Deletes a worklog property.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the worklog has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue worklog properties`

#### Input Parameters
* `issueIdOrKey` - _required_ - The ID or key of the issue.<br/>
* `worklogId` - _required_ - The ID of the worklog.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Create issue link
> Creates a link between two issues. Use this operation to indicate a relationship between two issues and optionally add a comment to the from (outward) issue. To use this resource the site must have [Issue Linking](https://confluence.atlassian.com/x/yoXKM) enabled.<br/>
> <br/>
> This resource returns nothing on the creation of an issue link. To obtain the ID of the issue link, use `https://your-domain.atlassian.net/rest/api/3/issue/[linked issue key]?fields=issuelinks`.<br/>
> <br/>
> If the link request duplicates a link, the response indicates that the issue link was created. If the request included a comment, the comment is added.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse project* [project permission](https://confluence.atlassian.com/x/yodKLg) for all the projects containing the issues to be linked,<br/>
>  *  *Link issues* [project permission](https://confluence.atlassian.com/x/yodKLg) on the project containing the from (outward) issue,<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>
>  *  If the comment has visibility restrictions, belongs to the group or has the role visibility is restricted to.<br/>

*Tags:* `Issue links`

### Get issue link
> Returns an issue link.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Browse project* [project permission](https://confluence.atlassian.com/x/yodKLg) for all the projects containing the linked issues.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, permission to view both of the issues.<br/>

*Tags:* `Issue links`

#### Input Parameters
* `linkId` - _required_ - The ID of the issue link.<br/>

### Delete issue link
> Deletes an issue link.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  Browse project [project permission](https://confluence.atlassian.com/x/yodKLg) for all the projects containing the issues in the link.<br/>
>  *  *Link issues* [project permission](https://confluence.atlassian.com/x/yodKLg) for at least one of the projects containing issues in the link.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, permission to view both of the issues.<br/>

*Tags:* `Issue links`

#### Input Parameters
* `linkId` - _required_ - The ID of the issue link.<br/>

### Create issue link type
> Creates an issue link type. Use this operation to create descriptions of the reasons why issues are linked. The issue link type consists of a name and descriptions for a link's inward and outward relationships.<br/>
> <br/>
> To use this operation, the site must have [issue linking](https://confluence.atlassian.com/x/yoXKM) enabled.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue link types`

### Get issue link type
> Returns an issue link type.<br/>
> <br/>
> To use this operation, the site must have [issue linking](https://confluence.atlassian.com/x/yoXKM) enabled.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for a project in the site.<br/>

*Tags:* `Issue link types`

#### Input Parameters
* `issueLinkTypeId` - _required_ - The ID of the issue link type.<br/>

### Update issue link type
> Updates an issue link type.<br/>
> <br/>
> To use this operation, the site must have [issue linking](https://confluence.atlassian.com/x/yoXKM) enabled.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue link types`

#### Input Parameters
* `issueLinkTypeId` - _required_ - The ID of the issue link type.<br/>

### Delete issue link type
> Deletes an issue link type.<br/>
> <br/>
> To use this operation, the site must have [issue linking](https://confluence.atlassian.com/x/yoXKM) enabled.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue link types`

#### Input Parameters
* `issueLinkTypeId` - _required_ - The ID of the issue link type.<br/>

### Get issue security scheme
> Returns an issue security scheme along with its security levels.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>
>  *  *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for a project that uses the requested issue security scheme.<br/>

*Tags:* `Issue security schemes`

#### Input Parameters
* `id` - _required_ - The ID of the issue security scheme. Use the [Get issue security schemes](#api-rest-api-3-issuesecurityschemes-get) operation to get a list of issue security scheme IDs.<br/>

### Create issue type
> Creates an issue type and adds it to the default issue type scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue types`

### Get issue type
> Returns an issue type.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) in a project the issue type is associated with or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue types`

#### Input Parameters
* `id` - _required_ - The ID of the issue type.<br/>

### Update issue type
> Updates the issue type.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue types`

#### Input Parameters
* `id` - _required_ - The ID of the issue type.<br/>

### Delete issue type
> Deletes the issue type. If the issue type is in use, all uses are updated with the alternative issue type (`alternativeIssueTypeId`). A list of alternative issue types are obtained from the [Get alternative issue types](#api-rest-api-3-issuetype-id-alternatives-get) resource.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue types`

#### Input Parameters
* `id` - _required_ - The ID of the issue type.<br/>
* `alternativeIssueTypeId` - _optional_ - The ID of the replacement issue type.<br/>

### Load issue type avatar
> Loads an avatar for the issue type.<br/>
> <br/>
> Specify the avatar's local file location in the body of the request. Also, include the following headers:<br/>
> <br/>
>  *  `X-Atlassian-Token: no-check` To prevent XSRF protection blocking the request, for more information see [Special Headers](#special-request-headers).<br/>
>  *  `Content-Type: image/image type` Valid image types are JPEG, GIF, or PNG.<br/>
> <br/>
> For example:  <br/>
> `curl --request POST \ --user email@example.com:<api_token> \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "<@/path/to/file/with/your/avatar>" \ --url 'https://your-domain.atlassian.net/rest/api/3/issuetype/{issueTypeId}'This`<br/>
> <br/>
> The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image.<br/>
> <br/>
> The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size.<br/>
> <br/>
> After creating the avatar, use [ Update issue type](#api-rest-api-3-issuetype-id-put) to set it as the issue type's displayed avatar.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue types`

#### Input Parameters
* `id` - _required_ - The ID of the issue type.<br/>
* `x` - _optional_ - The X coordinate of the top-left corner of the crop region.<br/>
* `y` - _optional_ - The Y coordinate of the top-left corner of the crop region.<br/>
* `size` - _required_ - The length of each side of the crop region.<br/>

### Get issue type property
> Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) to get the details of any issue type.<br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) to get the details of any issue types associated with the projects the user has permission to browse.<br/>

*Tags:* `Issue type properties`

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.<br/>
* `propertyKey` - _required_ - The key of the property. Use [Get issue type property keys](#api-rest-api-3-issuetype-issueTypeId-properties-get) to get a list of all issue type property keys.<br/>

### Set issue type property
> Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). Use this resource to store and update data against an issue type.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type properties`

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.<br/>
* `propertyKey` - _required_ - The key of the issue type property. The maximum length is 255 characters.<br/>

### Delete issue type property
> Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type properties`

#### Input Parameters
* `issueTypeId` - _required_ - The ID of the issue type.<br/>
* `propertyKey` - _required_ - The key of the property. Use [Get issue type property keys](#api-rest-api-3-issuetype-issueTypeId-properties-get) to get a list of all issue type property keys.<br/>

### Create issue type scheme
> Creates an issue type scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

### Assign issue type scheme to project
> Assigns an issue type scheme to a project.<br/>
> <br/>
> If any issues in the project are assigned issue types not present in the new scheme, the operation will fail. To complete the assignment those issues must be updated to use issue types in the new scheme.<br/>
> <br/>
> Issue type schemes can only be assigned to classic projects.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

### Update issue type scheme
> Updates an issue type scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

#### Input Parameters
* `issueTypeSchemeId` - _required_ - The ID of the issue type scheme.<br/>

### Delete issue type scheme
> Deletes an issue type scheme.<br/>
> <br/>
> Only issue type schemes used in classic projects can be deleted.<br/>
> <br/>
> Any projects assigned to the scheme are reassigned to the default issue type scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

#### Input Parameters
* `issueTypeSchemeId` - _required_ - The ID of the issue type scheme.<br/>

### Add issue types to issue type scheme
> Adds issue types to an issue type scheme.<br/>
> <br/>
> The added issue types are appended to the issue types list.<br/>
> <br/>
> If any of the issue types exist in the issue type scheme, the operation fails and no issue types are added.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

#### Input Parameters
* `issueTypeSchemeId` - _required_ - The ID of the issue type scheme.<br/>

### Change order of issue types
> Changes the order of issue types in an issue type scheme.<br/>
> <br/>
> The request body parameters must meet the following requirements:<br/>
> <br/>
>  *  all of the issue types must belong to the issue type scheme.<br/>
>  *  either `after` or `position` must be provided.<br/>
>  *  the issue type in `after` must not be in the issue type list.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

#### Input Parameters
* `issueTypeSchemeId` - _required_ - The ID of the issue type scheme.<br/>

### Remove issue type from issue type scheme
> Removes an issue type from an issue type scheme.<br/>
> <br/>
> This operation cannot remove:<br/>
> <br/>
>  *  any issue type used by issues.<br/>
>  *  any issue types from the default issue type scheme.<br/>
>  *  the last standard issue type from an issue type scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type schemes`

#### Input Parameters
* `issueTypeSchemeId` - _required_ - The ID of the issue type scheme.<br/>
* `issueTypeId` - _required_ - The ID of the issue type.<br/>

### Create issue type screen scheme
> Creates an issue type screen scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

### Assign issue type screen scheme to project
> Assigns an issue type screen scheme to a project.<br/>
> <br/>
> Issue type screen schemes can only be assigned to classic projects.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

### Update issue type screen scheme
> Updates an issue type screen scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

#### Input Parameters
* `issueTypeScreenSchemeId` - _required_ - The ID of the issue type screen scheme.<br/>

### Delete issue type screen scheme
> Deletes an issue type screen scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

#### Input Parameters
* `issueTypeScreenSchemeId` - _required_ - The ID of the issue type screen scheme.<br/>

### Append mappings to issue type screen scheme
> Appends issue type to screen scheme mappings to an issue type screen scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

#### Input Parameters
* `issueTypeScreenSchemeId` - _required_ - The ID of the issue type screen scheme.<br/>

### Update issue type screen scheme default screen scheme
> Updates the default screen scheme of an issue type screen scheme. The default screen scheme is used for all unmapped issue types.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

#### Input Parameters
* `issueTypeScreenSchemeId` - _required_ - The ID of the issue type screen scheme.<br/>

### Remove mappings from issue type screen scheme
> Removes issue type to screen scheme mappings from an issue type screen scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue type screen schemes`

#### Input Parameters
* `issueTypeScreenSchemeId` - _required_ - The ID of the issue type screen scheme.<br/>

### Get field reference data (POST)
> Returns reference data for JQL searches. This is a downloadable version of the documentation provided in [Advanced searching - fields reference](https://confluence.atlassian.com/x/gwORLQ) and [Advanced searching - functions reference](https://confluence.atlassian.com/x/hgORLQ), along with a list of JQL-reserved words. Use this information to assist with the programmatic creation of JQL queries or the validation of queries built in a custom query builder.<br/>
> <br/>
> This operation can filter the custom fields returned by project. Invalid project IDs in `projectIds` are ignored. System fields are always returned.<br/>
> <br/>
> It can also return the collapsed field for custom fields. Collapsed fields enable searches to be performed across all fields with the same name and of the same field type. For example, the collapsed field `Component - Component[Dropdown]` enables dropdown fields `Component - cf[10061]` and `Component - cf[10062]` to be searched simultaneously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `JQL`

### Check issues against JQL
> Checks whether one or more issues would be returned by one or more JQL queries.<br/>
> <br/>
> **[Permissions](#permissions) required:** None, however, issues are only matched against JQL queries where the user has:<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that the issue is in.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue search`

### Parse JQL query
> Parses and validates JQL queries.<br/>
> <br/>
> Validation is performed in context of the current user.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `JQL`

#### Input Parameters
* `validation` - _optional_ - How to validate the JQL query and treat the validation results. Validation options include:<br/>
<br/>
 *  `strict` Returns all errors. If validation fails, the query structure is not returned.<br/>
 *  `warn` Returns all errors. If validation fails but the JQL query is correctly formed, the query structure is returned.<br/>
 *  `none` No validation is performed. If JQL query is correctly formed, the query structure is returned.<br/>
    Possible values: strict, warn, none.

### Convert user identifiers to account IDs in JQL queries
> Converts one or more JQL queries with user identifiers (username or user key) to equivalent JQL queries with account IDs.<br/>
> <br/>
> You may wish to use this operation if your system stores JQL queries and you want to make them GDPR-compliant. For more information about GDPR-related changes, see the [migration guide](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/).<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `JQL`

### Set preference
> Creates a preference for the user or updates a preference's value by sending a plain text string. For example, `false`. An arbitrary preference can be created with the value containing up to 255 characters. In addition, the following keys define system preferences that can be set or created:<br/>
> <br/>
>  *  *user.notifications.mimetype* The mime type used in notifications sent to the user. Defaults to `html`.<br/>
>  *  *user.notify.own.changes* Whether the user gets notified of their own changes. Defaults to `false`.<br/>
>  *  *user.default.share.private* Whether new [ filters](https://confluence.atlassian.com/x/eQiiLQ) are set to private. Defaults to `true`.<br/>
>  *  *user.keyboard.shortcuts.disabled* Whether keyboard shortcuts are disabled. Defaults to `false`.<br/>
>  *  *user.autowatch.disabled* Whether the user automatically watches issues they create or add a comment to. By default, not set: the user takes the instance autowatch setting.<br/>
> <br/>
> Note that these keys are deprecated:<br/>
> <br/>
>  *  *jira.user.locale* The locale of the user. By default, not set. The user takes the instance locale.<br/>
>  *  *jira.user.timezone* The time zone of the user. By default, not set. The user takes the instance timezone.<br/>
> <br/>
> Use [ Update a user profile](https://developer.atlassian.com/cloud/admin/user-management/rest/#api-users-account-id-manage-profile-patch) from the user management REST API to manage timezone and locale instead.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Myself`

#### Input Parameters
* `key` - _required_ - The key of the preference. The maximum length is 255 characters.<br/>

### Delete preference
> Deletes a preference of the user, which restores the default value of system defined settings.<br/>
> <br/>
> Note that these keys are deprecated:<br/>
> <br/>
>  *  *jira.user.locale* The locale of the user. By default, not set. The user takes the instance locale.<br/>
>  *  *jira.user.timezone* The time zone of the user. By default, not set. The user takes the instance timezone.<br/>
> <br/>
> Use [ Update a user profile](https://developer.atlassian.com/cloud/admin/user-management/rest/#api-users-account-id-manage-profile-patch) from the user management REST API to manage timezone and locale instead.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Myself`

#### Input Parameters
* `key` - _required_ - The key of the preference.<br/>

### Set locale
> Deprecated, use [ Update a user profile](https://developer.atlassian.com/cloud/admin/user-management/rest/#api-users-account-id-manage-profile-patch) from the user management REST API instead.<br/>
> <br/>
> Sets the locale of the user. The locale must be one supported by the instance of Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Myself`

### Delete locale
> Deprecated, use [ Update a user profile](https://developer.atlassian.com/cloud/admin/user-management/rest/#api-users-account-id-manage-profile-patch) from the user management REST API instead.<br/>
> <br/>
> Deletes the locale of the user, which restores the default setting.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Myself`

### Get notification scheme
> Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however the user must have permission to administer at least one project associated with the notification scheme.<br/>

*Tags:* `Issue notification schemes`

#### Input Parameters
* `id` - _required_ - The ID of the notification scheme. Use [Get notification schemes paginated](#api-rest-api-3-notificationscheme-get) to get a list of notification scheme IDs.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `all` Returns all expandable information.<br/>
 *  `field` Returns information about any custom fields assigned to receive an event.<br/>
 *  `group` Returns information about any groups assigned to receive an event.<br/>
 *  `notificationSchemeEvents` Returns a list of event associations. This list is returned for all expandable information.<br/>
 *  `projectRole` Returns information about any project roles assigned to receive an event.<br/>
 *  `user` Returns information about any users assigned to receive an event.<br/>

### Get bulk permissions
> Returns:<br/>
> <br/>
>  *  for a list of global permissions, the global permissions granted to a user.<br/>
>  *  for a list of project permissions and lists of projects and issues, for each project permission a list of the projects and issues a user can access or manipulate.<br/>
> <br/>
> If no account ID is provided, the operation returns details for the logged in user.<br/>
> <br/>
> Note that:<br/>
> <br/>
>  *  Invalid project and issue IDs are ignored.<br/>
>  *  A maximum of 1000 projects and 1000 issues can be checked.<br/>
>  *  Null values in `globalPermissions`, `projectPermissions`, `projectPermissions.projects`, and `projectPermissions.issues` are ignored.<br/>
>  *  Empty strings in `projectPermissions.permissions` are ignored.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) to check the permissions for other users, otherwise none. However, Connect apps can make a call from the app server to the product to obtain permission details for any user, without admin permission. This Connect app ability doesn't apply to calls made using AP.request() in a browser.<br/>

*Tags:* `Permissions`

### Get permitted projects
> Returns all the projects where the user is granted a list of project permissions.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `Permissions`

### Create permission scheme
> Creates a new permission scheme. You can create a permission scheme with or without defining a set of permission grants.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts a comma-separated list. Note that permissions are always included when you specify any value. Expand options include:<br/>
<br/>
 *  `all` Returns all expandable information.<br/>
 *  `field` Returns information about the custom field granted the permission.<br/>
 *  `group` Returns information about the group that is granted the permission.<br/>
 *  `permissions` Returns all permission grants for each permission scheme.<br/>
 *  `projectRole` Returns information about the project role granted the permission.<br/>
 *  `user` Returns information about the user who is granted the permission.<br/>

### Get permission scheme
> Returns a permission scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme to return.<br/>
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts a comma-separated list. Note that permissions are included when you specify any value. Expand options include:<br/>
<br/>
 *  `all` Returns all expandable information.<br/>
 *  `field` Returns information about the custom field granted the permission.<br/>
 *  `group` Returns information about the group that is granted the permission.<br/>
 *  `permissions` Returns all permission grants for each permission scheme.<br/>
 *  `projectRole` Returns information about the project role granted the permission.<br/>
 *  `user` Returns information about the user who is granted the permission.<br/>

### Update permission scheme
> Updates a permission scheme. Below are some important things to note when using this resource:<br/>
> <br/>
>  *  If a permissions list is present in the request, then it is set in the permission scheme, overwriting *all existing* grants.<br/>
>  *  If you want to update only the name and description, then do not send a permissions list in the request.<br/>
>  *  Sending an empty list will remove all permission grants from the permission scheme.<br/>
> <br/>
> If you want to add or delete a permission grant instead of updating the whole list, see [Create permission grant](#api-rest-api-3-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](#api-rest-api-3-permissionscheme-schemeId-permission-permissionId-delete).<br/>
> <br/>
> See [About permission schemes and grants](../api-group-permission-schemes/#about-permission-schemes-and-grants) for more details.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme to update.<br/>
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts a comma-separated list. Note that permissions are always included when you specify any value. Expand options include:<br/>
<br/>
 *  `all` Returns all expandable information.<br/>
 *  `field` Returns information about the custom field granted the permission.<br/>
 *  `group` Returns information about the group that is granted the permission.<br/>
 *  `permissions` Returns all permission grants for each permission scheme.<br/>
 *  `projectRole` Returns information about the project role granted the permission.<br/>
 *  `user` Returns information about the user who is granted the permission.<br/>

### Delete permission scheme
> Deletes a permission scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme being deleted.<br/>

### Create permission grant
> Creates a permission grant in a permission scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme in which to create a new permission grant.<br/>
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts a comma-separated list. Note that permissions are always included when you specify any value. Expand options include:<br/>
<br/>
 *  `permissions` Returns all permission grants for each permission scheme.<br/>
 *  `user` Returns information about the user who is granted the permission.<br/>
 *  `group` Returns information about the group that is granted the permission.<br/>
 *  `projectRole` Returns information about the project role granted the permission.<br/>
 *  `field` Returns information about the custom field granted the permission.<br/>
 *  `all` Returns all expandable information.<br/>

### Get permission scheme grant
> Returns a permission grant.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme.<br/>
* `permissionId` - _required_ - The ID of the permission grant.<br/>
* `expand` - _optional_ - Use expand to include additional information in the response. This parameter accepts a comma-separated list. Note that permissions are always included when you specify any value. Expand options include:<br/>
<br/>
 *  `all` Returns all expandable information.<br/>
 *  `field` Returns information about the custom field granted the permission.<br/>
 *  `group` Returns information about the group that is granted the permission.<br/>
 *  `permissions` Returns all permission grants for each permission scheme.<br/>
 *  `projectRole` Returns information about the project role granted the permission.<br/>
 *  `user` Returns information about the user who is granted the permission.<br/>

### Delete permission scheme grant
> Deletes a permission grant from a permission scheme. See [About permission schemes and grants](../api-group-permission-schemes/#about-permission-schemes-and-grants) for more details.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Permission schemes`

#### Input Parameters
* `schemeId` - _required_ - The ID of the permission scheme to delete the permission grant from.<br/>
* `permissionId` - _required_ - The ID of the permission grant to delete.<br/>

### Get priority
> Returns an issue priority.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Issue priorities`

#### Input Parameters
* `id` - _required_ - The ID of the issue priority.<br/>

### Create project
> Creates a project based on a project type template, as shown in the following table:<br/>
> <br/>
> | Project Type Key | Project Template Key |  <br/>
> |--|--|  <br/>
> | `business` | `com.atlassian.jira-core-project-templates:jira-core-simplified-content-management`, `com.atlassian.jira-core-project-templates:jira-core-simplified-document-approval`, `com.atlassian.jira-core-project-templates:jira-core-simplified-lead-tracking`, `com.atlassian.jira-core-project-templates:jira-core-simplified-process-control`, `com.atlassian.jira-core-project-templates:jira-core-simplified-procurement`, `com.atlassian.jira-core-project-templates:jira-core-simplified-project-management`, `com.atlassian.jira-core-project-templates:jira-core-simplified-recruitment`, `com.atlassian.jira-core-project-templates:jira-core-simplified-task-tracking` |  <br/>
> | `service_desk` | `com.atlassian.servicedesk:simplified-it-service-management`, `com.atlassian.servicedesk:simplified-general-service-desk`, `com.atlassian.servicedesk:simplified-internal-service-desk`, `com.atlassian.servicedesk:simplified-external-service-desk`, `com.atlassian.servicedesk:simplified-hr-service-desk`, `com.atlassian.servicedesk:simplified-facilities-service-desk`, `com.atlassian.servicedesk:simplified-legal-service-desk` |  <br/>
> | `software` | `com.pyxis.greenhopper.jira:gh-simplified-agility-kanban`, `com.pyxis.greenhopper.jira:gh-simplified-agility-scrum`, `com.pyxis.greenhopper.jira:gh-simplified-basic`, `com.pyxis.greenhopper.jira:gh-simplified-kanban-classic`, `com.pyxis.greenhopper.jira:gh-simplified-scrum-classic` |  <br/>
> The project types are available according to the installed Jira features as follows:<br/>
> <br/>
>  *  Jira Core, the default, enables `business` projects.<br/>
>  *  Jira Service Management enables `service_desk` projects.<br/>
>  *  Jira Software enables `software` projects.<br/>
> <br/>
> To determine which features are installed, go to **Jira settings** > **Apps** > **Manage apps** and review the System Apps list. To add Jira Software or Jira Service Management into a JIRA instance, use **Jira settings** > **Apps** > **Finding new apps**. For more information, see [ Managing add-ons](https://confluence.atlassian.com/x/S31NLg).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

### Get project type by key
> Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `Project types`

#### Input Parameters
* `projectTypeKey` - _required_ - The key of the project type.<br/>
    Possible values: software, service_desk, business, product_discovery.

### Get project
> Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for a project.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information in the response. This parameter accepts a comma-separated list. Note that the project description, issue types, and project lead are included in all responses by default. Expand options include:<br/>
<br/>
 *  `description` The project description.<br/>
 *  `issueTypes` The issue types associated with the project.<br/>
 *  `lead` The project lead.<br/>
 *  `projectKeys` All project keys associated with the project.<br/>
 *  `issueTypeHierarchy` The project issue type hierarchy.<br/>
* `properties` - _optional_ - A list of project properties to return for the project. This parameter accepts a comma-separated list.<br/>

### Update project
> Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of a project.<br/>
> <br/>
> All parameters are optional in the body of the request.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information in the response. This parameter accepts a comma-separated list. Note that the project description, issue types, and project lead are included in all responses by default. Expand options include:<br/>
<br/>
 *  `description` The project description.<br/>
 *  `issueTypes` The issue types associated with the project.<br/>
 *  `lead` The project lead.<br/>
 *  `projectKeys` All project keys associated with the project.<br/>

### Delete project
> Deletes a project.<br/>
> <br/>
> You can't delete a project if it's archived. To delete an archived project, restore the project and then delete it. To restore a project, use the Jira UI.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `enableUndo` - _optional_ - Whether this project is placed in the Jira recycle bin where it will be available for restoration.<br/>

### Archive project
> Archives a project. You can't delete a project if it's archived. To delete an archived project, restore the project and then delete it. To restore a project, use the Jira UI.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>

### Set project avatar
> Sets the avatar displayed for a project.<br/>
> <br/>
> Use [Load project avatar](#api-rest-api-3-project-projectIdOrKey-avatar2-post) to store avatars against the project, before using this operation to set the displayed avatar.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer projects* [project permission](https://confluence.atlassian.com/x/yodKLg).<br/>

*Tags:* `Project avatars`

#### Input Parameters
* `projectIdOrKey` - _required_ - The ID or (case-sensitive) key of the project.<br/>

### Delete project avatar
> Deletes a custom avatar from a project. Note that system avatars cannot be deleted.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer projects* [project permission](https://confluence.atlassian.com/x/yodKLg).<br/>

*Tags:* `Project avatars`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or (case-sensitive) key.<br/>
* `id` - _required_ - The ID of the avatar.<br/>

### Load project avatar
> Loads an avatar for a project.<br/>
> <br/>
> Specify the avatar's local file location in the body of the request. Also, include the following headers:<br/>
> <br/>
>  *  `X-Atlassian-Token: no-check` To prevent XSRF protection blocking the request, for more information see [Special Headers](#special-request-headers).<br/>
>  *  `Content-Type: image/image type` Valid image types are JPEG, GIF, or PNG.<br/>
> <br/>
> For example:  <br/>
> `curl --request POST `<br/>
> <br/>
> `--user email@example.com:<api_token> `<br/>
> <br/>
> `--header 'X-Atlassian-Token: no-check' `<br/>
> <br/>
> `--header 'Content-Type: image/< image_type>' `<br/>
> <br/>
> `--data-binary "<@/path/to/file/with/your/avatar>" `<br/>
> <br/>
> `--url 'https://your-domain.atlassian.net/rest/api/3/project/{projectIdOrKey}/avatar2'`<br/>
> <br/>
> The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image.<br/>
> <br/>
> The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size.<br/>
> <br/>
> After creating the avatar use [Set project avatar](#api-rest-api-3-project-projectIdOrKey-avatar-put) to set it as the project's displayed avatar.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer projects* [project permission](https://confluence.atlassian.com/x/yodKLg).<br/>

*Tags:* `Project avatars`

#### Input Parameters
* `projectIdOrKey` - _required_ - The ID or (case-sensitive) key of the project.<br/>
* `x` - _optional_ - The X coordinate of the top-left corner of the crop region.<br/>
* `y` - _optional_ - The Y coordinate of the top-left corner of the crop region.<br/>
* `size` - _optional_ - The length of each side of the crop region.<br/>

### Delete project asynchronously
> Deletes a project asynchronously.<br/>
> <br/>
> This operation is:<br/>
> <br/>
>  *  transactional, that is, if part of the delete fails the project is not deleted.<br/>
>  *  [asynchronous](#async). Follow the `location` link in the response to determine the status of the task and use [Get task](#api-rest-api-3-task-taskId-get) to obtain subsequent updates.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>

### Get project property
> Returns the value of a [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the property.<br/>

*Tags:* `Project properties`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `propertyKey` - _required_ - The project property key. Use [Get project property keys](#api-rest-api-3-project-projectIdOrKey-properties-get) to get a list of all project property keys.<br/>

### Set project property
> Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project in which the property is created.<br/>

*Tags:* `Project properties`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `propertyKey` - _required_ - The key of the project property. The maximum length is 255 characters.<br/>

### Delete project property
> Deletes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from a project.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the property.<br/>

*Tags:* `Project properties`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `propertyKey` - _required_ - The project property key. Use [Get project property keys](#api-rest-api-3-project-projectIdOrKey-properties-get) to get a list of all project property keys.<br/>

### Restore deleted project
> Restores a project from the Jira recycle bin.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>

### Get project role for project
> Returns a project role's details and actors associated with the project. The list of actors is sorted by display name.<br/>
> <br/>
> To check whether a user belongs to a role based on their group memberships, use [Get user](#api-rest-api-3-user-get) with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project roles`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Set actors for project role
> Sets the actors for a project role for a project, replacing all existing actors.<br/>
> <br/>
> To add actors to the project without overwriting the existing list, use [Add actors to project role](#api-rest-api-3-project-projectIdOrKey-role-id-post).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project role actors`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Add actors to project role
> Adds actors to a project role for the project.<br/>
> <br/>
> To replace all actors for the project, use [Set actors for project role](#api-rest-api-3-project-projectIdOrKey-role-id-put).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project role actors`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Delete actors from project role
> Deletes actors from a project role for the project.<br/>
> <br/>
> To remove default actors from the project role, use [Delete default actors from project role](#api-rest-api-3-role-id-actors-delete).<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project or *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project role actors`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>
* `user` - _optional_ - The user account ID of the user to remove from the project role.<br/>
* `group` - _optional_ - The name of the group to remove from the project role.<br/>

### Update project type
> Deprecated, this feature is no longer supported and no alternatives are available, see [Convert project to a different template or type](https://confluence.atlassian.com/x/yEKeOQ). Updates a [project type](https://confluence.atlassian.com/x/GwiiLQ). The project type can be updated for classic projects only, project type cannot be updated for next-gen projects.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Projects`

#### Input Parameters
* `projectIdOrKey` - _required_ - The project ID or project key (case sensitive).<br/>
* `newProjectTypeKey` - _required_ - The key of the new project type.<br/>
    Possible values: software, service_desk, business.

### Set project's sender email
> Sets the [project's sender email address](https://confluence.atlassian.com/x/dolKLg).<br/>
> <br/>
> If `emailAddress` is an empty string, the default email address is restored.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.<br/>

*Tags:* `Project email`

#### Input Parameters
* `projectId` - _required_ - The project ID.<br/>

### Assign permission scheme
> Assigns a permission scheme with a project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg)<br/>

*Tags:* `Project permission schemes`

#### Input Parameters
* `projectKeyOrId` - _required_ - The project ID or project key (case sensitive).<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information in the response. This parameter accepts a comma-separated list. Note that permissions are included when you specify any value. Expand options include:<br/>
<br/>
 *  `all` Returns all expandable information.<br/>
 *  `field` Returns information about the custom field granted the permission.<br/>
 *  `group` Returns information about the group that is granted the permission.<br/>
 *  `permissions` Returns all permission grants for each permission scheme.<br/>
 *  `projectRole` Returns information about the project role granted the permission.<br/>
 *  `user` Returns information about the user who is granted the permission.<br/>

### Create project category
> Creates a project category.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project categories`

### Get project category by ID
> Returns a project category.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Project categories`

#### Input Parameters
* `id` - _required_ - The ID of the project category.<br/>

### Update project category
> Updates a project category.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project categories`

#### Input Parameters
* `id` - _required_

### Delete project category
> Deletes a project category.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project categories`

#### Input Parameters
* `id` - _required_ - ID of the project category to delete.<br/>

### Get resolution
> Returns an issue resolution value.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Issue resolutions`

#### Input Parameters
* `id` - _required_ - The ID of the issue resolution value.<br/>

### Create project role
> Creates a new project role with no [default actors](#api-rest-api-3-resolution-get). You can use the [Add default actors to project role](#api-rest-api-3-role-id-actors-post) operation to add default actors to the project role after creating it.<br/>
> <br/>
> *Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created.*<<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project roles`

### Get project role by ID
> Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project roles`

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Fully update project role
> Updates the project role's name and description. You must include both a name and a description in the request.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project roles`

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Partial update project role
> Updates either the project role's name or its description.<br/>
> <br/>
> You cannot update both the name and description at the same time using this operation. If you send a request with a name and a description only the name is updated.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project roles`

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Delete project role
> Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project roles`

#### Input Parameters
* `id` - _required_ - The ID of the project role to delete. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>
* `swap` - _optional_ - The ID of the project role that will replace the one being deleted.<br/>

### Add default actors to project role
> Adds [default actors](#api-rest-api-3-resolution-get) to a role. You may add groups or users, but you cannot add groups and users in the same request.<br/>
> <br/>
> Changing a project role's default actors does not affect project role members for projects already created.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project role actors`

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>

### Delete default actors from project role
> Deletes the [default actors](#api-rest-api-3-resolution-get) from a project role. You may delete a group or user, but you cannot delete a group and a user in the same request.<br/>
> <br/>
> Changing a project role's default actors does not affect project role members for projects already created.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Project role actors`

#### Input Parameters
* `id` - _required_ - The ID of the project role. Use [Get all project roles](#api-rest-api-3-role-get) to get a list of project role IDs.<br/>
* `user` - _optional_ - The user account ID of the user to remove as a default actor.<br/>
* `group` - _optional_ - The group name of the group to be removed as a default actor.<br/>

### Create screen
> Creates a screen with a default field tab.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screens`

### Add field to default screen
> Adds a field to the default tab of the default screen.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screens`

#### Input Parameters
* `fieldId` - _required_ - The ID of the field.<br/>

### Update screen
> Updates a screen. Only screens used in classic projects can be updated.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screens`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>

### Delete screen
> Deletes a screen. A screen cannot be deleted if it is used in a screen scheme, workflow, or workflow draft.<br/>
> <br/>
> Only screens used in classic projects can be deleted.<br/>

*Tags:* `Screens`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>

### Create screen tab
> Creates a tab for a screen.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tabs`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>

### Update screen tab
> Updates the name of a screen tab.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tabs`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>
* `tabId` - _required_ - The ID of the screen tab.<br/>

### Delete screen tab
> Deletes a screen tab.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tabs`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>
* `tabId` - _required_ - The ID of the screen tab.<br/>

### Add screen tab field
> Adds a field to a screen tab.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tab fields`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>
* `tabId` - _required_ - The ID of the screen tab.<br/>

### Remove screen tab field
> Removes a field from a screen tab.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tab fields`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>
* `tabId` - _required_ - The ID of the screen tab.<br/>
* `id` - _required_ - The ID of the field.<br/>

### Move screen tab field
> Moves a screen tab field.<br/>
> <br/>
> If `after` and `position` are provided in the request, `position` is ignored.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tab fields`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>
* `tabId` - _required_ - The ID of the screen tab.<br/>
* `id` - _required_ - The ID of the field.<br/>

### Move screen tab
> Moves a screen tab.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen tabs`

#### Input Parameters
* `screenId` - _required_ - The ID of the screen.<br/>
* `tabId` - _required_ - The ID of the screen tab.<br/>
* `pos` - _required_ - The position of tab. The base index is 0.<br/>

### Create screen scheme
> Creates a screen scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen schemes`

### Update screen scheme
> Updates a screen scheme. Only screen schemes used in classic projects can be updated.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen schemes`

#### Input Parameters
* `screenSchemeId` - _required_ - The ID of the screen scheme.<br/>

### Delete screen scheme
> Deletes a screen scheme. A screen scheme cannot be deleted if it is used in an issue type screen scheme.<br/>
> <br/>
> Only screens schemes used in classic projects can be deleted.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Screen schemes`

#### Input Parameters
* `screenSchemeId` - _required_ - The ID of the screen scheme.<br/>

### Search for issues using JQL (POST)
> Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ).<br/>
> <br/>
> There is a [GET](#api-rest-api-3-search-get) version of this resource that can be used for smaller JQL query expressions.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** Issues are included in the response where the user has:<br/>
> <br/>
>  *  *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the issue.<br/>
>  *  If [issue-level security](https://confluence.atlassian.com/x/J4lKLg) is configured, issue-level security permission to view the issue.<br/>

*Tags:* `Issue search`

### Get issue security level
> Returns details of an issue security level.<br/>
> <br/>
> Use [Get issue security scheme](#api-rest-api-3-issuesecurityschemes-id-get) to obtain the IDs of issue security levels associated with the issue security scheme.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `Issue security level`

#### Input Parameters
* `id` - _required_ - The ID of the issue security level.<br/>

### Set issue navigator default columns
> Sets the default issue navigator columns.<br/>
> <br/>
> The `columns` parameter accepts a navigable field value and is expressed as HTML form data. To specify multiple columns, pass multiple `columns` parameters. For example, in curl:<br/>
> <br/>
> `curl -X PUT -d columns=summary -d columns=description https://your-domain.atlassian.net/rest/api/3/settings/columns`<br/>
> <br/>
> If no column details are sent, then all default columns are removed.<br/>
> <br/>
> A navigable field is one that can be used as a column on the issue navigator. Find details of navigable issue columns using [Get fields](#api-rest-api-3-field-get).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Issue navigator settings`

### Get status
> Returns a status. The status must be associated with a workflow to be returned.<br/>
> <br/>
> If a name is used on more than one status, only the status found first is returned. Therefore, identifying the status by its ID may be preferable.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> [Permissions](#permissions) required: None.<br/>

*Tags:* `Workflow statuses`

#### Input Parameters
* `idOrName` - _required_ - The ID or name of the status.<br/>

### Get status category
> Returns a status category. Status categories provided a mechanism for categorizing [statuses](#api-rest-api-3-status-idOrName-get).<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira.<br/>

*Tags:* `Workflow status categories`

#### Input Parameters
* `idOrKey` - _required_ - The ID or key of the status category.<br/>

### Get task
> Returns the status of a [long-running asynchronous task](#async).<br/>
> <br/>
> When a task has finished, this operation returns the JSON blob applicable to the task. See the documentation of the operation that created the task for details. Task details are not permanently retained. As of September 2019, details are retained for 14 days although this period may change without notice.<br/>
> <br/>
> **[Permissions](#permissions) required:** either of:<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>
>  *  Creator of the task.<br/>

*Tags:* `Tasks`

#### Input Parameters
* `taskId` - _required_ - The ID of the task.<br/>

### Cancel task
> Cancels a task.<br/>
> <br/>
> **[Permissions](#permissions) required:** either of:<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>
>  *  Creator of the task.<br/>

*Tags:* `Tasks`

#### Input Parameters
* `taskId` - _required_ - The ID of the task.<br/>

### Get avatars
> Returns the system and custom avatars for a project or issue type.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  for custom project avatars, *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project the avatar belongs to.<br/>
>  *  for custom issue type avatars, *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for at least one project the issue type is used in.<br/>
>  *  for system avatars, none.<br/>

*Tags:* `Avatars`

#### Input Parameters
* `type` - _required_ - The avatar type.<br/>
    Possible values: project, issuetype.
* `entityId` - _required_ - The ID of the item the avatar is associated with.<br/>

### Load avatar
> Loads a custom avatar for a project or issue type.<br/>
> <br/>
> Specify the avatar's local file location in the body of the request. Also, include the following headers:<br/>
> <br/>
>  *  `X-Atlassian-Token: no-check` To prevent XSRF protection blocking the request, for more information see [Special Headers](#special-request-headers).<br/>
>  *  `Content-Type: image/image type` Valid image types are JPEG, GIF, or PNG.<br/>
> <br/>
> For example:  <br/>
> `curl --request POST `<br/>
> <br/>
> `--user email@example.com:<api_token> `<br/>
> <br/>
> `--header 'X-Atlassian-Token: no-check' `<br/>
> <br/>
> `--header 'Content-Type: image/< image_type>' `<br/>
> <br/>
> `--data-binary "<@/path/to/file/with/your/avatar>" `<br/>
> <br/>
> `--url 'https://your-domain.atlassian.net/rest/api/3/universal_avatar/type/{type}/owner/{entityId}'`<br/>
> <br/>
> The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image.<br/>
> <br/>
> The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size.<br/>
> <br/>
> After creating the avatar use:<br/>
> <br/>
>  *  [Update issue type](#api-rest-api-3-issuetype-id-put) to set it as the issue type's displayed avatar.<br/>
>  *  [Set project avatar](#api-rest-api-3-project-projectIdOrKey-avatar-put) to set it as the project's displayed avatar.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Avatars`

#### Input Parameters
* `type` - _required_ - The avatar type.<br/>
    Possible values: project, issuetype.
* `entityId` - _required_ - The ID of the item the avatar is associated with.<br/>
* `x` - _optional_ - The X coordinate of the top-left corner of the crop region.<br/>
* `y` - _optional_ - The Y coordinate of the top-left corner of the crop region.<br/>
* `size` - _required_ - The length of each side of the crop region.<br/>

### Delete avatar
> Deletes an avatar from a project or issue type.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Avatars`

#### Input Parameters
* `type` - _required_ - The avatar type.<br/>
    Possible values: project, issuetype.
* `owningObjectId` - _required_ - The ID of the item the avatar is associated with.<br/>
* `id` - _required_ - The ID of the avatar.<br/>

### Get avatar image by type
> Returns the default project or issue type avatar image.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** None.<br/>

*Tags:* `Avatars`

#### Input Parameters
* `type` - _required_ - The icon type of the avatar.<br/>
    Possible values: issuetype, project.
* `size` - _optional_ - The size of the avatar image. If not provided the default size is returned.<br/>
    Possible values: xsmall, small, medium, large, xlarge.
* `format` - _optional_ - The format to return the avatar image in. If not provided the original content format is returned.<br/>
    Possible values: png.

### Get avatar image by ID
> Returns a project or issue type avatar image by ID.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  For system avatars, none.<br/>
>  *  For custom project avatars, *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project the avatar belongs to.<br/>
>  *  For custom issue type avatars, *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for at least one project the issue type is used in.<br/>

*Tags:* `Avatars`

#### Input Parameters
* `type` - _required_ - The icon type of the avatar.<br/>
    Possible values: issuetype, project.
* `id` - _required_ - The ID of the avatar.<br/>
* `size` - _optional_ - The size of the avatar image. If not provided the default size is returned.<br/>
    Possible values: xsmall, small, medium, large, xlarge.
* `format` - _optional_ - The format to return the avatar image in. If not provided the original content format is returned.<br/>
    Possible values: png.

### Get avatar image by owner
> Returns the avatar image for a project or issue type.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  For system avatars, none.<br/>
>  *  For custom project avatars, *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project the avatar belongs to.<br/>
>  *  For custom issue type avatars, *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for at least one project the issue type is used in.<br/>

*Tags:* `Avatars`

#### Input Parameters
* `type` - _required_ - The icon type of the avatar.<br/>
    Possible values: issuetype, project.
* `entityId` - _required_ - The ID of the project or issue type the avatar belongs to.<br/>
* `size` - _optional_ - The size of the avatar image. If not provided the default size is returned.<br/>
    Possible values: xsmall, small, medium, large, xlarge.
* `format` - _optional_ - The format to return the avatar image in. If not provided the original content format is returned.<br/>
    Possible values: png.

### Create user
> Creates a user. This resource is retained for legacy compatibility. As soon as a more suitable alternative is available this resource will be deprecated.<br/>
> <br/>
> If the user exists and has access to Jira, the operation returns a 201 status. If the user exists but does not have access to Jira, the operation returns a 400 status.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Users`

### Delete user
> Deletes a user.<br/>
> <br/>
> **[Permissions](#permissions) required:** Site administration (that is, membership of the *site-admin* [group](https://confluence.atlassian.com/x/24xjL)).<br/>

*Tags:* `Users`

#### Input Parameters
* `accountId` - _required_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>
* `username` - _optional_ - This parameter is no longer available. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `key` - _optional_ - This parameter is no longer available. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>

### Set user default columns
> Sets the default [ issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If an account ID is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed.<br/>
> <br/>
> The parameters for this resource are expressed as HTML form data. For example, in curl:<br/>
> <br/>
> `curl -X PUT -d columns=summary -d columns=description https://your-domain.atlassian.net/rest/api/3/user/columns?accountId=5b10ac8d82e05b22cc7d4ef5'`<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg), to set the columns on any user.<br/>
>  *  Permission to access Jira, to set the calling user's columns.<br/>

*Tags:* `Users`

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>

### Reset user default columns
> Resets the default [ issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If `accountId` is not passed, the calling user's default columns are reset.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg), to set the columns on any user.<br/>
>  *  Permission to access Jira, to set the calling user's columns.<br/>

*Tags:* `Users`

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>
* `username` - _optional_ - This parameter is no longer available. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>

### Get user property
> Returns the value of a user's property. If no property key is provided [Get user property keys](#api-rest-api-3-user-properties-get) is called.<br/>
> <br/>
> Note: This operation does not access the [user properties](https://confluence.atlassian.com/x/8YxjL) created and maintained in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg), to get a property from any user.<br/>
>  *  Access to Jira, to get a property from the calling user's record.<br/>

*Tags:* `User properties`

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>
* `userKey` - _optional_ - This parameter is no longer available and will be removed from the documentation soon. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `username` - _optional_ - This parameter is no longer available and will be removed from the documentation soon. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `propertyKey` - _required_ - The key of the user's property.<br/>

### Set user property
> Sets the value of a user's property. Use this resource to store custom data against a user.<br/>
> <br/>
> Note: This operation does not access the [user properties](https://confluence.atlassian.com/x/8YxjL) created and maintained in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg), to set a property on any user.<br/>
>  *  Access to Jira, to set a property on the calling user's record.<br/>

*Tags:* `User properties`

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>
* `userKey` - _optional_ - This parameter is no longer available and will be removed from the documentation soon. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `username` - _optional_ - This parameter is no longer available and will be removed from the documentation soon. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `propertyKey` - _required_ - The key of the user's property. The maximum length is 255 characters.<br/>

### Delete user property
> Deletes a property from a user.<br/>
> <br/>
> Note: This operation does not access the [user properties](https://confluence.atlassian.com/x/8YxjL) created and maintained in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:**<br/>
> <br/>
>  *  *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg), to delete a property from any user.<br/>
>  *  Access to Jira, to delete a property from the calling user's record.<br/>

*Tags:* `User properties`

#### Input Parameters
* `accountId` - _optional_ - The account ID of the user, which uniquely identifies the user across all Atlassian products. For example, *5b10ac8d82e05b22cc7d4ef5*.<br/>
* `userKey` - _optional_ - This parameter is no longer available and will be removed from the documentation soon. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `username` - _optional_ - This parameter is no longer available and will be removed from the documentation soon. See the [deprecation notice](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-user-privacy-api-migration-guide/) for details.<br/>
* `propertyKey` - _required_ - The key of the user's property.<br/>

### Create version
> Creates a project version.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project the version is added to.<br/>

*Tags:* `Project versions`

### Get version
> Returns a project version.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project containing the version.<br/>

*Tags:* `Project versions`

#### Input Parameters
* `id` - _required_ - The ID of the version.<br/>
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about version in the response. This parameter accepts a comma-separated list. Expand options include:<br/>
<br/>
 *  `operations` Returns the list of operations available for this version.<br/>
 *  `issuesstatus` Returns the count of issues in this version for each of the status categories *to do*, *in progress*, *done*, and *unmapped*. The *unmapped* property represents the number of issues with a status other than *to do*, *in progress*, and *done*.<br/>

### Update version
> Updates a project version.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that contains the version.<br/>

*Tags:* `Project versions`

#### Input Parameters
* `id` - _required_ - The ID of the version.<br/>

### Delete version
> Deletes a project version.<br/>
> <br/>
> Deprecated, use [ Delete and replace version](#api-rest-api-3-version-id-removeAndSwap-post) that supports swapping version values in custom fields, in addition to the swapping for `fixVersion` and `affectedVersion` provided in this resource.<br/>
> <br/>
> Alternative versions can be provided to update issues that use the deleted version in `fixVersion` or `affectedVersion`. If alternatives are not provided, occurrences of `fixVersion` and `affectedVersion` that contain the deleted version are cleared.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that contains the version.<br/>

*Tags:* `Project versions`

#### Input Parameters
* `id` - _required_ - The ID of the version.<br/>
* `moveFixIssuesTo` - _optional_ - The ID of the version to update `fixVersion` to when the field contains the deleted version. The replacement version must be in the same project as the version being deleted and cannot be the version being deleted.<br/>
* `moveAffectedIssuesTo` - _optional_ - The ID of the version to update `affectedVersion` to when the field contains the deleted version. The replacement version must be in the same project as the version being deleted and cannot be the version being deleted.<br/>

### Merge versions
> Merges two project versions. The merge is completed by deleting the version specified in `id` and replacing any occurrences of its ID in `fixVersion` with the version ID specified in `moveIssuesTo`.<br/>
> <br/>
> Consider using [ Delete and replace version](#api-rest-api-3-version-id-removeAndSwap-post) instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`, and custom fields.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that contains the version.<br/>

*Tags:* `Project versions`

#### Input Parameters
* `id` - _required_ - The ID of the version to delete.<br/>
* `moveIssuesTo` - _required_ - The ID of the version to merge into.<br/>

### Move version
> Modifies the version's sequence within the project, which affects the display order of the versions in Jira.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Browse projects* project permission for the project that contains the version.<br/>

*Tags:* `Project versions`

#### Input Parameters
* `id` - _required_ - The ID of the version to be moved.<br/>

### Delete and replace version
> Deletes a project version.<br/>
> <br/>
> Alternative versions can be provided to update issues that use the deleted version in `fixVersion`, `affectedVersion`, or any version picker custom fields. If alternatives are not provided, occurrences of `fixVersion`, `affectedVersion`, and any version picker custom field, that contain the deleted version, are cleared. Any replacement version must be in the same project as the version being deleted and cannot be the version being deleted.<br/>
> <br/>
> This operation can be accessed anonymously.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg) or *Administer Projects* [project permission](https://confluence.atlassian.com/x/yodKLg) for the project that contains the version.<br/>

*Tags:* `Project versions`

#### Input Parameters
* `id` - _required_ - The ID of the version.<br/>

### Register dynamic webhooks
> Registers webhooks.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only [Connect](https://developer.atlassian.com/cloud/jira/platform/#connect-apps) and [OAuth 2.0](https://developer.atlassian.com/cloud/jira/platform/oauth-2-3lo-apps) apps can use this operation.<br/>

*Tags:* `Webhooks`

### Delete webhooks by ID
> Removes webhooks by ID. Only webhooks registered by the calling app are removed. If webhooks created by other apps are specified, they are ignored.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only [Connect](https://developer.atlassian.com/cloud/jira/platform/#connect-apps) and [OAuth 2.0](https://developer.atlassian.com/cloud/jira/platform/oauth-2-3lo-apps) apps can use this operation.<br/>

*Tags:* `Webhooks`

### Extend webhook life
> Webhooks registered through the REST API expire after 30 days. Call this resource periodically to keep them alive.<br/>
> <br/>
> Unrecognized webhook IDs (those that are not found or belong to other apps) are ignored.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only [Connect](https://developer.atlassian.com/cloud/jira/platform/#connect-apps) and [OAuth 2.0](https://developer.atlassian.com/cloud/jira/platform/oauth-2-3lo-apps) apps can use this operation.<br/>

*Tags:* `Webhooks`

### Create workflow
> Creates a workflow. You can define transition rules using the shapes detailed in the following sections. If no transitional rules are specified the default system transition rules are used.<br/>
> <br/>
> #### Conditions ####<br/>
> <br/>
> Conditions enable workflow rules that govern whether a transition can execute.<br/>
> <br/>
> ##### Always false condition #####<br/>
> <br/>
> A condition that always fails.<br/>
> <br/>
>     {<br/>
>        "type": "AlwaysFalseCondition"<br/>
>      }<br/>
> <br/>
> ##### Block transition until approval #####<br/>
> <br/>
> A condition that blocks issue transition if there is a pending approval.<br/>
> <br/>
>     {<br/>
>        "type": "BlockInProgressApprovalCondition"<br/>
>      }<br/>
> <br/>
> ##### Compare number custom field condition #####<br/>
> <br/>
> A condition that allows transition if a comparison between a number custom field and a value is true.<br/>
> <br/>
>     {<br/>
>        "type": "CompareNumberCFCondition",<br/>
>        "configuration": {<br/>
>          "comparator": "=",<br/>
>          "fieldId": "customfield_10029",<br/>
>          "fieldValue": 2<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `comparator` One of the supported comparator: `=`, `>`, and `<`.<br/>
>  *  `fieldId` The custom numeric field ID. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:float`<br/>
>      *  `com.pyxis.greenhopper.jira:jsw-story-points`<br/>
>  *  `fieldValue` The value for comparison.<br/>
> <br/>
> ##### Hide from user condition #####<br/>
> <br/>
> A condition that hides a transition from users. The transition can only be triggered from a workflow function or REST API operation.<br/>
> <br/>
>     {<br/>
>        "type": "RemoteOnlyCondition"<br/>
>      }<br/>
> <br/>
> ##### Only assignee condition #####<br/>
> <br/>
> A condition that allows only the assignee to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "AllowOnlyAssignee"<br/>
>      }<br/>
> <br/>
> ##### Only Bamboo notifications workflow condition #####<br/>
> <br/>
> A condition that makes the transition available only to Bamboo build notifications.<br/>
> <br/>
>     {<br/>
>        "type": "OnlyBambooNotificationsCondition"<br/>
>      }<br/>
> <br/>
> ##### Only reporter condition #####<br/>
> <br/>
> A condition that allows only the reporter to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "AllowOnlyReporter"<br/>
>      }<br/>
> <br/>
> ##### Permission condition #####<br/>
> <br/>
> A condition that allows only users with a permission to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "PermissionCondition",<br/>
>        "configuration": {<br/>
>            "permissionKey": "BROWSE_PROJECTS"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `permissionKey` The permission required to perform the transition. Allowed values: [built-in](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-permission-schemes/#built-in-permissions) or app defined permissions.<br/>
> <br/>
> ##### Previous status condition #####<br/>
> <br/>
> A condition that allows a transition based on whether an issue has or has not transitioned through a status.<br/>
> <br/>
>     {<br/>
>        "type": "PreviousStatusCondition",<br/>
>        "configuration": {<br/>
>          "ignoreLoopTransitions": true,<br/>
>          "includeCurrentStatus": true,<br/>
>          "mostRecentStatusOnly": true,<br/>
>          "reverseCondition": true,<br/>
>          "previousStatus": {<br/>
>            "id": "5"<br/>
>          }<br/>
>        }<br/>
>      }<br/>
> <br/>
> By default this condition allows the transition if the status, as defined by its ID in the `previousStatus` object, matches any previous issue status, unless:<br/>
> <br/>
>  *  `ignoreLoopTransitions` is `true`, then loop transitions (from and to the same status) are ignored.<br/>
>  *  `includeCurrentStatus` is `true`, then the current issue status is also checked.<br/>
>  *  `mostRecentStatusOnly` is `true`, then only the issue's preceding status (the one immediately before the current status) is checked.<br/>
>  *  `reverseCondition` is `true`, then the status must not be present.<br/>
> <br/>
> ##### Separation of duties condition #####<br/>
> <br/>
> A condition that prevents a user to perform the transition, if the user has already performed a transition on the issue.<br/>
> <br/>
>     {<br/>
>        "type": "SeparationOfDutiesCondition",<br/>
>        "configuration": {<br/>
>          "fromStatus": {<br/>
>            "id": "5"<br/>
>          },<br/>
>          "toStatus": {<br/>
>            "id": "6"<br/>
>          }<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `fromStatus` OPTIONAL. An object containing the ID of the source status of the transition that is blocked. If omitted any transition to `toStatus` is blocked.<br/>
>  *  `toStatus` An object containing the ID of the target status of the transition that is blocked.<br/>
> <br/>
> ##### Subtask blocking condition #####<br/>
> <br/>
> A condition that blocks transition on a parent issue if any of its subtasks are in any of one or more statuses.<br/>
> <br/>
>     {<br/>
>        "type": "SubTaskBlockingCondition",<br/>
>        "configuration": {<br/>
>          "statuses": [<br/>
>            {<br/>
>              "id": "1"<br/>
>            },<br/>
>            {<br/>
>              "id": "3"<br/>
>            }<br/>
>          ]<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `statuses` A list of objects containing status IDs.<br/>
> <br/>
> ##### User is in any group condition #####<br/>
> <br/>
> A condition that allows users belonging to any group from a list of groups to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "UserInAnyGroupCondition",<br/>
>        "configuration": {<br/>
>          "groups": [<br/>
>            "administrators",<br/>
>            "atlassian-addons-admin"<br/>
>          ]<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `groups` A list of group names.<br/>
> <br/>
> ##### User is in any project role condition #####<br/>
> <br/>
> A condition that allows only users with at least one project roles from a list of project roles to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "InAnyProjectRoleCondition",<br/>
>        "configuration": {<br/>
>          "projectRoles": [<br/>
>            {<br/>
>              "id": "10002"<br/>
>            },<br/>
>            {<br/>
>              "id": "10003"<br/>
>            },<br/>
>            {<br/>
>              "id": "10012"<br/>
>            },<br/>
>            {<br/>
>              "id": "10013"<br/>
>            }<br/>
>          ]<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `projectRoles` A list of objects containing project role IDs.<br/>
> <br/>
> ##### User is in custom field condition #####<br/>
> <br/>
> A condition that allows only users listed in a given custom field to execute the transition.<br/>
> <br/>
>     {<br/>
>        "type": "UserIsInCustomFieldCondition",<br/>
>        "configuration": {<br/>
>          "allowUserInField": false,<br/>
>          "fieldId": "customfield_10010"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `allowUserInField` If `true` only a user who is listed in `fieldId` can perform the transition, otherwise, only a user who is not listed in `fieldId` can perform the transition.<br/>
>  *  `fieldId` The ID of the field containing the list of users.<br/>
> <br/>
> ##### User is in group condition #####<br/>
> <br/>
> A condition that allows users belonging to a group to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "UserInGroupCondition",<br/>
>        "configuration": {<br/>
>          "group": "administrators",<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `group` The name of the group.<br/>
> <br/>
> ##### User is in group custom field condition #####<br/>
> <br/>
> A condition that allows users belonging to a group specified in a custom field to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "InGroupCFCondition",<br/>
>        "configuration": {<br/>
>          "fieldId": "customfield_10012",<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `fieldId` The ID of the field. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:multigrouppicker`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:grouppicker`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:select`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:multiselect`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:radiobuttons`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:multicheckboxes`<br/>
>      *  `com.pyxis.greenhopper.jira:gh-epic-status`<br/>
> <br/>
> ##### User is in project role condition #####<br/>
> <br/>
> A condition that allows users with a project role to execute a transition.<br/>
> <br/>
>     {<br/>
>        "type": "InProjectRoleCondition",<br/>
>        "configuration": {<br/>
>          "projectRole": {<br/>
>            "id": "10002"<br/>
>          }<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `projectRole` An object containing the ID of a project role.<br/>
> <br/>
> ##### Value field condition #####<br/>
> <br/>
> A conditions that allows a transition to execute if the value of a field is equal to a constant value or simply set.<br/>
> <br/>
>     {<br/>
>        "type": "ValueFieldCondition",<br/>
>        "configuration": {<br/>
>          "fieldId": "assignee",<br/>
>          "fieldValue": "qm:6e1ecee6-8e64-4db6-8c85-916bb3275f51:54b56885-2bd2-4381-8239-78263442520f",<br/>
>          "comparisonType": "NUMBER",<br/>
>          "comparator": "="<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `fieldId` The ID of a field used in the comparison.<br/>
>  *  `fieldValue` The expected value of the field.<br/>
>  *  `comparisonType` The type of the comparison. Allowed values: `STRING`, `NUMBER`, `DATE`, `DATE_WITHOUT_TIME`, or `OPTIONID`.<br/>
>  *  `comparator` One of the supported comparator: `>`, `>=`, `=`, `<=`, `<`, `!=`.<br/>
> <br/>
> **Notes:**<br/>
> <br/>
>  *  If you choose the comparison type `STRING`, only `=` and `!=` are valid options.<br/>
>  *  You may leave `fieldValue` empty when comparison type is `!=` to indicate that a value is required in the field.<br/>
>  *  For date fields without time format values as `yyyy-MM-dd`, and for those with time as `yyyy-MM-dd HH:mm`. For example, for July 16 2021 use `2021-07-16`, for 8:05 AM use `2021-07-16 08:05`, and for 4 PM: `2021-07-16 16:00`.<br/>
> <br/>
> #### Validators ####<br/>
> <br/>
> Validators check that any input made to the transition is valid before the transition is performed.<br/>
> <br/>
> ##### Date field validator #####<br/>
> <br/>
> A validator that compares two dates.<br/>
> <br/>
>     {<br/>
>        "type": "DateFieldValidator",<br/>
>        "configuration": {<br/>
>            "comparator": ">",<br/>
>            "date1": "updated",<br/>
>            "date2": "created",<br/>
>            "expression": "1d",<br/>
>            "includeTime": true<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `comparator` One of the supported comparator: `>`, `>=`, `=`, `<=`, `<`, or `!=`.<br/>
>  *  `date1` The date field to validate. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datepicker`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datetime`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-end`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-start`<br/>
>      *  `duedate`<br/>
>      *  `created`<br/>
>      *  `updated`<br/>
>      *  `Resolved`<br/>
>  *  `date2` The second date field. Required, if `expression` is not passed. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datepicker`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datetime`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-end`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-start`<br/>
>      *  `duedate`<br/>
>      *  `created`<br/>
>      *  `updated`<br/>
>      *  `Resolved`<br/>
>  *  `expression` An expression specifying an offset. Required, if `date2` is not passed. Offsets are built with a number, with `-` as prefix for the past, and one of these time units: `d` for day, `w` for week, `m` for month, or `y` for year. For example, -2d means two days into the past and 1w means one week into the future. The `now` keyword enables a comparison with the current date.<br/>
>  *  `includeTime` If `true`, then the time part of the data is included for the comparison. If the field doesn't have a time part, 00:00:00 is used.<br/>
> <br/>
> ##### Windows date validator #####<br/>
> <br/>
> A validator that checks that a date falls on or after a reference date and before or on the reference date plus a number of days.<br/>
> <br/>
>     {<br/>
>        "type": "WindowsDateValidator",<br/>
>        "configuration": {<br/>
>            "date1": "customfield_10009",<br/>
>            "date2": "created",<br/>
>            "windowsDays": 5<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `date1` The date field to validate. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datepicker`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datetime`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-end`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-start`<br/>
>      *  `duedate`<br/>
>      *  `created`<br/>
>      *  `updated`<br/>
>      *  `Resolved`<br/>
>  *  `date2` The reference date. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datepicker`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:datetime`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-end`<br/>
>      *  `com.atlassian.jpo:jpo-custom-field-baseline-start`<br/>
>      *  `duedate`<br/>
>      *  `created`<br/>
>      *  `updated`<br/>
>      *  `Resolved`<br/>
>  *  `windowsDays` A positive integer indicating a number of days.<br/>
> <br/>
> ##### Field required validator #####<br/>
> <br/>
> A validator that checks fields are not empty. By default, if a field is not included in the current context it's ignored and not validated.<br/>
> <br/>
>     {<br/>
>          "type": "FieldRequiredValidator",<br/>
>          "configuration": {<br/>
>              "ignoreContext": true,<br/>
>              "errorMessage": "Hey",<br/>
>              "fieldIds": [<br/>
>                  "versions",<br/>
>                  "customfield_10037",<br/>
>                  "customfield_10003"<br/>
>              ]<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `ignoreContext` If `true`, then the context is ignored and all the fields are validated.<br/>
>  *  `errorMessage` OPTIONAL. The error message displayed when one or more fields are empty. A default error message is shown if an error message is not provided.<br/>
>  *  `fieldIds` The list of fields to validate.<br/>
> <br/>
> ##### Field changed validator #####<br/>
> <br/>
> A validator that checks that a field value is changed. However, this validation can be ignored for users from a list of groups.<br/>
> <br/>
>     {<br/>
>          "type": "FieldChangedValidator",<br/>
>          "configuration": {<br/>
>              "fieldId": "comment",<br/>
>              "errorMessage": "Hey",<br/>
>              "exemptedGroups": [<br/>
>                  "administrators",<br/>
>                  "atlassian-addons-admin"<br/>
>              ]<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `fieldId` The ID of a field.<br/>
>  *  `errorMessage` OPTIONAL. The error message displayed if the field is not changed. A default error message is shown if the error message is not provided.<br/>
>  *  `exemptedGroups` OPTIONAL. The list of groups.<br/>
> <br/>
> ##### Field has single value validator #####<br/>
> <br/>
> A validator that checks that a multi-select field has only one value. Optionally, the validation can ignore values copied from subtasks.<br/>
> <br/>
>     {<br/>
>          "type": "FieldHasSingleValueValidator",<br/>
>          "configuration": {<br/>
>              "fieldId": "attachment,<br/>
>              "excludeSubtasks": true<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `fieldId` The ID of a field.<br/>
>  *  `excludeSubtasks` If `true`, then values copied from subtasks are ignored.<br/>
> <br/>
> ##### Parent status validator #####<br/>
> <br/>
> A validator that checks the status of the parent issue of a subtask. If the issue is not a subtask, no validation is performed.<br/>
> <br/>
>     {<br/>
>          "type": "ParentStatusValidator",<br/>
>          "configuration": {<br/>
>              "parentStatuses": [<br/>
>                  {<br/>
>                    "id":"1"<br/>
>                  },<br/>
>                  {<br/>
>                    "id":"2"<br/>
>                  }<br/>
>              ]<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `parentStatus` The list of required parent issue statuses.<br/>
> <br/>
> ##### Permission validator #####<br/>
> <br/>
> A validator that checks the user has a permission.<br/>
> <br/>
>     {<br/>
>        "type": "PermissionValidator",<br/>
>        "configuration": {<br/>
>            "permissionKey": "ADMINISTER_PROJECTS"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `permissionKey` The permission required to perform the transition. Allowed values: [built-in](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-permission-schemes/#built-in-permissions) or app defined permissions.<br/>
> <br/>
> ##### Previous status validator #####<br/>
> <br/>
> A validator that checks if the issue has held a status.<br/>
> <br/>
>     {<br/>
>        "type": "PreviousStatusValidator",<br/>
>        "configuration": {<br/>
>            "mostRecentStatusOnly": false,<br/>
>            "previousStatus": {<br/>
>                "id": "15"<br/>
>            }<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `mostRecentStatusOnly` If `true`, then only the issue's preceding status (the one immediately before the current status) is checked.<br/>
>  *  `previousStatus` An object containing the ID of an issue status.<br/>
> <br/>
> ##### Regular expression validator #####<br/>
> <br/>
> A validator that checks the content of a field against a regular expression.<br/>
> <br/>
>     {<br/>
>        "type": "RegexpFieldValidator",<br/>
>        "configuration": {<br/>
>            "regExp": "[0-9]",<br/>
>            "fieldId": "customfield_10029"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `regExp`A regular expression.<br/>
>  *  `fieldId` The ID of a field. Allowed field types:<br/>
>     <br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:select`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:multiselect`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:radiobuttons`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:multicheckboxes`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:textarea`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:textfield`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:url`<br/>
>      *  `com.atlassian.jira.plugin.system.customfieldtypes:float`<br/>
>      *  `com.pyxis.greenhopper.jira:jsw-story-points`<br/>
>      *  `com.pyxis.greenhopper.jira:gh-epic-status`<br/>
>      *  `description`<br/>
>      *  `summary`<br/>
> <br/>
> ##### User permission validator #####<br/>
> <br/>
> A validator that checks if a user has a permission. Obsolete. You may encounter this validator when getting transition rules and can pass it when updating or creating rules, for example, when you want to duplicate the rules from a workflow on a new workflow.<br/>
> <br/>
>     {<br/>
>          "type": "UserPermissionValidator",<br/>
>          "configuration": {<br/>
>              "permissionKey": "BROWSE_PROJECTS",<br/>
>              "nullAllowed": false,<br/>
>              "username": "TestUser"<br/>
>          }<br/>
>      }<br/>
> <br/>
>  *  `permissionKey` The permission to be validated. Allowed values: [built-in](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-permission-schemes/#built-in-permissions) or app defined permissions.<br/>
>  *  `nullAllowed` If `true`, allows the transition when `username` is empty.<br/>
>  *  `username` The username to validate against the `permissionKey`.<br/>
> <br/>
> #### Post functions ####<br/>
> <br/>
> Post functions carry out any additional processing required after a Jira workflow transition is executed.<br/>
> <br/>
> ##### Fire issue event function #####<br/>
> <br/>
> A post function that fires an event that is processed by the listeners.<br/>
> <br/>
>     {<br/>
>        "type": "FireIssueEventFunction",<br/>
>        "configuration": {<br/>
>          "event": {<br/>
>            "id":"1"<br/>
>          }<br/>
>        }<br/>
>      }<br/>
> <br/>
> **Note:** If provided, this post function overrides the default `FireIssueEventFunction`. Can be included once in a transition.<br/>
> <br/>
>  *  `event` An object containing the ID of the issue event.<br/>
> <br/>
> ##### Update issue status #####<br/>
> <br/>
> A post function that sets issue status to the linked status of the destination workflow status.<br/>
> <br/>
>     {<br/>
>        "type": "UpdateIssueStatusFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function is a default function in global and directed transitions. It can only be added to the initial transition and can only be added once.<br/>
> <br/>
> ##### Create comment #####<br/>
> <br/>
> A post function that adds a comment entered during the transition to an issue.<br/>
> <br/>
>     {<br/>
>        "type": "CreateCommentFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function is a default function in global and directed transitions. It can only be added to the initial transition and can only be added once.<br/>
> <br/>
> ##### Store issue #####<br/>
> <br/>
> A post function that stores updates to an issue.<br/>
> <br/>
>     {<br/>
>        "type": "IssueStoreFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function can only be added to the initial transition and can only be added once.<br/>
> <br/>
> ##### Assign to current user function #####<br/>
> <br/>
> A post function that assigns the issue to the current user if the current user has the `ASSIGNABLE_USER` permission.<br/>
> <br/>
>     {<br/>
>          "type": "AssignToCurrentUserFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function can be included once in a transition.<br/>
> <br/>
> ##### Assign to lead function #####<br/>
> <br/>
> A post function that assigns the issue to the project or component lead developer.<br/>
> <br/>
>     {<br/>
>          "type": "AssignToLeadFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function can be included once in a transition.<br/>
> <br/>
> ##### Assign to reporter function #####<br/>
> <br/>
> A post function that assigns the issue to the reporter.<br/>
> <br/>
>     {<br/>
>          "type": "AssignToReporterFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function can be included once in a transition.<br/>
> <br/>
> ##### Clear field value function #####<br/>
> <br/>
> A post function that clears the value from a field.<br/>
> <br/>
>     {<br/>
>        "type": "ClearFieldValuePostFunction",<br/>
>        "configuration": {<br/>
>          "fieldId": "assignee"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `fieldId` The ID of the field.<br/>
> <br/>
> ##### Copy value from other field function #####<br/>
> <br/>
> A post function that copies the value of one field to another, either within an issue or from parent to subtask.<br/>
> <br/>
>     {<br/>
>        "type": "CopyValueFromOtherFieldPostFunction",<br/>
>        "configuration": {<br/>
>          "sourceFieldId": "assignee",<br/>
>          "destinationFieldId": "creator",<br/>
>          "copyType": "same"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `sourceFieldId` The ID of the source field.<br/>
>  *  `destinationFieldId` The ID of the destination field.<br/>
>  *  `copyType` Use `same` to copy the value from a field inside the issue, or `parent` to copy the value from the parent issue.<br/>
> <br/>
> ##### Create Crucible review workflow function #####<br/>
> <br/>
> A post function that creates a Crucible review for all unreviewed code for the issue.<br/>
> <br/>
>     {<br/>
>          "type": "CreateCrucibleReviewWorkflowFunction"<br/>
>      }<br/>
> <br/>
> **Note:** This post function can be included once in a transition.<br/>
> <br/>
> ##### Set issue security level based on user's project role function #####<br/>
> <br/>
> A post function that sets the issue's security level if the current user has a project role.<br/>
> <br/>
>     {<br/>
>        "type": "SetIssueSecurityFromRoleFunction",<br/>
>        "configuration": {<br/>
>          "projectRole": {<br/>
>              "id":"10002"<br/>
>          },<br/>
>          "issueSecurityLevel": {<br/>
>              "id":"10000"<br/>
>          }<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `projectRole` An object containing the ID of the project role.<br/>
>  *  `issueSecurityLevel` OPTIONAL. The object containing the ID of the security level. If not passed, then the security level is set to `none`.<br/>
> <br/>
> ##### Trigger a webhook function #####<br/>
> <br/>
> A post function that triggers a webhook.<br/>
> <br/>
>     {<br/>
>        "type": "TriggerWebhookFunction",<br/>
>        "configuration": {<br/>
>          "webhook": {<br/>
>            "id": "1"<br/>
>          }<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `webhook` An object containing the ID of the webhook listener to trigger.<br/>
> <br/>
> ##### Update issue custom field function #####<br/>
> <br/>
> A post function that updates the content of an issue custom field.<br/>
> <br/>
>     {<br/>
>        "type": "UpdateIssueCustomFieldPostFunction",<br/>
>        "configuration": {<br/>
>          "mode": "append",<br/>
>          "fieldId": "customfield_10003",<br/>
>          "fieldValue": "yikes"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `mode` Use `replace` to override the field content with `fieldValue` or `append` to add `fieldValue` to the end of the field content.<br/>
>  *  `fieldId` The ID of the field.<br/>
>  *  `fieldValue` The update content.<br/>
> <br/>
> ##### Update issue field function #####<br/>
> <br/>
> A post function that updates a simple issue field.<br/>
> <br/>
>     {<br/>
>        "type": "UpdateIssueFieldFunction",<br/>
>        "configuration": {<br/>
>          "fieldId": "assignee",<br/>
>          "fieldValue": "5f0c277e70b8a90025a00776",<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `fieldId` The ID of the field. Allowed field types:<br/>
>     <br/>
>      *  `assignee`<br/>
>      *  `description`<br/>
>      *  `environment`<br/>
>      *  `priority`<br/>
>      *  `resolution`<br/>
>      *  `summary`<br/>
>      *  `timeoriginalestimate`<br/>
>      *  `timeestimate`<br/>
>      *  `timespent`<br/>
>  *  `fieldValue` The update value.<br/>
>  *  If the `fieldId` is `assignee`, the `fieldValue` should be one of these values:<br/>
>     <br/>
>      *  an account ID.<br/>
>      *  `automatic`.<br/>
>      *  a blank string, which sets the value to `unassigned`.<br/>
> <br/>
> #### Connect rules ####<br/>
> <br/>
> Connect rules are conditions, validators, and post functions of a transition that are registered by Connect apps. To create a rule registered by the app, the app must be enabled and the rule's module must exist.<br/>
> <br/>
>     {<br/>
>        "type": "appKey__moduleKey",<br/>
>        "configuration": {<br/>
>          "value":"{\"isValid\":\"true\"}"<br/>
>        }<br/>
>      }<br/>
> <br/>
>  *  `type` A Connect rule key in a form of `appKey__moduleKey`.<br/>
>  *  `value` The stringified JSON configuration of a Connect rule.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflows`

### Update workflow transition rule configurations
> Updates configuration of workflow transition rules. The following rule types are supported:<br/>
> <br/>
>  *  [post functions](https://developer.atlassian.com/cloud/jira/platform/modules/workflow-post-function/)<br/>
>  *  [conditions](https://developer.atlassian.com/cloud/jira/platform/modules/workflow-condition/)<br/>
>  *  [validators](https://developer.atlassian.com/cloud/jira/platform/modules/workflow-validator/)<br/>
> <br/>
> Only rules created by the calling Connect app can be updated.<br/>
> <br/>
> To assist with app migration, this operation can be used to:<br/>
> <br/>
>  *  Disable a rule.<br/>
>  *  Add a `tag`. Use this to filter rules in the [Get workflow transition rule configurations](https://developer.atlassian.com/cloud/jira/platform/rest/v3/api-group-workflow-transition-rules/#api-rest-api-3-workflow-rule-config-get).<br/>
> <br/>
> Rules are enabled if the `disabled` parameter is not provided.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only Connect apps can use this operation.<br/>

*Tags:* `Workflow transition rules`

### Delete workflow transition rule configurations
> Deletes workflow transition rules from one or more workflows. These rule types are supported:<br/>
> <br/>
>  *  [post functions](https://developer.atlassian.com/cloud/jira/platform/modules/workflow-post-function/)<br/>
>  *  [conditions](https://developer.atlassian.com/cloud/jira/platform/modules/workflow-condition/)<br/>
>  *  [validators](https://developer.atlassian.com/cloud/jira/platform/modules/workflow-validator/)<br/>
> <br/>
> Only rules created by the calling Connect app can be deleted.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only Connect apps can use this operation.<br/>

*Tags:* `Workflow transition rules`

### Update workflow transition property
> Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow transition properties`

#### Input Parameters
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira admin settings. The ID is shown next to the transition.<br/>
* `key` - _required_ - The key of the property being updated, also known as the name of the property. Set this to the same value as the `key` defined in the request body.<br/>
* `workflowName` - _required_ - The name of the workflow that the transition belongs to.<br/>
* `workflowMode` - _optional_ - The workflow status. Set to `live` for inactive workflows or `draft` for draft workflows. Active workflows cannot be edited.<br/>
    Possible values: live, draft.

### Create workflow transition property
> Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow transition properties`

#### Input Parameters
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira admin settings. The ID is shown next to the transition.<br/>
* `key` - _required_ - The key of the property being added, also known as the name of the property. Set this to the same value as the `key` defined in the request body.<br/>
* `workflowName` - _required_ - The name of the workflow that the transition belongs to.<br/>
* `workflowMode` - _optional_ - The workflow status. Set to *live* for inactive workflows or *draft* for draft workflows. Active workflows cannot be edited.<br/>
    Possible values: live, draft.

### Delete workflow transition property
> Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow transition properties`

#### Input Parameters
* `transitionId` - _required_ - The ID of the transition. To get the ID, view the workflow in text mode in the Jira admin settings. The ID is shown next to the transition.<br/>
* `key` - _required_ - The name of the transition property to delete, also known as the name of the property.<br/>
* `workflowName` - _required_ - The name of the workflow that the transition belongs to.<br/>
* `workflowMode` - _optional_ - The workflow status. Set to `live` for inactive workflows or `draft` for draft workflows. Active workflows cannot be edited.<br/>
    Possible values: live, draft.

### Delete inactive workflow
> Deletes a workflow.<br/>
> <br/>
> The workflow cannot be deleted if it is:<br/>
> <br/>
>  *  an active workflow.<br/>
>  *  a system workflow.<br/>
>  *  associated with any workflow scheme.<br/>
>  *  associated with any draft workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflows`

#### Input Parameters
* `entityId` - _required_ - The entity ID of the workflow.<br/>

### Create workflow scheme
> Creates a workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

### Assign workflow scheme to project
> Assigns a workflow scheme to a project. This operation is performed only when there are no issues in the project.<br/>
> <br/>
> Workflow schemes can only be assigned to classic projects.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme project associations`

### Get workflow scheme
> Returns a workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme. Find this ID by editing the desired workflow scheme in Jira. The ID is shown in the URL as `schemeId`. For example, *schemeId=10301*.<br/>
* `returnDraftIfExists` - _optional_ - Returns the workflow scheme's draft rather than scheme itself, if set to true. If the workflow scheme does not have a draft, then the workflow scheme is returned.<br/>

### Update workflow scheme
> Updates a workflow scheme, including the name, default workflow, issue type to project mappings, and more. If the workflow scheme is active (that is, being used by at least one project), then a draft workflow scheme is created or updated instead, provided that `updateDraftIfNeeded` is set to `true`.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme. Find this ID by editing the desired workflow scheme in Jira. The ID is shown in the URL as `schemeId`. For example, *schemeId=10301*.<br/>

### Delete workflow scheme
> Deletes a workflow scheme. Note that a workflow scheme cannot be deleted if it is active (that is, being used by at least one project).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme. Find this ID by editing the desired workflow scheme in Jira. The ID is shown in the URL as `schemeId`. For example, *schemeId=10301*.<br/>

### Create draft workflow scheme
> Create a draft workflow scheme from an active workflow scheme, by copying the active workflow scheme. Note that an active workflow scheme can only have one draft workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft is created from.<br/>

### Update default workflow
> Sets the default workflow for a workflow scheme.<br/>
> <br/>
> Note that active workflow schemes cannot be edited. If the workflow scheme is active, set `updateDraftIfNeeded` to `true` in the request object and a draft workflow scheme is created or updated with the new default workflow. The draft workflow scheme can be published in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>

### Delete default workflow
> Resets the default workflow for a workflow scheme. That is, the default workflow is set to Jira's system workflow (the *jira* workflow).<br/>
> <br/>
> Note that active workflow schemes cannot be edited. If the workflow scheme is active, set `updateDraftIfNeeded` to `true` and a draft workflow scheme is created or updated with the default workflow reset. The draft workflow scheme can be published in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>
* `updateDraftIfNeeded` - _optional_ - Set to true to create or update the draft of a workflow scheme and delete the mapping from the draft, when the workflow scheme cannot be edited. Defaults to `false`.<br/>

### Update draft workflow scheme
> Updates a draft workflow scheme. If a draft workflow scheme does not exist for the active workflow scheme, then a draft is created. Note that an active workflow scheme can only have one draft workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft was created from.<br/>

### Delete draft workflow scheme
> Deletes a draft workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the active workflow scheme that the draft was created from.<br/>

### Update draft default workflow
> Sets the default workflow for a workflow scheme's draft.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>

### Delete draft default workflow
> Resets the default workflow for a workflow scheme's draft. That is, the default workflow is set to Jira's system workflow (the *jira* workflow).<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>

### Get workflow for issue type in draft workflow scheme
> Returns the issue type-workflow mapping for an issue type in a workflow scheme's draft.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>
* `issueType` - _required_ - The ID of the issue type.<br/>

### Set workflow for issue type in draft workflow scheme
> Sets the workflow for an issue type in a workflow scheme's draft.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>
* `issueType` - _required_ - The ID of the issue type.<br/>

### Delete workflow for issue type in draft workflow scheme
> Deletes the issue type-workflow mapping for an issue type in a workflow scheme's draft.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>
* `issueType` - _required_ - The ID of the issue type.<br/>

### Publish draft workflow scheme
> Publishes a draft workflow scheme.<br/>
> <br/>
> Where the draft workflow includes new workflow statuses for an issue type, mappings are provided to update issues with the original workflow status to the new workflow status.<br/>
> <br/>
> This operation is [asynchronous](#async). Follow the `location` link in the response to determine the status of the task and use [Get task](#api-rest-api-3-task-taskId-get) to obtain updates.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>
* `validateOnly` - _optional_ - Whether the request only performs a validation.<br/>

### Set issue types for workflow in workflow scheme
> Sets the issue types for a workflow in a workflow scheme's draft. The workflow can also be set as the default workflow for the draft workflow scheme. Unmapped issues types are mapped to the default workflow.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>
* `workflowName` - _required_ - The name of the workflow.<br/>

### Delete issue types for workflow in draft workflow scheme
> Deletes the workflow-issue type mapping for a workflow in a workflow scheme's draft.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow scheme drafts`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme that the draft belongs to.<br/>
* `workflowName` - _required_ - The name of the workflow.<br/>

### Get workflow for issue type in workflow scheme
> Returns the issue type-workflow mapping for an issue type in a workflow scheme.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>
* `issueType` - _required_ - The ID of the issue type.<br/>
* `returnDraftIfExists` - _optional_ - Returns the mapping from the workflow scheme's draft rather than the workflow scheme, if set to true. If no draft exists, the mapping from the workflow scheme is returned.<br/>

### Set workflow for issue type in workflow scheme
> Sets the workflow for an issue type in a workflow scheme.<br/>
> <br/>
> Note that active workflow schemes cannot be edited. If the workflow scheme is active, set `updateDraftIfNeeded` to `true` in the request body and a draft workflow scheme is created or updated with the new issue type-workflow mapping. The draft workflow scheme can be published in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>
* `issueType` - _required_ - The ID of the issue type.<br/>

### Delete workflow for issue type in workflow scheme
> Deletes the issue type-workflow mapping for an issue type in a workflow scheme.<br/>
> <br/>
> Note that active workflow schemes cannot be edited. If the workflow scheme is active, set `updateDraftIfNeeded` to `true` and a draft workflow scheme is created or updated with the issue type-workflow mapping deleted. The draft workflow scheme can be published in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>
* `issueType` - _required_ - The ID of the issue type.<br/>
* `updateDraftIfNeeded` - _optional_ - Set to true to create or update the draft of a workflow scheme and update the mapping in the draft, when the workflow scheme cannot be edited. Defaults to `false`.<br/>

### Set issue types for workflow in workflow scheme
> Sets the issue types for a workflow in a workflow scheme. The workflow can also be set as the default workflow for the workflow scheme. Unmapped issues types are mapped to the default workflow.<br/>
> <br/>
> Note that active workflow schemes cannot be edited. If the workflow scheme is active, set `updateDraftIfNeeded` to `true` in the request body and a draft workflow scheme is created or updated with the new workflow-issue types mappings. The draft workflow scheme can be published in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>
* `workflowName` - _required_ - The name of the workflow.<br/>

### Delete issue types for workflow in workflow scheme
> Deletes the workflow-issue type mapping for a workflow in a workflow scheme.<br/>
> <br/>
> Note that active workflow schemes cannot be edited. If the workflow scheme is active, set `updateDraftIfNeeded` to `true` and a draft workflow scheme is created or updated with the workflow-issue type mapping deleted. The draft workflow scheme can be published in Jira.<br/>
> <br/>
> **[Permissions](#permissions) required:** *Administer Jira* [global permission](https://confluence.atlassian.com/x/x4dKLg).<br/>

*Tags:* `Workflow schemes`

#### Input Parameters
* `id` - _required_ - The ID of the workflow scheme.<br/>
* `workflowName` - _required_ - The name of the workflow.<br/>
* `updateDraftIfNeeded` - _optional_ - Set to true to create or update the draft of a workflow scheme and delete the mapping from the draft, when the workflow scheme cannot be edited. Defaults to `false`.<br/>

### Get worklogs
> Returns worklog details for a list of worklog IDs.<br/>
> <br/>
> The returned list of worklogs is limited to 1000 items.<br/>
> <br/>
> **[Permissions](#permissions) required:** Permission to access Jira, however, worklogs are only returned where either of the following is true:<br/>
> <br/>
>  *  the worklog is set as *Viewable by All Users*.<br/>
>  *  the user is a member of a project role or group with permission to view the worklog.<br/>

*Tags:* `Issue worklogs`

#### Input Parameters
* `expand` - _optional_ - Use [expand](#expansion) to include additional information about worklogs in the response. This parameter accepts `properties` that returns the properties of each worklog.<br/>

### Get app property
> Returns the key and value of an app's property.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only a Connect app whose key matches `addonKey` can make this request.<br/>

*Tags:* `App properties`

#### Input Parameters
* `addonKey` - _required_ - The key of the app, as defined in its descriptor.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Set app property
> Sets the value of an app's property. Use this resource to store custom data for your app.<br/>
> <br/>
> The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 characters.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only a Connect app whose key matches `addonKey` can make this request.<br/>

*Tags:* `App properties`

#### Input Parameters
* `addonKey` - _required_ - The key of the app, as defined in its descriptor.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Delete app property
> Deletes an app's property.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only a Connect app whose key matches `addonKey` can make this request.<br/>

*Tags:* `App properties`

#### Input Parameters
* `addonKey` - _required_ - The key of the app, as defined in its descriptor.<br/>
* `propertyKey` - _required_ - The key of the property.<br/>

### Register modules
> Registers a list of modules.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only Connect apps can make this request.<br/>

*Tags:* `Dynamic modules`

### Remove modules
> Remove all or a list of modules registered by the calling app.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only Connect apps can make this request.<br/>

*Tags:* `Dynamic modules`

#### Input Parameters
* `moduleKey` - _optional_ - The key of the module to remove. To include multiple module keys, provide multiple copies of this parameter.<br/>
For example, `moduleKey=dynamic-attachment-entity-property&moduleKey=dynamic-select-field`.<br/>
Nonexistent keys are ignored.<br/>

### Bulk update custom field value
> Updates the value of a custom field added by Connect apps on one or more issues.<br/>
> The values of up to 200 custom fields can be updated.<br/>
> <br/>
> **[Permissions](#permissions) required:** Only Connect apps can make this request.<br/>

*Tags:* `App migration`

#### Input Parameters
* `Atlassian-Transfer-Id` - _required_ - The ID of the transfer.<br/>
* `Atlassian-Account-Id` - _required_ - The Atlassian account ID of the impersonated user. This user must be a member of the site admin group.<br/>

### Bulk update entity properties
> Updates the values of multiple entity properties for an object, up to 50 updates per request. This operation is for use by Connect apps during app migration.<br/>

*Tags:* `App migration`

#### Input Parameters
* `Atlassian-Transfer-Id` - _required_ - The app migration transfer ID.<br/>
* `Atlassian-Account-Id` - _required_ - The Atlassian account ID of the impersonated user. This user must be a member of the site admin group.<br/>
* `entityType` - _required_ - The type indicating the object that contains the entity properties.<br/>
    Possible values: IssueProperty, CommentProperty, DashboardItemProperty, IssueTypeProperty, ProjectProperty, UserProperty, WorklogProperty, BoardProperty, SprintProperty.

### Get workflow transition rule configurations
> Returns configurations for workflow transition rules migrated from server to cloud and owned by the calling Connect app.<br/>

*Tags:* `App migration`

#### Input Parameters
* `Atlassian-Transfer-Id` - _required_ - The app migration transfer ID.<br/>

## License

: jira-component<br/>
                    <br/>

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
