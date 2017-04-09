# Wimpy Slack
Ansible role to notify a Slack channel when you deploy your application using Wimpy.

## Required Parameters
The required parameters are

  - `wimpy_project_name`: Project's name.
  - `wimpy_release_version`: Version being deployed.
  - `wimpy_deployment_status`: Current status for the deployment.
  - `wimpy_slack_channel`: Channel where the message will be published.
  - `wimpy_slack_token`: Something like `G922VJP24/D921DW937/3Ffe373sfhRE6y42Fg3rvf4GlK`.

## Optional Parameters
The optional parameters are

  - `wimpy_slack_icon`: Url for the message sender's icon.
  - `wimpy_slack_username`: This is the sender of the message. 
  - `wimpy_slack_color`: Color for the message: normal|good|warning|danger. 
  - `wimpy_slack_message`: Message to publish. 

## Usage

```yaml
- hosts: localhost
  connection: local
  vars:
    wimpy_project_name: "my-project"
    wimpy_release_version: "9da8s9fud8"
    wimpy_deployment_status: "Success"
    wimpy_slack_channel: "#my-channel"
    wimpy_slack_token: G922VJP24/D921DW937/3Ffe373sfhRE6y42Fg3rvf4GlK
  roles:
    - wimpy.slack
```
