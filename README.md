## Disclaimer

**Note:** This repository is mainly based on code from [mariusz-ostoja-swierczynski/tech-controllers](https://github.com/mariusz-ostoja-swierczynski/tech-controllers), which is currently stalled. I have created this repository for my own purposes and integrated some code lines from [MichalKrasowski/tech-controllers](https://github.com/MichalKrasowski/tech-controllers) to make it running. Kudos to proevious codeowners :) 
I've decided to move on as both repos lacked thing I need - multiple controllers support.

My primary goal with this repository is to provide a stable integration for TECH Controllers in Home Assistant, specifically for controllers with at least L-4 WiFi capability, which I personally own and use daily. If there are any changes in the API that would prevent this integration from working, I will aim to update it as soon as possible.

It's important to note that I am not an active developer, and my knowledge of Home Assistant integrations is limited. As a result, there are no warranties provided, and I cannot take responsibility for any problems that may arise from using this integration, although I do not anticipate any issues.

## Description

The TECH Controllers integration for Home Assistant allows you to control heating controllers manufactured by the Polish company TECH Sterowniki Sp. z o.o. This integration is based on the API provided by TECH, which *supposedly* supports the following controllers:

- L-4 Wifi
- L-7
- L-7E
- L-8
- WiFi 8S
- ST-8S WiFi
- ST-16S WIFI
- M-9

To use this integration, your controller needs to be accessible from the internet, and you must have an account on either [https://emodul.eu](https://emodul.eu) or [https://emodul.pl](https://emodul.pl).

## Features

- Configuration through Integrations (not via configuration.yaml)
- Support for multiple controllers
- Climate entities representing zones in the household
- Climate entities display data through Thermostat card
- Zone names
- Current zone temperature
- Target zone temperature
- Current zone state (heating or idle)
- Display and control for zone mode (on or off)

## Installation

Follow these steps to install and set up the Tech Controllers integration in Home Assistant:

1. Copy the entire contents of this repository into your Home Assistant's `config/custom_components/tech` folder.
   - **Note:** If the `custom_components` folder does not exist in your Home Assistant installation, you will need to create it first, and then create a `tech` folder inside it.

2. Restart your Home Assistant instance.

3. In the Home Assistant web interface, navigate to `Configuration` -> `Integrations`.

4. Click the `Add` button to add a new integration.

5. Search for "Tech Controllers" integration and select it.

6. Enter your username (could be an email) and password for your eModule account and click the "Submit" button.

7. You should see a "Success!" dialog with the name and version of your main Tech controller.
   - **Note:** The integration currently supports handling only one controller. If the API returns a list of more than one controller in your household, only the first one will be used.

8. You should now have Climate entities representing your home zones available in Home Assistant. To add these Climate entities to your Home Assistant UI Lovelace configuration, follow these steps:

   - Go to your Home Assistant UI Lovelace configuration.
   - Add a Thermostat card and select your Climate entities.

![Tech Controllers Setup 1](/custom_components/tech/images/ha-tech-add-integration-1.png)

![Tech Controllers Setup 2](/custom_components/tech/images/ha-tech-add-integration-2.png)

![Tech Controllers Setup 3](/custom_components/tech/images/ha-tech-add-integration-3.png)

![Tech Controllers Setup 4](/custom_components/tech/images/ha-tech-2.png)
