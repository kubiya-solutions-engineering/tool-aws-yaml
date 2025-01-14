# Amazon Web Services Command Line Interface (AWS-CLI) tool

This tool definition wraps a Docker Hub container containing the AWS CLI into a tool. Can be used
by Kubiya Teammates to access AWS using CLI commands.

# Installation

## Pre-requisites

To use this tool:
- Create a new role with the required permissions as needed on AWS Console.
- Create an AWS Integration on the Kubiya Web App, [app.kubiya.ai](app.kubiya.ai).

## Uploading the tool as a new Source

1. Navigate to the Kubiya Web App, [app.kubiya.ai](https://app.kubiya.ai). Login if needed.
2. Select *Resources*, *Sources*, and then *+ New Source*.
3. Copy and paste this respository's URL into the text box *Source URL* and select *Load tools &
workflows*.
4. Under *Tools & workflows discovered* you should see a list of tools associated with this
repository.
5. Select *+ Create*.

The tool is now available for use by a Teammate.

# Usage

Depending on the roles and access assigned to the associated user, this tool can execute any command
using the AWS CLI, as indicated below:

    aws {{.command}}

This gives the tool significant ability to affect change on your AWS account. Therefore it is highly
recommended to ensure that appropriate roles and access is assigned.

In addition, this tool can be modified to only execute one type of command. For example:

    aws s3 ls {{.command}}

# Contact

Please contact the author of this tool using the email address:
[support@kubiya.ai](mailto:support@kubiya.ai).
