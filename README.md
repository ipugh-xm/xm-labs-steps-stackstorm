# StackStorm Steps

This step allows you to call an HTTP Trigger in StackStorm.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [StackStormSteps.zip](StackStormSteps.zip) - Workflow zip file with the step and example flow
* [stackstorm.png](/stackstorm.png) - StackStorm logo

# How it works
This step calls a webhook in StackStorm.


# Installation

## StackStorm Setup
Create an API Key in Stackstorm.

To do this from the command line, run `st2 apikey create -k -m '{"used_by": "xm"}'`

## xMatters Setup
1. Download the [StackStormSteps.zip](StackStormSteps.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Add an Endpoint for StackStorm. `https://example.com/api/v1`
5. Add the API Key as a constant in xMatters


## Usage
The **StackStorm - Post Webhook** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **StackStorm - Post Webhook** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Api Key | Yes | 0 | 2000 | The Auth Token used in the header | | No |
| Body | Yes | 0 | 2000 | The Body of the POST Request | | No |
| Path | Yes | 0 | 2000 | Path for the webhook (everything after `/webhooks/`) | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| result | The full JSON Output of the API Call |



## Example
This is an example of an xMatters webhook calling a webhook in StackStorm. 

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

